Perfeito! Vamos montar um **mini curso completo**, com **explicações aprofundadas e progressivas** sobre:

1. **Funções**
2. **Classes**
3. **Decoradores**
4. **Programação Orientada a Objetos (POO)**

Tudo com foco em **análise de dados e finanças**.

---

# 📘 Módulo 1 – Funções em Python (do Básico ao Avançado)

## 🔹 O que é uma função?

Uma função é um **bloco de código com um nome**, que você pode **chamar (executar)** sempre que quiser. Serve para **organizar o código**, **evitar repetição** e **facilitar a manutenção**.

### 📌 Exemplo didático:

```python
def somar(a, b):
    resultado = a + b
    return resultado
```

Essa função:

* Se chama `somar`
* Recebe dois parâmetros: `a` e `b`
* Retorna a soma dos dois

### 💡 Chamada:

```python
print(somar(10, 5))  # Saída: 15
```

---

## 🔹 Por que usar funções?

Imagine que você precise calcular imposto sobre várias vendas:

```python
def calcular_imposto(valor, taxa=0.15):
    return valor * taxa
```

Chamadas:

```python
print(calcular_imposto(1000))      # 150
print(calcular_imposto(2000, 0.2)) # 400
```

---

## 🔹 Tipos de argumentos

```python
def exemplo(a, b=10, *args, **kwargs):
    pass
```

| Tipo       | Exemplo        | Explicação                    |
| ---------- | -------------- | ----------------------------- |
| `a`        | Obrigatório    | Precisa ser passado           |
| `b=10`     | Default        | Valor padrão                  |
| `*args`    | Vários valores | Tupla de valores extras       |
| `**kwargs` | Chave=valor    | Dicionário com pares nomeados |

---

## 🔹 Funções lambda (anônimas)

```python
imposto = lambda valor: valor * 0.15
print(imposto(1000))  # 150.0
```

Boa para usar dentro de `.apply()` no pandas.

---

## 🔹 Funções em análise de dados

Exemplo: aplicar imposto a uma coluna de DataFrame:

```python
import pandas as pd

df = pd.DataFrame({'venda': [100, 200, 300]})

def aplicar_imposto(valor):
    return valor * 0.15

df['imposto'] = df['venda'].apply(aplicar_imposto)
print(df)
```

---

# 🧱 Módulo 2 – Classes em Python

## 🔹 O que é uma classe?

Uma **classe** é como um **molde** que define como serão os objetos.

Exemplo de classe que representa um produto:

```python
class Produto:
    def __init__(self, nome, preco):
        self.nome = nome
        self.preco = preco

    def aplicar_desconto(self, percentual):
        self.preco -= self.preco * percentual
```

### 🔍 Explicando:

* `__init__`: método especial chamado quando criamos o objeto
* `self`: referência ao próprio objeto
* `self.nome`, `self.preco`: atributos

### 🔧 Criando objetos:

```python
p1 = Produto("Notebook", 3000)
p1.aplicar_desconto(0.1)
print(p1.preco)  # 2700.0
```

---

## 🔹 Atributos vs Métodos

| Conceito | O que é                   | Exemplo                   |
| -------- | ------------------------- | ------------------------- |
| Atributo | Dado do objeto            | `self.nome`, `self.preco` |
| Método   | Função que atua no objeto | `.aplicar_desconto()`     |

---

## 🔹 Classes em finanças

Classe que calcula margem de lucro:

```python
class Lucro:
    def __init__(self, receita, custo):
        self.receita = receita
        self.custo = custo

    def margem(self):
        return (self.receita - self.custo) / self.receita
```

Uso:

```python
lucro = Lucro(10000, 7000)
print(lucro.margem())  # 0.3 ou 30%
```

---

# 🎁 Módulo 3 – Decoradores em Python

## 🔹 O que são decoradores?

Decoradores são **funções que recebem outra função como argumento**, **modificam ou estendem seu comportamento** e **a devolvem**.

### Exemplo básico:

```python
def meu_decorador(func):
    def wrapper():
        print("Antes da função")
        resultado = func()
        print("Depois da função")
        return resultado
    return wrapper

@meu_decorador
def diz_oi():
    print("Oi!")

diz_oi()
```

### Saída:

```
Antes da função
Oi!
Depois da função
```

---

## 🔹 Decoradores com parâmetros

```python
def logar(func):
    def wrapper(*args, **kwargs):
        print(f"Executando {func.__name__} com {args} {kwargs}")
        return func(*args, **kwargs)
    return wrapper

@logar
def somar(a, b):
    return a + b

print(somar(5, 3))
```

---

## 🔹 Decoradores em análise de dados

### Medir tempo de execução:

```python
import time

def tempo_execucao(func):
    def wrapper(*args, **kwargs):
        inicio = time.time()
        resultado = func(*args, **kwargs)
        fim = time.time()
        print(f"Executado em {fim - inicio:.2f}s")
        return resultado
    return wrapper

@tempo_execucao
def carregar_dados():
    time.sleep(1)
    print("Dados carregados")

carregar_dados()
```

---

# 🧭 Módulo 4 – Programação Orientada a Objetos (POO)

## 🔹 Pilares da POO

| Pilar              | Explicação                                   | Exemplo                           |
| ------------------ | -------------------------------------------- | --------------------------------- |
| **Abstração**      | Esconder complexidade                        | `.resumo()` sem saber os detalhes |
| **Encapsulamento** | Ocultar atributos internos                   | `self.__custo`                    |
| **Herança**        | Uma classe herda outra                       | `class Analista(Funcionario)`     |
| **Polimorfismo**   | Métodos com o mesmo nome funcionam diferente | `.calcular()` em várias classes   |

---

## 🔹 Exemplo real – Lucro por Centro de Custo com POO

```python
class CentroCusto:
    def __init__(self, nome, receita, custo):
        self.nome = nome
        self.receita = receita
        self.custo = custo

    def calcular_lucro(self):
        return self.receita - self.custo

    def margem(self):
        return self.calcular_lucro() / self.receita
```

### Vários centros:

```python
centros = [
    CentroCusto("TI", 10000, 7000),
    CentroCusto("RH", 8000, 3000),
    CentroCusto("Logística", 12000, 11000)
]

for c in centros:
    print(f"{c.nome} | Lucro: R${c.calcular_lucro()} | Margem: {c.margem():.1%}")
```

---

## ➕ Próximos Passos

Se quiser, posso te entregar um **projeto prático passo a passo** com:

* Dashboard com Streamlit
* POO aplicada a KPIs financeiros
* Banco de dados com SQLite ou Excel
* Uso de `decorators`, `functools`, `pandas` e `matplotlib`

---

### Deseja seguir para esse projeto prático?

Posso iniciar com a definição da estrutura, classes e funções, e evoluir com você!
