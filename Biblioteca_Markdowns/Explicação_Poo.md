<details>
<summary>🔹<h1> <strong> 📘 Módulo 1 – Funções em Python </strong></h1></summary>


<details>
<summary>🔹<h4> <strong>O que é uma função?</strong></h4></summary>

Uma função é um **bloco de código com um nome**, que você pode **chamar (executar)** sempre que quiser.  
Serve para **organizar o código**, **evitar repetição** e **facilitar a manutenção**.


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

</details>

<details>

<summary>🔹<h4> <strong> Base das Funções </strong></h4></summary>
    
<details>
<summary>🔹<h4> <strong> __Init e Self </strong></h4></summary>

<details>
<summary>🔹<h4> <strong> O que é Init e Self? </strong></h4></summary>
    
<details>
<summary>🔹<h4> <strong>🔧 `__init__` — Para que serve? </strong></h4></summary>

### ✅ **O que é:**

O `__init__` é um **método especial** das classes em Python. Ele é chamado **automaticamente toda vez que você cria um novo objeto** daquela classe.

### ✅ **Para que serve:**

* **Inicializar os dados do objeto**
* **Configurar o estado inicial** (atributos)
* É o **"construtor"** da classe (assim como em outras linguagens orientadas a objetos)

### 📌 Exemplo:

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
```

> Quando você faz:

```python
p1 = Pessoa("João", 30)
```

O Python **automaticamente chama**:

```python
Pessoa.__init__(p1, "João", 30)
```
</details>

<details>
<summary>🔹<h4> <strong> 👤 `self` — Para que serve? </strong></h4></summary>

### ✅ **O que é:**

O `self` representa a **instância atual** da classe — ou seja, **o próprio objeto** que está usando o método.

> É como dizer: “**esse objeto que estou usando agora**”.

### ✅ **Por que usar `self`?**

* Para **armazenar dados** dentro do objeto
* Para que **cada objeto tenha seus próprios dados**
* Para **acessar atributos e métodos** dentro da própria classe

### 📌 Exemplo:

```python
class Pessoa:
    def __init__(self, nome):
        self.nome = nome

    def falar(self):
        print(f"{self.nome} está falando.")
```

✔️ Aqui, `self.nome` **guarda o nome da pessoa dentro do próprio objeto**, e `falar()` acessa esse valor.
</details>
</details>

<details>
<summary>🔹<h4> <strong> 🤔 Por que preciso deles? </strong></h4></summary>

### 🔹 `__init__`: Porque você **quer que cada objeto comece com seus próprios valores.**

* Ex: um objeto `Cliente` começa com `nome`, `email`, `saldo`.
* Sem `__init__`, você teria que setar tudo **manualmente depois** da criação, o que não é prático.

### 🔹 `self`: Porque **você quer que cada objeto “lembre” de suas próprias informações**.

* Sem `self`, todos os objetos **compartilhariam os mesmos dados** — o que geralmente não é desejado.
</details>
<details>
<summary>🔹<h4> <strong>❓ Preciso sempre usar `__init__`? </strong></h4></summary>

**Não obrigatoriamente.**
Você só precisa do `__init__` **se quiser passar informações iniciais ao criar o objeto**.

### Exemplo sem `__init__`:

```python
class Animal:
    def emitir_som(self):
        print("Som!")
        
a = Animal()
a.emitir_som()
```

✔️ Isso funciona. Mas se você quiser que cada `Animal` tenha um nome diferente, aí você usaria `__init__`.

</details>


<details>
<summary>🔹<h4> <strong> ❓ Preciso sempre usar `self`? </strong></h4></summary>


**Sim, dentro de métodos comuns da classe.**

* O `self` é o **canal para acessar os dados do objeto**.
* Você **não precisa passá-lo na chamada** — o Python cuida disso internamente.

---
</details>

<details>
<summary>🔹<h4> <strong> ✅ Resumo final em forma de tabela </strong></h4></summary>

| Elemento   | O que é              | Para que serve                       | Obrigatório?                 |
| ---------- | -------------------- | ------------------------------------ | ---------------------------- |
| `__init__` | Construtor da classe | Inicializar dados da instância       | Não, mas muito útil          |
| `self`     | A instância atual    | Guardar e acessar os dados do objeto | Sim, em métodos de instância |

---
</details>

<details>
<summary>🔹<h4> <strong> 🧠 Analogia simples </strong></h4></summary>

> 💬 Pense que uma **classe** é uma **forma de bolo**, e um **objeto** é um **bolo real** feito com aquela forma.

* O `__init__` é o momento em que **você coloca os ingredientes e assa o bolo**.
* O `self` é o jeito que **cada bolo sabe seu sabor, tamanho, cobertura etc**.
* 
</details>

<details>
<summary>🔹<h4> <strong> 🧪 Exemplo real aplicado (finanças) </strong></h4></summary>

```python
class Transacao:
    def __init__(self, descricao, valor):
        self.descricao = descricao
        self.valor = valor

    def exibir(self):
        print(f"{self.descricao}: R${self.valor:.2f}")

