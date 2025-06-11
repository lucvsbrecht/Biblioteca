# SQL

# PostGreSQL Documentação

[https://www.notion.so](https://www.notion.so)

# Códigos auxiliares

## Ordem Exexução

![Fqtt03faAAAdyYp.jpeg](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Fqtt03faAAAdyYp.jpeg)

## Duvidas Aleatórias que surgiram durante a Vida

### Qual a diferença de usar With e Sub-Query?

O que o eu, Lucas entendi no momento que surgiu a dúvida:

É que, me parece, que sub-query possui uma leitura mais complicada, o código me parece mais desorganizado, em um teste, o desempenho com o With ficou melhor. Percebi tambpem que consigo referenciar o With outras vezes, coisa que não consigo na Subquery

O que meu amigo robozinho entende:

### **`WITH` (Common Table Expressions - CTE) vs. Subquery no PostgreSQL**

Tanto **`WITH` (CTE)** quanto **subqueries** permitem criar consultas intermediárias para organizar o código SQL. No entanto, existem diferenças de desempenho e legibilidade entre elas.

---

## 📌 **1. O que é uma Subquery?**

Uma **subquery (subconsulta)** é uma consulta aninhada dentro de outra. Ela pode ser usada em `SELECT`, `FROM` ou `WHERE`.

### **🔹 Exemplo de Subquery no `FROM`**

```sql
SELECT ranked.*
FROM (
    SELECT
        produtos.product_id AS "Código do Produto",
        produtos.product_name AS "Nome do Produto",
        SUM(detalhes.quantity) AS "Quantidade Total Vendida",
        RANK() OVER (ORDER BY SUM(detalhes.quantity) DESC) AS "Ranking"
    FROM public.order_details detalhes
    LEFT JOIN public.products produtos
        ON detalhes.product_id = produtos.product_id
    GROUP BY produtos.product_id, produtos.product_name
) ranked
WHERE ranked."Ranking" <= 5;

```

✔ **Vantagens:**

- Não precisa de nome global para a subquery.
- Pode ser usada dentro de `SELECT`, `FROM` ou `WHERE`.

❌ **Desvantagens:**

- Pode ficar difícil de ler quando há muitas subqueries aninhadas.
- Em alguns casos, pode ser **menos eficiente** do que `WITH`, pois a subquery pode ser recalculada várias vezes.

---

## 📌 **2. O que é `WITH` (CTE - Common Table Expression)?**

O `WITH` cria uma **tabela temporária nomeada** que pode ser reutilizada na consulta principal.

### **🔹 Exemplo de `WITH` (CTE)**

```sql
WITH ranked AS (
    SELECT
        produtos.product_id AS "Código do Produto",
        produtos.product_name AS "Nome do Produto",
        SUM(detalhes.quantity) AS "Quantidade Total Vendida",
        RANK() OVER (ORDER BY SUM(detalhes.quantity) DESC) AS "Ranking"
    FROM public.order_details detalhes
    LEFT JOIN public.products produtos
        ON detalhes.product_id = produtos.product_id
    GROUP BY produtos.product_id, produtos.product_name
)
SELECT * FROM ranked WHERE "Ranking" <= 5;

```

✔ **Vantagens:**

- **Código mais legível**, pois você pode nomear e reutilizar a CTE.
- **Reutilização**: Se precisar da mesma consulta em diferentes partes do código, basta referenciar a CTE.
- **Melhor otimização pelo PostgreSQL**, pois a CTE pode ser materializada (armazenada temporariamente) antes de ser usada.

❌ **Desvantagens:**

- Se a CTE **não for inline**, pode consumir mais memória.

---

## 📌 **3. Quando usar `WITH` (CTE) ou Subquery?**

| Situação | Usar `WITH` (CTE) | Usar Subquery |
| --- | --- | --- |
| Código mais organizado e reutilizável | ✅ Sim | ❌ Não |
| Melhor desempenho ao evitar recalculações | ✅ Sim | ❌ Pode ser ruim |
| Simples e rápida, sem necessidade de reutilização | ❌ Pode ser exagero | ✅ Sim |
| PostgreSQL precisa otimizar a execução | ✅ Sim | ❌ Pode repetir cálculos |

---

### **📌 Resumo Final**

- Use **`WITH` (CTE)** quando precisar de **código organizado e reutilizável**.
- Use **subquery** para **consultas simples** que não precisam ser reutilizadas.
- Para **grandes conjuntos de dados**, **testar o desempenho** pode ser importante para escolher a melhor abordagem.

🚀 Agora você pode decidir qual usar no seu SQL! Se precisar de mais detalhes, me avise. 😊

Comentario Final: Me parece que estava certo :)

## Verificar informações das tabelas

```sql
SELECT column_name, data_type 
FROM information_schema.columns 
WHERE table_name = 'zzz';
```

## Verificar primeira linha

