
# Decoradores

Decoradores são um elemento significante do Python, também são conhecidos como meta-programação, para simplificarmos sua ideia, podemos dizer que eles são funções que modificam a funcionalidade de uma outra função, eles nos ajudam a deixar o código menor e mais Pythônico (legível ao modo Python). O conceito de decoradores pode ser inicialmente um pouco difícil de capturarmos, mas vamos por partes.

Antes de compreendermos os decoradores, é interessante que entendamos como as funções funcionam. Lembre que uma função retorna um valor baseado nos argumentos fornecidos a ela. Vejamos um simples exemplo:

```python
def saudar(nome='Gabriel'):
    return f'Saudações, {nome}!'
````

Podemos agora chamar essa função sem um argumento (pois já existe um argumento padrão nela), ou com um argumento:

```python
saudar() # 'Saudações, Gabriel!'
saudar('Rafael') # 'Saudações, Rafael!'
```

Em geral, as funções em Python também podem ter efeitos colaterais, em vez de apenas transformar um input em um output. A função print() é um exemplo básico disso: ela retorna None enquanto tem o efeito colateral de enviar algo para o console. Porém, para entender os decoradores, basta pensar nas funções como algo que transforma determinados argumentos em um valor.

Também podemos atribuir uma função a uma variável, para isso, não usamos parenteses, dessa maneira estamos guardando apenas a referência ao objeto função.

```python
saudacao = saudar
print(saudacao) # <function saudar at 0x7f7ab6fca290>
saudacao('Miguel') # 'Saudações, Miguel!'
```

Podemos por exemplo deletar a referência em memória da antiga função:

```python
del saudar
saudar() # NameError: name 'saudar' is not defined
```

Veja que se tentarmos invocá-la írá ocorrer um NameError, mas veja que ainda podemos chamar a outra referência que temos:

```python
saudacao() # 'Saudações, Gabriel!'
```

Veja que mesmo deletando a função antiga, ainda conseguimos executar a função saudacao()!

## Funções dentro de Funções

Em Python, funções são first-class objects. Isso significa que as funções podem ser transmitidas e usadas como argumentos, assim como qualquer outro objeto (string, int, float, listas e assim por diante).

Vamos começar definindo uma simples função:

```python
def func(string):
    def wrapper():
        print("Iniciada")
        print(string)
        print("Finalizada")
    return wrapper()
```

Observe que temos uma função de nome func() que recebe uma string como argumento e dentro dela temos uma função de nome wrapper() que não recebe nenhum argumento e imprime "Iniciada", a string passada para a função func() e "Finalizada" e finalmente retorna a função wrapper() (ela mesma) invocando-a. Podemos usá-la da seguinte forma:

```python
f = func("Hello World")
# Iniciada
# Hello World
# Finalizada
```

Vamos agora modificá-la para que a função wrapper() não retorne a ela mesmo invocando-a, mas dessa vez apenas o objeto função.

```python
def func(string):
    def wrapper():
        print("Iniciada")
        print(string)
        print("Finalizada")
    return wrapper
```

Dessa vez para usá-la temos de usar o seguinte procedimento:

```python
f = func("Hello World")
print(f) # <function func.<locals>.wrapper at 0x7f7ab6fca0e0>
f()
# Iniciada
# Hello World
# Finalizada
```

Também existe a opção de chamá-la da seguinte forma:

```python
func("Hello World")()
# Iniciada
# Hello World
# Finalizada
```

Até então tudo bem, nada que venha a nos surpreender. Mas e se desejarmos passar uma outra função como argumento para func()? Vamos definir duas novas funções para testarmos:

```python
def func(f):
    def wrapper():
        print("Iniciada")
        f()
        print("Finalizada")
    return wrapper

def f1():
    print("Função f1() chamada!")

def f2():
    print("Função f2() chamada")
```

Observe que modificamos a função wrapper() e agora ela está invocando a função f() (esta que passaremos como argumento). Vamos agora chamar a função func() passando as funções f1() e f2() como argumento:

```python
f1 = func(f1)
f2 = func(f2)
print(f1) # <function func.<locals>.wrapper at 0x7f7ab702ab90>
print(f2) # <function func.<locals>.wrapper at 0x7f7ab702a950>
f1() 
# Iniciada
# Função f1() chamada!
# Finalizada
f2() 
# Iniciada
# Função f2() chamada
# Finalizada
```

Basicamente este é o conceito de decoradores, estamos usando a função func() para alterar o comportamento das funções f1() e f2(), porém existe uma maneira mais interessante de definí-los, em outras palavras, mais Pythônica.

## Decorando Funções

Vamos decorar as funções f1() e f2() usando a sintaxe `@`:

```python
@func
def f1():
    print("Função f1() chamada!")

@func
def f2():
    print("Função f2() chamada")