t1 = Transacao("Compra de material", 150.75)
t2 = Transacao("Venda de produto", 300.00)

t1.exibir()  # Compra de material: R$150.75
t2.exibir()  # Venda de produto: R$300.00
```
</details>
</details>

<details> 
<summary>🔹<h4> <strong> 🧠 Args e Kwargs </strong></h4></summary>

<details> 
<summary>🔹<h4> <strong> ✅ O que são `*args` e `**kwargs`? </strong></h4></summary>

## `*args` (positional arguments - argumentos posicionais)

* Permite que **uma função receba vários argumentos em ordem**, sem saber antecipadamente quantos.
* Internamente, o Python transforma os argumentos em uma **tupla**.

## `**kwargs` (keyword arguments - argumentos nomeados)

* Permite que **uma função receba vários argumentos nomeados** (chave=valor).
* Internamente, o Python transforma os argumentos em um **dicionário**.


<summary>🔹<h4> <strong> 🧠 Estrutura interna </strong></h4></summary>

```python
def exemplo(a, *args, **kwargs):
    print("a:", a)
    print("args:", args)      # tupla
    print("kwargs:", kwargs)  # dicionário

exemplo(1, 2, 3, x=10, y=20)
```

### Saída:

```
a: 1
args: (2, 3)
kwargs: {'x': 10, 'y': 20}
```

* `a`: primeiro argumento obrigatório.
* `*args`: empacota 2 e 3 numa tupla.
* `**kwargs`: empacota x=10 e y=20 num dicionário.

---

# 🔄 Regras de ordem em funções

```python
def func(a, b=2, *args, c=3, **kwargs):
    pass
```

✅ Ordem recomendada:

```
parâmetros fixos ➜ padrão ➜ *args ➜ parâmetros com nome ➜ **kwargs
```
</details>
<details>
<summary>🔹<h4> <strong> 📦 Desempacotamento com `*` e `**` </strong></h4></summary>

Você também pode usar `*` e `**` para **desempacotar** valores em chamadas de funções.

### Exemplo com `*args`:

```python
valores = (4, 5)
def somar(a, b):
    return a + b

print(somar(*valores))  # Equivale a somar(4, 5)
```

### Exemplo com `**kwargs`:

```python
parametros = {"nome": "Ana", "idade": 28}
def exibir(nome, idade):
    print(f"{nome} tem {idade} anos")

exibir(**parametros)
```
</details>

<details>
<summary>🔹<h4> <strong> 💡 Aplicações reais </strong></h4></summary>

## 1. Função flexível em pipeline de análise de dados

```python
import pandas as pd

def carregar_dados(path, *args, **kwargs):
    return pd.read_csv(path, *args, **kwargs)

df = carregar_dados("vendas.csv", sep=";", encoding="utf-8", usecols=["produto", "valor"])
```

✔️ `*args` e `**kwargs` permitem passar qualquer parâmetro que o `read_csv()` aceite, tornando a função reutilizável.

---

## 2. Uso com classes

```python
class Produto:
    def __init__(self, nome, **kwargs):
        self.nome = nome
        self.preco = kwargs.get("preco", 0)
        self.estoque = kwargs.get("estoque", 0)

