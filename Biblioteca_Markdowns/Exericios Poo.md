
# 📘 Exercícios – Funções, Classes, Decoradores e POO em Python

---

## 🔹 Módulo 1 – Funções (10 exercícios)

### 🟢 Básico
1. Crie uma função que receba dois números e retorne a soma.
2. Crie uma função que verifique se um número é par ou ímpar.
3. Escreva uma função que calcule o fatorial de um número.
4. Crie uma função que receba uma lista de preços e aplique um desconto de 10% em todos.
5. Crie uma função que receba um nome e imprima "Olá, [nome]!".

### 🔴 Avançado
6. Crie uma função que receba qualquer número de argumentos e retorne a média deles.
7. Escreva uma função que retorne o maior e o menor número de uma lista.
8. Implemente uma função lambda que eleve um número ao quadrado.
9. Crie uma função que simule um cálculo de IR com faixas progressivas.
10. Crie uma função que use `map()` e `filter()` para retornar somente os valores maiores que 100 com 20% de acréscimo.

---

## 🔹 Módulo 2 – Classes (10 exercícios)

### 🟢 Básico
1. Crie uma classe `Pessoa` com atributos `nome` e `idade`.
2. Adicione um método `apresentar()` que imprime nome e idade.
3. Crie uma classe `Produto` com método `aplicar_desconto(percentual)`.
4. Crie uma classe `Livro` com método que informa se ele está disponível ou emprestado.
5. Instancie 3 objetos de uma classe `Funcionario` e mostre seus dados.

### 🔴 Avançado
6. Crie uma classe `ContaBancaria` com métodos `depositar`, `sacar` e `ver_saldo`.
7. Crie uma classe `Investimento` com cálculo de rendimento mensal.
8. Implemente `__str__` para uma classe `Cliente` imprimir seus dados bonitos.
9. Crie uma classe `RelatorioFinanceiro` que recebe uma lista de centros de custo e calcula a margem média.
10. Adicione validação (ex: impedir que um valor negativo seja atribuído a custo) usando métodos personalizados.

---

## 🔹 Módulo 3 – Decoradores (10 exercícios)

### 🟢 Básico
1. Crie um decorador que imprime "Executando função..." antes da execução.
2. Crie um decorador que mede tempo de execução.
3. Crie um decorador que transforma o retorno da função em maiúsculas.
4. Crie um decorador que só executa uma função se o usuário estiver logado (`logado=True`).
5. Crie um decorador que loga os argumentos da função.

### 🔴 Avançado
6. Crie um decorador com argumentos (ex: `@logar("INÍCIO")`) que imprime uma tag antes da execução.
7. Crie um decorador que cacheia o resultado de funções caras (`functools.lru_cache`).
8. Crie um decorador que conta quantas vezes a função foi chamada.
9. Combine dois decoradores em uma mesma função.
10. Aplique um decorador para medir o tempo de um carregamento de dados simulado com `time.sleep`.

---

## 🔹 Módulo 4 – Programação Orientada a Objetos (POO) (10 exercícios)

### 🟢 Básico
1. Crie uma classe `Aluno` e uma subclasse `AlunoFinanceiro`.
2. Use herança para criar uma classe `Analista` que herda de `Funcionario`.
3. Crie um método `calcular_salario()` que some base + bônus.
4. Implemente encapsulamento para proteger um atributo sensível (`__senha`).
5. Crie uma classe com método estático que converta dólar para real.

### 🔴 Avançado
6. Implemente polimorfismo com duas classes `VendaOnline` e `VendaLoja` com método `emitir_nota()`.
7. Use `@property` e `@setter` para criar um atributo controlado.
8. Crie um sistema que gerencia vários produtos e calcula a média de preços com métodos de classe.
9. Crie uma hierarquia de classes para contas bancárias com tipos (Corrente, Poupança).
10. Crie uma classe abstrata `Relatorio` com método `gerar()` e subclasses que implementam esse método.

---

## 🔄 Exercícios Finais – Integração de Tudo (10 exercícios)

1. Crie uma função que recebe um DataFrame com receita e custo e retorna margem.
2. Crie uma classe `CentroCusto` com atributos, métodos e validações.
3. Aplique um decorador para medir o tempo de execução do cálculo de margens em vários centros.
4. Crie uma lista de objetos `CentroCusto` e calcule a média das margens.
5. Crie uma função que recebe uma lista de produtos (como dicionários) e os transforma em objetos.
6. Crie uma classe que representa uma Análise Financeira com métodos para gerar relatórios com base em pandas.
7. Aplique decoradores para validar os dados de entrada antes de gerar o relatório.
8. Use herança para criar diferentes tipos de relatórios (`Mensal`, `Anual`).
9. Crie uma função de utilidade com `*args` e `**kwargs` que filtra os dados de forma dinâmica.
10. Combine tudo em um script que lê um CSV, transforma em objetos, calcula margens e imprime um relatório formatado.

---