```

Dessa vez podemos chamá-las diretamente e teremos o mesmo efeito anterior:

```python
f1()
# Iniciada
# Função f1() chamada!
# Finalizada
f2()
# Iniciada
# Função f2() chamada
# Finalizada
```

Faremos agora outra modificação, dessa vez as funções wrapper() e f1() passam a receber um argumento e a função passada como argumento para func() passa a ser invocada com esse argumento:

```python
def func(f):
    def wrapper(x):
        print("Iniciada")
        f(x)
        print("Finalizada")
    return wrapper

@func
def f1(x):
    print(f"O valor de x é = {x}")

@func
def f2():
    print("Função f2() chamada")
```

Vejamos agora o que ocorre se invocarmos as funções f1() e f2():

```python
f1(7)
# Iniciada
# O valor de x é = 7
# Finalizada
f2() # TypeError: wrapper() missing 1 required positional argument: 'x'
```

f1() é chamada e nos imprime o valor como esperado, porém f2() "quebra", não somo capazes de chamá-la, pois a função wrapper() espera um argumento. Para solucionar este problema podemos usar o conceito de \*args e \*\*kwargs, vamos então masi uma vez modificar nossas funções:

```python
def func(f):
    def wrapper(*args, **kwargs):
        print("Iniciada")
        f(*args, **kwargs)
        print("Finalizada")
    return wrapper

@func
def f1(x):
    print(f"O valor de x é = {x}")

@func
def f2():
    print("Função f2() chamada")
```

```python
f1(7)
# Iniciada
# O valor de x é = 7
# Finalizada
f2()
# Iniciada
# Função f2() chamada
# Finalizada
```

Para finalizarmos, vamos modificar nossas funções wrapper() e f1() para retornar um valor:

```python
def func(f):
    def wrapper(*args, **kwargs):
        print("Iniciada")
        valor_retorno = f(*args, **kwargs)
        print("Finalizada")
        return valor_retorno
    return wrapper

@func
def f1(x, y):
    print(f"O valor de x é = {x}")
    print(f"O valor de y é = {y}")
    return y + x

f1 = f1(5,33)
# Iniciada
# O valor de x é = 5
# O valor de y é = 33
# Finalizada
print(f1) # 38
```

## Outros Exemplos

Funções e métodos são chamados callable se for possível chamá-los. De fato, qualquer objeto que implemente o método especial **call**() é um callable, então um decorador seria um callable que retorna um callable.

Então como já tinhamos dito na nossa introdução, um decorador recebe um função, adiciona alguma funcionalidade a ela e a retorna:

```python
def embelezar(func):
    def interno():
        print("Fui decorado")
        func()
    return interno

def normal():
    print("Eu sou normal")

normal() # Eu sou normal

bonito = embelezar(normal)
bonito() 
# Fui decorado
# Eu sou normal
```

Veja que a função normal() foi decorada e demos o nome à função retornada, que se chamou bonito. Uma forma mais eficaz de usarmos os decoradores é usando o símbolo @ junto do nome da função decoradora e colocar ele em cima da definição da função a ser decorada. Por exemplo:

```python
@embelezar
def normal
```


():
print("Eu sou normal também")

normal()

# Fui decorado

# Eu sou normal também

````

## Decorando Funções com Parâmetros
O último decorador que escrevemos foi bastante simples, só funcionava com funções sem parâmatros, apenas para ilustrarmos o conceito, mas e se tivermos funções que operam com parâmetros?

```python
def divisao(x, y):
    return x / y
````

A função recebe dois parâmetros x e y, sabemos que se passarmos 0 para y ocorrerá um erro.

```python
print(divisao(10,2)) # 5.0
print(divisao(3,0)) # ZeroDivisionError: division by zero
```

Agora vamos fazer um decorador para resolvermos esse problema.

```python
def divisao_inteligente(func):
    def interior(x,y):
        print("Será feita uma divisão de {0} por {1}".format(x,y))
        if y == 0:
            print("Impossível dividir")
            return
        return func(x,y)
    return interior

@divisao_inteligente
def divisao(x,y):
    return x / y        
```

```python
divisao(3,3)
# Será feita uma divisão de 3 por 3
# 1.0

divisao(3,0)
# Será feita uma divisão de 3 por 0
# Impossível dividir
```

## Medindo Desempenho

Podemos criar um decorar que é capaz de medir quanto tempo uma função leva para rodar:

```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        inicio = time.time()
        valor_retorno = func()
        total = time.time() - inicio
        print(f"Tempo: {total}")
        return valor_retorno
    return wrapper
```

Vamos definir duas funções para medí-las:

```python
@timer
def t1():
    for _ in range(10_000_000):
        pass

@timer
def t2():
    time.sleep(2.3)
```

Finalmente, vamos obter o tempo de cada uma:

```python
t1() # Tempo: 0.36320018768310547
t2() # Tempo: 2.302194118499756
```