p = Produto("Notebook", preco=3500, estoque=5)
```

✔️ Permite adicionar **atributos extras** ao objeto sem alterar a assinatura do `__init__`.

---

## 3. Uso com decoradores

```python
def logar_execucao(func):
    def wrapper(*args, **kwargs):
        print(f"Executando: {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

@logar_execucao
def multiplicar(a, b):
    return a * b

print(multiplicar(4, 5))
```

✔️ Decoradores **precisam aceitar qualquer função**, por isso usam `*args` e `**kwargs` para capturar qualquer assinatura.

---

## 4. Somar qualquer número de valores

```python
def somar_tudo(*args):
    return sum(args)

print(somar_tudo(1, 2, 3, 4, 5))  # 15
```

✔️ Você não precisa saber a quantidade de números de antemão.

---

## 5. Combinar ambos:

```python
def exemplo_completo(msg, *args, nivel="INFO", **kwargs):
    print(f"[{nivel}] {msg}")
    print("Args:", args)
    print("Kwargs:", kwargs)

exemplo_completo("Processo iniciado", 1, 2, 3, user="admin", retry=True)
```
</details>
<details>
<summary>🔹<h4> <strong>  📊 Aplicação em finanças </strong></h4></summary>

```python
def calcular_lucro(receita, custos_fixos, *custos_variaveis, **ajustes):
    total_variavel = sum(custos_variaveis)
    total_ajustes = sum(ajustes.values())
    return receita - custos_fixos - total_variavel - total_ajustes

lucro = calcular_lucro(
    receita=10000,
    custos_fixos=2000,
    500, 600, 700,   # *custos_variaveis
    bonus=300, impostos=400  # **ajustes
)
```
</details>
<details>
<summary>🔹<h4> <strong> ✅ Resumo </strong></h4></summary>

| Item       | Explicação                                          |
| ---------- | --------------------------------------------------- |
| `*args`    | Recebe múltiplos valores posicionais como tupla     |
| `**kwargs` | Recebe múltiplos valores nomeados como dicionário   |
| Usado em   | Funções, métodos, decoradores, e chamadas dinâmicas |
| Ideal para | Criar funções genéricas e reutilizáveis             |
</details>
</details>
</details>

<details>
<summary>🔹<h4> <strong> Por que usar funções? </strong></h4></summary>

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
</details>

<details>
<summary>🔹<h4> <strong> Tipos de argumentos </strong></h4></summary>

<details>
<summary>🔹<h4> <strong> Argumentos </strong></h4></summary>
    
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

</details>
<details>
<summary>🔹<h4> <strong> Funções lambda (anônimas) </strong></h4></summary>

```python
imposto = lambda valor: valor * 0.15
print(imposto(1000))  # 150.0
```

Boa para usar dentro de `.apply()` no pandas.
</details>

<details>
<summary>🔹<h4> <strong> Funções em análise de dados </strong></h4></summary>

Exemplo: aplicar imposto a uma coluna de DataFrame:

```python
import pandas as pd

df = pd.DataFrame({'venda': [100, 200, 300]})

def aplicar_imposto(valor):
    return valor * 0.15

df['imposto'] = df['venda'].apply(aplicar_imposto)
print(df)
```
</details>
</details>
</details>
</details>
</details>
</details>
</details>
<details>
    
<summary>🔹<h1> <strong> 🎁 Módulo 2 – Decoradores em Python </strong></h1></summary>
    
<details>
<summary>🔹<h4> <strong>  🧠 O que é um decorador? </strong></h4></summary>

> **Decorador é uma função que recebe outra função como argumento, faz algo com ela e retorna uma nova função.**

Você pode pensar nele como um **"embrulho"** em volta de uma função. Ele **adiciona funcionalidades extras** *sem modificar o código da função original*.

---

## 🎨 Analogia simples

Imagine que você tem um **bolo (função original)**. Um decorador seria como **cobertura de chocolate**: você não muda o bolo, só **adiciona algo extra por fora**.

---

## 🧪 Exemplo básico

```python
def meu_decorador(func):
    def wrapper():
        print("Executando antes da função...")
        func()
        print("Executando depois da função...")
    return wrapper

@meu_decorador
def minha_funcao():
    print("Sou a função principal.")

minha_funcao()
```

### 🧾 Saída:

```
Executando antes da função...
Sou a função principal.
Executando depois da função...
```

🔍 O `@meu_decorador` **envolve** `minha_funcao()` com código antes e depois. Isso é o básico de um decorador.

---
</details>

<details>
<summary>🔹<h4> <strong> 🛠 Como funciona internamente? </strong></h4></summary>

```python
# Estas duas formas são equivalentes:
@meu_decorador
def ola():
    print("Oi")

# É o mesmo que fazer:
def ola():
    print("Oi")

ola = meu_decorador(ola)
```
</details>

<details>
<summary>🔹<h4> <strong> ✅ Aplicações úteis de decoradores </strong></h4></summary>

1. **Log de execução**
2. **Controle de tempo de execução**
3. **Validação de argumentos**
4. **Autenticação**
5. **Cache de resultados**
6. **Medição de performance**
7. **Rate-limiting (limitar número de chamadas)**

---

## 🧪 Exemplo com `functools.wraps`

Se você quiser manter o nome e docstring da função original:

```python
from functools import wraps

def logar_execucao(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print(f"Chamando {func.__name__} com args={args} kwargs={kwargs}")
        return func(*args, **kwargs)
    return wrapper

@logar_execucao
def soma(a, b):
    """Soma dois números"""
    return a + b

print(soma(2, 3))
```

</details>

<details>
<summary>🔹<h4> <strong>📦 Decoradores com argumentos </strong></h4></summary>

Você pode criar decoradores personalizados que aceitam parâmetros.

```python
def repetir(n):
    def decorador(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return wrapper
    return decorador

@repetir(3)
def dizer_ola():
    print("Olá!")

dizer_ola()
```

</details>

<details>
<summary>🔹<h4> <strong> 🤖 Decoradores com funções lambda (exemplo comum no pandas) </strong></h4></summary>

```python
import pandas as pd

def log_dataframe(func):
    def wrapper(*args, **kwargs):
        print("🔍 Aplicando transformação no DataFrame...")
        resultado = func(*args, **kwargs)
        print("✅ Transformação concluída.")
        return resultado
    return wrapper

@log_dataframe
def transformar(df):
    return df[df["valor"] > 10]

df = pd.DataFrame({"valor": [5, 20, 15]})
novo_df = transformar(df)
```

---

## 🧬 Decoradores com métodos de classes

```python
def checar_login(func):
    def wrapper(self, *args, **kwargs):
        if not self.logado:
            print("⚠️ Acesso negado. Faça login.")
            return
        return func(self, *args, **kwargs)
    return wrapper

class Sistema:
    def __init__(self):
        self.logado = False

    def login(self):
        self.logado = True

    @checar_login
    def acessar_dados(self):
        print("📊 Dados confidenciais exibidos.")

app = Sistema()
app.acessar_dados()  # Não permite
app.login()
app.acessar_dados()  # Agora permite
```
</details>


<details>

<summary>🔹<h4> <strong>🧠 Decoradores Prontos</strong></h4></summary>

<details>
<summary>🔹<h4> <strong> 🎯 O que são Decoradores Prontos? </strong></h4></summary>

Decoradores prontos são **funções especiais do próprio Python** (ou de bibliotecas padrão como `functools`) que modificam o comportamento de funções ou métodos de forma elegante, sem mudar o corpo da função diretamente.

Você aplica com `@decorador`, logo acima da função ou método.

</details>


<details>
<summary>🔹<h4> <strong>🧠 Diferença entre funções e métodos decorados</strong></h4></summary>

| Tipo             | Uso com `@decorador` | Primeiro parâmetro |
| ---------------- | -------------------- | ------------------ |
| Função           | Sim                  | Nenhum             |
| Método de classe | Sim                  | `self` ou `cls`    |

---
</details>

<details>
<summary>🔹<h4> <strong> 📚 Decoradores prontos do Python</strong></h4></summary>

| Decorador       | Uso                                   |
| --------------- | ------------------------------------- |
| `@staticmethod` | Cria método estático                  |
| `@classmethod`  | Cria método de classe                 |
| `@property`     | Transforma método em atributo         |
| `@lru_cache`    | Cache de resultados (functools)       |
| `@wraps`        | Preserva metadados da função original |

---

## 🧠 Comparativo rápido

| Decorador       | Quando usar                                               | Acesso a `self` ou `cls`?  |
| --------------- | --------------------------------------------------------- | -------------------------- |
| `@staticmethod` | Funções independentes dentro da classe                    | ❌ Não usa `self` nem `cls` |
| `@classmethod`  | Métodos que alteram ou usam a **classe**, não a instância | ✅ Usa `cls`                |
| `@property`     | Expor métodos como atributos calculados                   | ✅ Usa `self`               |
| `@lru_cache`    | Otimizar funções caras (recursivas, repetitivas)          | ❌ Função pura              |
| `@wraps`        | Preservar metadados ao criar decoradores customizados     | ✅ Usado **em decoradores** |
</details>

<details>
<summary>🔹<h4> <strong> ✅ Decoradores mais comuns e para que servem </strong></h4></summary>

<details>
<summary>🔹<h4> <strong> 1. `@staticmethod` </strong></h4></summary>

### 📌 O que faz:

Cria um método **que pertence à classe**, mas **não precisa acessar atributos da instância (`self`) nem da classe (`cls`)**.

### 📎 Quando usar:

Quando o método **não depende de nenhum dado interno** da instância nem da classe, mas **conceitualmente faz sentido estar dentro da classe**.

### 🧠 Exemplo:

```python
class Conversor:
    @staticmethod
    def km_para_milhas(km):
        return km * 0.621371

print(Conversor.km_para_milhas(10))  # 6.21371
```

---
</details>
<details>
<summary>🔹<h4> <strong> 2. `@classmethod` </strong></h4></summary>

### 📌 O que faz:

Cria um método que recebe **a classe como primeiro parâmetro** (em vez de `self`, usa `cls`).

### 📎 Quando usar:

Quando você quer **modificar atributos da classe**, criar **fábricas de objetos**, ou usar a **classe como contexto**.

### 🧠 Exemplo:

```python
class Produto:
    imposto = 0.1

    def __init__(self, preco):
        self.preco = preco

    @classmethod
    def mudar_imposto(cls, novo_valor):
        cls.imposto = novo_valor

Produto.mudar_imposto(0.2)
print(Produto.imposto)  # 0.2
```

</details>

<details>
<summary>🔹<h4> <strong> 3. `@property` </strong></h4></summary>


### 📌 O que faz:

Transforma um **método** em um **atributo acessável diretamente**, sem parênteses.

### 📎 Quando usar:

Quando você quer **expor atributos calculados** como se fossem propriedades simples, melhorando a legibilidade.

### 🧠 Exemplo:

```python
class Retangulo:
    def __init__(self, largura, altura):
        self.largura = largura
        self.altura = altura

    @property
    def area(self):
        return self.largura * self.altura

r = Retangulo(5, 10)
print(r.area)  # 50 — parece atributo, mas é calculado
```
</details>

<details>
<summary>🔹<h4> <strong> 4. `@lru_cache` (do módulo `functools`) </strong></h4></summary>

### 📌 O que faz:

Guarda os resultados de chamadas anteriores da função (cache), acelerando funções **puras** (sem efeitos colaterais) que são chamadas com frequência.

> LRU = **Least Recently Used**: remove os menos usados quando o cache enche.

### 📎 Quando usar:

Em funções **recursivas ou caras computacionalmente**, como cálculos matemáticos pesados.

### 🧠 Exemplo:

```python
from functools import lru_cache

@lru_cache(maxsize=1000)
def fib(n):
    if n <= 1:
        return n
    return fib(n - 1) + fib(n - 2)

print(fib(30))  # Muito mais rápido que sem cache
```
</details>

<details>
<summary>🔹<h4> <strong>  5. `@wraps` (do módulo `functools`) </strong></h4></summary>

### 📌 O que faz:

Usado **dentro de um decorador personalizado**, para **preservar os metadados da função original** (nome, docstring etc.)

> Sem ele, a função decorada perde sua identidade.

### 📎 Quando usar:

Sempre que você cria um decorador personalizado.

### 🧠 Exemplo:

```python
from functools import wraps

def meu_decorador(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print("Antes da função")
        resultado = func(*args, **kwargs)
        print("Depois da função")
        return resultado
    return wrapper

@meu_decorador
def saudacao():
    """Função que imprime uma saudação"""
    print("Olá!")

print(saudacao.__name__)     # saudacao
print(saudacao.__doc__)      # Função que imprime uma saudação
```

> Sem `@wraps`, o nome seria "wrapper" e a docstring seria `None`.
</details>
</details>

<details>
<summary>🔹<h4> <strong> 🧪 Exemplo com todos juntos </strong></h4></summary>

```python
from functools import lru_cache, wraps

class Exemplo:
    taxa = 1.1

    def __init__(self, valor):
        self.valor = valor

    @property
    def valor_com_taxa(self):
        return self.valor * Exemplo.taxa

    @classmethod
    def mudar_taxa(cls, nova):
        cls.taxa = nova

    @staticmethod
    def ajuda():
        return "Classe para aplicar taxa sobre valores"

@lru_cache
def calcular(n):
    if n < 2:
        return n
    return calcular(n-1) + calcular(n-2)
```

</details>
</details>

<details>
<summary>🔹<h4> <strong> 📊 Aplicação em análise de dados / finanças </strong></h4></summary>

### 🔄 Exemplo: Medir performance de uma função que processa DataFrame

```python
import time

def medir_tempo(func):
    def wrapper(*args, **kwargs):
        inicio = time.time()
        resultado = func(*args, **kwargs)
        fim = time.time()
        print(f"⏱ Tempo de execução: {fim - inicio:.4f} segundos")
        return resultado
    return wrapper

@medir_tempo
def simular_processamento(df):
    time.sleep(2)
    return df[df["lucro"] > 1000]

# Teste
import pandas as pd
df = pd.DataFrame({"lucro": [500, 2000, 1500]})
novo = simular_processamento(df)
```

</details>

<details>
<summary>🔹<h4> <strong>  ✅ Quando usar decoradores? </strong></h4></summary>

Use decoradores quando você quiser:

* **Reutilizar lógica comum** (log, validação, medição)
* **Separar responsabilidades** no código
* **Evitar repetição** com funções utilitárias

</details>  
</details>
</details>
</details>
<details>
    
<summary>🔹<h1> <strong> 🧱 Módulo 3 – Classes em Python </strong></h1></summary>

<details>
<summary>🔹<h4> <strong> 🧠 O que é uma classe? </strong></h4></summary>

<details>
<summary>🔹<h5> <strong> 🧠 Classe, explicação: </strong></h5></summary>
Uma classe é um molde para criar objetos.
Cada objeto tem atributos (dados) e métodos (comportamentos).

💬 Analogia:
*    A classe é a receita do bolo.

*    O objeto é o bolo feito a partir da receita.

*    Cada bolo pode ter recheio, tamanho e sabor diferentes (atributos), mas todos foram feitos pela mesma receita.
</details>
<details>
<summary>🔹<h5> <strong> 🧱 Estrutura de uma classe </strong></h5></summary>
```python
class NomeDaClasse:
    def __init__(self, parametros):
        self.atributo = valor

    def metodo(self):
        # ação
        pass
```

### 🔍 Partes da classe:

| Parte      | O que é                                                       |
| ---------- | ------------------------------------------------------------- |
| `class`    | Palavra-chave para criar uma classe                           |
| `__init__` | Método construtor, chamado quando um novo objeto é criado     |
| `self`     | Representa o próprio objeto (instância)                       |
| Atributos  | Variáveis ligadas ao objeto (`self.nome`, `self.preco`, etc.) |
| Métodos    | Funções dentro da classe, que usam ou modificam atributos     |

---
</details>
<details>
<strong><h5><summary>✅ Exemplo básico: Pessoa </strong></h5></summary>

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def apresentar(self):
        print(f"Olá, meu nome é {self.nome} e tenho {self.idade} anos.")

# Criando objetos
p1 = Pessoa("João", 30)
p2 = Pessoa("Ana", 25)

p1.apresentar()
p2.apresentar()
```

✔️ Cada `Pessoa` criada tem **seus próprios dados**, mas compartilha os mesmos **métodos**.

</details>

<details>
<summary>🔹<h5> <strong> Exemplo de classe que representa um produto: </strong></h5></summary>

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
</details>
</details>
<details>
    
<summary>🔹<h5> <strong> 🔁 Métodos da classe </strong></h5></summary>

<details>
<summary>🔹<h5> <strong> 🔁 Métodos </strong></h5></summary>

---

### 1. Método comum (usa `self`)

```python
def aumentar_idade(self):
    self.idade += 1
```

### 2. Método de classe (`@classmethod`, usa `cls`)

```python
@classmethod
def criar_bebe(cls, nome):
    return cls(nome, 0)
```

### 3. Método estático (`@staticmethod`, sem `self` ou `cls`)

```python
@staticmethod
def ano_atual():
    from datetime import datetime
    return datetime.now().year
```
---

</details>
</details>

<details>
<summary>🔹<h5> <strong> 🔐 Encapsulamento </strong></h5></summary>

---
    
### ➕ Atributos protegidos

```python
class Conta:
    def __init__(self, saldo):
        self.__saldo = saldo  # privado

    def ver_saldo(self):
        return self.__saldo
```

✔️ `__saldo` não pode ser acessado diretamente (proteção contra uso indevido).

---

# 👪 Herança

> Permite que uma classe **herde** atributos e métodos de outra classe.

```python
class Funcionario:
    def __init__(self, nome):
        self.nome = nome

    def trabalhar(self):
        print(f"{self.nome} está trabalhando...")

class Gerente(Funcionario):
    def aprovar(self):
        print(f"{self.nome} está aprovando relatórios.")
```

✔️ A classe `Gerente` pode **usar os métodos da classe `Funcionario`**, além de ter seus próprios.

---

# 🧬 Polimorfismo

> Permite que diferentes classes tenham **métodos com o mesmo nome**, mas **com comportamentos diferentes**.

```python
class Animal:
    def falar(self):
        print("Algum som...")

class Cachorro(Animal):
    def falar(self):
        print("Au au!")

class Gato(Animal):
    def falar(self):
        print("Miau!")

for a in [Cachorro(), Gato()]:
    a.falar()
```

---

# 📊 Exemplo real aplicado: Análise Financeira

```python
class CentroCusto:
    def __init__(self, nome, receita, custo):
        self.nome = nome
        self.receita = receita
        self.custo = custo

    def lucro(self):
        return self.receita - self.custo

    def margem(self):
        if self.receita == 0:
            return 0
        return self.lucro() / self.receita
```

### 🧪 Usando com dados:

```python
centros = [
    CentroCusto("TI", 10000, 7000),
    CentroCusto("RH", 8000, 4000)
]

for c in centros:
    print(f"{c.nome} | Lucro: {c.lucro()} | Margem: {c.margem():.2%}")
```

---
</details>

<details>
<summary>🔹<h5> <strong> Atributos vs Métodos </strong></h5></summary>

---

| Conceito | O que é                   | Exemplo                   |
| -------- | ------------------------- | ------------------------- |
| Atributo | Dado do objeto            | `self.nome`, `self.preco` |
| Método   | Função que atua no objeto | `.aplicar_desconto()`     |

---

</details>



<details>
<summary>🔹<h5> <strong> 📦 Resumo dos principais conceitos </strong></h5></summary>

---

| Conceito       | Explicação rápida                                      |
| -------------- | ------------------------------------------------------ |
| Classe         | Molde para criar objetos                               |
| Objeto         | Instância da classe, com atributos próprios            |
| `__init__`     | Inicializador chamado ao criar o objeto                |
| `self`         | Referência ao objeto atual                             |
| Atributo       | Dado associado ao objeto (`self.nome`)                 |
| Método         | Ação que o objeto pode realizar (`self.fazer()`)       |
| Encapsulamento | Esconde/Protege partes do objeto (`__privado`)         |
| Herança        | Uma classe herda de outra (`class A(B):`)              |
| Polimorfismo   | Métodos com o mesmo nome agem diferente em cada classe |
---
</details>

<details>
<summary>🔹<h5> <strong>  🧠 Quando usar classes? </strong></h5></summary>

Use classes quando:
---
* Seu projeto precisa representar **entidades complexas** (clientes, produtos, contas, relatórios).
* Você quer organizar código **por responsabilidade**.
* Deseja **reutilização, legibilidade e escalabilidade**.
* Está fazendo **análise orientada a dados ou objetos**.

---

</details>

<details>
<summary>🔹<h4> <strong> Classes em finanças </strong></h4></summary>

---

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

</details>
</details>


<details>    
<summary>🔹<h1> <strong> 🧭 Módulo 4 – Programação Orientada a Objetos (POO) </strong></h4></summary>
<details>
<summary>🔹<h4> <strong> 🧠 O que é Programação Orientada a Objetos? </strong></h4></summary>

A **Programação Orientada a Objetos (POO)** é um paradigma de programação que organiza o código em **"objetos"** — estruturas que **agrupam dados e comportamentos**.

> Em vez de pensar só em funções soltas e variáveis separadas, a POO permite representar entidades do mundo real como objetos que **guardam informações (atributos)** e **sabem o que fazer (métodos)**.

</details>

<details>
<summary>🔹<h4> <strong>🧱 Quais são os pilares da POO? </strong></h4></summary>

### 1. **Classe**

* É um **molde** ou **modelo** para criar objetos.
* Define os **atributos (dados)** e **métodos (funções)** que os objetos criados a partir dela terão.

### 2. **Objeto**

* É uma **instância de uma classe**.
* Cada objeto tem seus próprios valores e pode executar suas funções.

### 3. **Encapsulamento**

* Esconde os detalhes internos do funcionamento do objeto.
* Protege os dados, permitindo acesso controlado (por exemplo, com métodos `get` e `set`).

### 4. **Herança**

* Uma classe pode **herdar** características de outra.
* Permite **reutilização de código** e criação de estruturas mais flexíveis.

### 5. **Polimorfismo**

* Objetos diferentes podem **compartilhar o mesmo nome de método**, mas com **comportamentos diferentes**.
* Ex: um método `.calcular()` pode funcionar diferente em classes diferentes.

</details>

<details>
<summary>🔹<h4> <strong> 🧪 Exemplo simples de classe e objeto </strong></h4></summary>

```python
class ContaBancaria:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.saldo = saldo

    def depositar(self, valor):
        self.saldo += valor

    def sacar(self, valor):
        if valor <= self.saldo:
            self.saldo -= valor
        else:
            print("Saldo insuficiente!")

    def exibir_saldo(self):
        print(f"Saldo de {self.titular}: R${self.saldo:.2f}")

# Criando um objeto (instância)
conta = ContaBancaria("Ana", 1000)
conta.depositar(500)
conta.sacar(200)
conta.exibir_saldo()  # Saldo de Ana: R$1300.00
```
</details>
<details>
<summary>🔹<h4> <strong> 🔐 Encapsulamento (com controle de acesso) </strong></h4></summary>

```python
class Produto:
    def __init__(self, nome, preco):
        self.nome = nome
        self.__preco = preco  # atributo privado

    def get_preco(self):
        return self.__preco

    def set_preco(self, novo_preco):
        if novo_preco >= 0:
            self.__preco = novo_preco
        else:
            print("Preço inválido!")

produto = Produto("Notebook", 3500)
print(produto.get_preco())  # 3500
produto.set_preco(-1000)    # Preço inválido!
```
</details>

<details>
<summary>🔹<h4> <strong> 🧬 Herança e polimorfismo </strong></h4></summary>

```python
class Funcionario:
    def __init__(self, nome):
        self.nome = nome

    def calcular_bonus(self):
        return 1000

class Gerente(Funcionario):
    def calcular_bonus(self):
        return 3000

class Vendedor(Funcionario):
    def calcular_bonus(self):
        return 2000

funcionarios = [Gerente("Carlos"), Vendedor("João")]

for f in funcionarios:
    print(f"{f.nome}: bônus de R${f.calcular_bonus()}")
```
</details>
<details>
<summary>🔹<h4> <strong>  📊 Exemplo aplicado à Análise de Dados / Finanças </strong></h4></summary>

Imagine que você trabalha com **controle de investimentos**.

### Criando uma estrutura orientada a objetos para ativos financeiros:

```python
class AtivoFinanceiro:
    def __init__(self, nome, tipo, valor_investido):
        self.nome = nome
        self.tipo = tipo
        self.valor_investido = valor_investido

    def calcular_retorno(self):
        raise NotImplementedError("Subclasse deve implementar este método.")

class Acoes(AtivoFinanceiro):
    def __init__(self, nome, valor_investido, cotacao_atual, cotacao_compra):
        super().__init__(nome, "Ação", valor_investido)
        self.cotacao_atual = cotacao_atual
        self.cotacao_compra = cotacao_compra

    def calcular_retorno(self):
        return (self.cotacao_atual - self.cotacao_compra) / self.cotacao_compra

class RendaFixa(AtivoFinanceiro):
    def __init__(self, nome, valor_investido, taxa_juros, tempo):
        super().__init__(nome, "Renda Fixa", valor_investido)
        self.taxa_juros = taxa_juros
        self.tempo = tempo

    def calcular_retorno(self):
        return self.valor_investido * (1 + self.taxa_juros) ** self.tempo - self.valor_investido

# Exemplo de uso
ativos = [
    Acoes("PETR4", 1000, cotacao_atual=32.00, cotacao_compra=25.00),
    RendaFixa("CDB Banco X", 5000, taxa_juros=0.12, tempo=2)
]

for ativo in ativos:
    print(f"{ativo.nome} ({ativo.tipo}): retorno = R${ativo.calcular_retorno():.2f}")
```
</details>
<details>
<summary>🔹<h4> <strong> 🧠 Por que usar POO na análise de dados? </strong></h4></summary>

1. **Organização do código**: agrupa dados e operações relacionadas em um só lugar.
2. **Reusabilidade**: você pode reaproveitar suas classes com outros dados.
3. **Escalabilidade**: facilita a manutenção e expansão do sistema.
4. **Modelagem de domínios**: você pode modelar **clientes, contratos, contas, fretes, produtos, relatórios** como objetos.

<details>
<summary>🔹<h4> <strong>  Pilares da POO </strong></h4></summary>

| Pilar              | Explicação                                   | Exemplo                           |
| ------------------ | -------------------------------------------- | --------------------------------- |
| **Abstração**      | Esconder complexidade                        | `.resumo()` sem saber os detalhes |
| **Encapsulamento** | Ocultar atributos internos                   | `self.__custo`                    |
| **Herança**        | Uma classe herda outra                       | `class Analista(Funcionario)`     |
| **Polimorfismo**   | Métodos com o mesmo nome funcionam diferente | `.calcular()` em várias classes   |
</details>

<details>
<summary>🔹<h4> <strong>  Exemplo real – Lucro por Centro de Custo com POO </strong></h4></summary>

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
</details>
</details>
</details>
</details>
</details>
</details>
</details>
</details>
