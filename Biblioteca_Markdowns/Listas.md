<details>
<summary>🔹<h1> <strong> Listas </strong></h1></summary>

Listas são uma das estruturas de dados mais comumente usadas em Python, e elas nos permitem armazenar uma coleção de itens em uma única variável.

<details>
<summary>🔹<h2> <strong> Criando uma lista </strong></h2></summary>

Para criar uma lista em Python, usamos colchetes e separamos os itens com vírgulas. Por exemplo:

```python
frutas = ['maçã', 'banana', 'laranja']

```
</details>


<details>
<summary>🔹<h2> <strong> Acessando itens da lista </strong></h2></summary>

Podemos acessar itens individuais em uma lista usando seu índice. O primeiro item em uma lista tem um índice de 0, o segundo item tem um índice de 1 e assim por diante. Por exemplo:

```python
frutas = ['maçã', 'banana', 'laranja']
print(frutas[0])  # Saída: 'maçã'
print(frutas[1])  # Saída: 'banana'
print(frutas[2])  # Saída: 'laranja'

```

Também podemos acessar itens do final da lista usando índices negativos. O último item em uma lista tem um índice de -1, o penúltimo item tem um índice de -2 e assim por diante. Por exemplo:

```python
frutas = ['maçã', 'banana', 'laranja']
print(frutas[-1])  # Saída: 'laranja'
print(frutas[-2])  # Saída: 'banana'
print(frutas[-3])  # Saída: 'maçã'
```
</details>

<details>
<summary>🔹<h2> <strong> Fatiando listas </strong></h2></summary>

Também podemos extrair um subconjunto de uma lista usando o fatiamento. O fatiamento cria uma nova lista que contém apenas os elementos especificados da lista original. A sintaxe básica para fatiar uma lista é a seguinte:

```python
nova_lista = lista[início:fim]

```

onde o `início` é o índice do primeiro item a incluir no fatiamento e o `fim` é o índice do primeiro item a excluir do fatiamento.
Por exemplo:

```python
numeros = [1, 2, 3, 4, 5]
print(numeros[1:4])  # Saída: [2, 3, 4]

```
</details>

<details>
<summary>🔹<h2> <strong> Modificando itens da lista </strong></h2></summary>

Podemos modificar itens individuais em uma lista usando seu índice. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas[1] = 'uva'
print(frutas)  # Saída: ['maçã', 'uva', 'laranja']

```
</details>


<details>
<summary>🔹<h2> <strong> Adicionando itens a uma lista </strong></h2></summary>

Podemos adicionar itens ao final de uma lista usando o método `append()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.append('pera')
print(frutas)  # Saída: ['maçã', 'banana', 'laranja', 'pera']

```

Também podemos inserir itens em uma posição específica da lista usando o método `insert()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.insert(1, 'pera')
print(frutas)  # Saída: ['maçã', 'pera', 'banana', 'laranja']

```
</details>


<details>
<summary>🔹<h2> <strong>  Removendo itens de uma lista </strong></h2></summary>

Podemos remover itens de uma lista usando o método `remove()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.remove('banana')
print(frutas)  # Saída: ['maçã', 'laranja']

```

Também podemos remover itens do final de uma lista usando o método `pop()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.pop()
print(frutas)  # Saída: ['maçã', 'banana']

```
</details>

<details>
<summary>🔹<h2> <strong> Compreensões de lista </strong></h2></summary>

As compreensões de lista são uma maneira concisa de criar novas listas executando alguma operação em cada item em uma lista existente. A sintaxe básica para uma compreensão de lista é a seguinte:

```
nova_lista = [expressão for item in lista if condição]

```

Por exemplo:

```
numeros = [1, 2, 3, 4, 5]
pares = [x for x in numeros if x % 2 == 0]
print(pares)  # Saída: [2, 4]

```

Podemos adicionar itens ao final de uma lista usando o método `append()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.append('pera')
print(frutas)  # Saída: ['maçã', 'banana', 'laranja', 'pera']

```

Também podemos inserir itens em uma posição específica da lista usando o método `insert()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas.insert(1, 'pera')
print(frutas)  # Saída: ['maçã', 'pera', 'banana', 'laranja']

```
</details>


<details>
<summary>🔹<h2> <strong> Compreensões de lista </strong></h2></summary>

As compreensões de lista são uma maneira concisa de criar novas listas executando alguma operação em cada item em uma lista existente. A sintaxe básica para uma compreensão de lista é a seguinte:

```
nova_lista = [expressão for item in lista if condição]

```

Por exemplo:

```
numeros = [1, 2, 3, 4, 5]
pares = [x for x in numeros if x % 2 == 0]
print(pares)  # Saída: [2, 4]