```sql
SELECT * FROM schema.table 
LIMIT 2;
```

## Utilização de IF (No caso, em SQL é o Case)

```sql
SELECT id, 
       nome, 
       salario,
       CASE 
           WHEN salario > 5000 THEN 'Alto'
           WHEN salario BETWEEN 3000 AND 5000 THEN 'Médio'
           ELSE 'Baixo'
       END AS categoria_salario
FROM funcionarios;

```

## Utilização do Having

```sql
SELECT detalhes.product_id AS "Código do Produto",
       SUM(detalhes.quantity) AS "Quantidade Total Vendida"
FROM public.order_details detalhes
GROUP BY detalhes.product_id
HAVING SUM(detalhes.quantity) > 100;
```

## Utilização do RANK()

```sql
SELECT 
    produtos.category_id AS "Código da Categoria",
    produtos.product_id AS "Código do Produto",
    produtos.product_name AS "Nome do Produto",
    SUM(detalhes.quantity) AS "Quantidade Total Vendida",
    ROUND(SUM(detalhes.quantity * detalhes.unit_price)::NUMERIC, 2) AS "Total",
    RANK() OVER (
        PARTITION BY produtos.category_id 
        ORDER BY SUM(detalhes.quantity * detalhes.unit_price) DESC
    ) AS "Ranking"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id
GROUP BY produtos.category_id, produtos.product_id, produtos.product_name;

```

## Utilização de Funções de Janela para substituir Group By

```sql
SELECT DISTINCT
    produtos.category_id AS "Código da Categoria",
    produtos.product_id AS "Código do Produto",
    produtos.product_name AS "Nome do Produto",
    SUM(detalhes.quantity * detalhes.unit_price) OVER (
        PARTITION BY produtos.category_id, produtos.product_id, produtos.product_name
    ) AS "Total"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id;
```

No exemplo abaixo, as duas querys estão fazendo a mesma coisa, o resultado é o mesmo, me fica como sugestão testar a eficiência com um conjunto de dados mais pesado

```sql
SELECT 
    pedidos.order_id AS "Numero do Pedido",
    detalhes.product_id AS "Código do Produto",
    pedidos.order_date AS "Data do Pedido",
    pedidos.freight AS "Peso Pedido",
    pedidos.ship_city AS "Cidade Destino",
    detalhes.quantity AS "Quantidade",
    detalhes.unit_price AS "Preço Unitário",
    ROUND((detalhes.quantity * detalhes.unit_price)::NUMERIC, 2) AS "Total"
FROM public.orders pedidos
LEFT JOIN public.order_details detalhes 
    ON pedidos.order_id = detalhes.order_id;

SELECT DISTINCT
    produtos.category_id AS "Código da Categoria",
    produtos.product_id AS "Código do Produto",
    produtos.product_name AS "Nome do Produto",
	COUNT (*) OVER (
        PARTITION BY produtos.category_id, produtos.product_id, produtos.product_name
    ) AS "Numero de Vendas",
    SUM(detalhes.quantity * detalhes.unit_price) OVER (
        PARTITION BY produtos.category_id, produtos.product_id, produtos.product_name
    ) AS "Total"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id
WHERE 
	produtos.category_id = 7;

SELECT DISTINCT
    produtos.category_id AS "Código da Categoria",
	COUNT (*) OVER (
        PARTITION BY produtos.category_id
    ) AS "Numero de Vendas",
    SUM(detalhes.quantity * detalhes.unit_price) OVER (
        PARTITION BY produtos.category_id
    ) AS "Total"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id
WHERE 
	produtos.category_id = 7;

SELECT
    produtos.category_id AS "Código da Categoria",
	COUNT (*) AS "Numero de Vendas",
    SUM(detalhes.quantity * detalhes.unit_price) "Total"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id
WHERE 
	produtos.category_id = 7
GROUP BY
    produtos.category_id;
```

Tentei urilizar uma função Janela junto com o RANK, mas não sei se o PostDegrees não aceita ou se é algo em comum no SQL, inclusive em outros bancos. Vou colocar a idéia aqui para poder testar em no Banco Oracle ou SQLServer da Luft

```sql
SELECT DISTINCT
    produtos.category_id AS "Código da Categoria",
    produtos.product_id AS "Código do Produto",
    produtos.product_name AS "Nome do Produto",
    SUM(detalhes.quantity * detalhes.unit_price) OVER (
        PARTITION BY produtos.category_id, produtos.product_id, produtos.product_name
    ) AS "Total",
    RANK() OVER (
        PARTITION BY produtos.category_id 
        ORDER BY SUM(detalhes.quantity * detalhes.unit_price) OVER (
            PARTITION BY produtos.category_id, produtos.product_id, produtos.product_name
        ) DESC
    ) AS "Ranking"
FROM public.order_details detalhes
LEFT JOIN public.products produtos 
    ON detalhes.product_id = produtos.product_id;
```