```

Abaixo estão alguns exemplos de list comprehension em Python:

Exemplo 1:

```
# Criar uma lista de números pares de 0 a 10
pares = [x for x in range(11) if x % 2 == 0]
print(pares)

```

Output:

```
[0, 2, 4, 6, 8, 10]

```

Exemplo 2:

```
# Criar uma lista de números ímpares de 0 a 10
impares = [x for x in range(11) if x % 2 == 1]
print(impares)

```

Output:

```
[1, 3, 5, 7, 9]

```

Exemplo 3:

```
# Criar uma lista de números quadrados de 0 a 10
quadrados = [x**2 for x in range(11)]
print(quadrados)

```

Output:

```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

```

Exemplo 4:

```
# Criar uma lista de letras maiúsculas a partir de uma lista de strings
palavras = ['banana', 'maçã', 'laranja']
maiusculas = [letra.upper() for palavra in palavras for letra in palavra]
print(maiusculas)

```

Output:

```
['B', 'A', 'N', 'A', 'N', 'A', 'M', 'A', 'Ç', 'Ã', 'L', 'A', 'R', 'A', 'N', 'J', 'A']

```

Exemplo 5:

```
# Criar uma lista de elementos únicos a partir de uma lista com elementos repetidos
repetidos = [1, 2, 3, 4, 3, 2, 1]
unicos = list(set(repetidos))
print(unicos)

```

Output:

```
[1, 2, 3, 4]

```
</details>

<details>
<summary>🔹<h2> <strong> Validar Lista </strong></h2></summary>

Podemos validar se um ou mais itens estão presentes em uma lista em Python de diversas formas, algumas delas incluem:

- Utilizar um loop for para iterar sobre a lista e verificar se cada item está presente utilizando a cláusula `in`

```
minha_lista = ['item1', 'item2', 'item3']
for item in minha_lista:
    if item == 'item1':
        print('O item1 está presente na lista!')

```

A função `any()` retorna True se pelo menos um dos elementos na lista passada como argumento for True. Caso contrário, retorna False. No exemplo mencionado, a função `any()` é usada em conjunto com uma lista de condições para verificar se pelo menos um item está presente em outra lista. Se pelo menos um item estiver presente, a condição retorna True e a mensagem "Pelo menos um dos itens está presente na lista!" é impressa. Caso contrário, a condição retorna False e a mensagem não é impressa.

```
minha_lista = ['item1', 'item2', 'item3']
if any(item in minha_lista for item in ['item1', 'item4']):
    print('Pelo menos um dos itens está presente na lista!')

```

A função `set()` é uma das funções integradas do Python que cria um conjunto, que é uma coleção de elementos únicos. Em outras palavras, um conjunto é uma coleção não ordenada de objetos exclusivos. Podemos criar um conjunto a partir de uma lista ou de qualquer outra sequência usando a função `set()`. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja', 'maçã']
conjunto_frutas = set(frutas)
print(conjunto_frutas)  # Saída: {'banana', 'laranja', 'maçã'}

```

Observe que o conjunto resultante contém apenas uma ocorrência de cada elemento da lista original. Além disso, os elementos do conjunto são exibidos em uma ordem não definida.

Podemos usar conjuntos para executar operações de conjunto, como união, interseção e diferença. Por exemplo:

```
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
uniao = A.union(B)
print(uniao)  # Saída: {1, 2, 3, 4, 5, 6}
intersecao = A.intersection(B)
print(intersecao)  # Saída: {3, 4}
diferenca = A.difference(B)
print(diferenca)  # Saída: {1, 2}

```

Na primeira linha, criamos dois conjuntos A e B. Em seguida, usamos o método `union()` para criar um novo conjunto que contém todos os elementos de A e B. Na terceira linha, usamos o método `intersection()` para criar um novo conjunto que contém apenas os elementos que estão em ambos A e B. Na quinta linha, usamos o método `difference()` para criar um novo conjunto que contém apenas os elementos que estão em A, mas não em B.

Os conjuntos são uma estrutura de dados poderosa e flexível em Python, e podem ser usados em uma variedade de contextos, incluindo filtragem de dados, remoção de duplicatas e cálculo de estatísticas.

- Utilizar a função `set()` para transformar a lista em um conjunto, e então verificar se a interseção entre o conjunto de itens que queremos encontrar e o conjunto da lista original é maior que zero

```
minha_lista = ['item1', 'item2', 'item3']
itens_procurados = set(['item1', 'item4'])
if len(set(minha_lista) & itens_procurados) > 0:
    print('Pelo menos um dos itens está presente na lista!')

```

Essas são apenas algumas das formas de validar se um ou mais itens estão presentes em uma lista em Python.

</details>
</details>
