# Escolinha  🫕

# **Python**

## **Básico**

### **Listas**

# Lists in Python

Listas são uma das estruturas de dados mais comumente usadas em Python, e elas nos permitem armazenar uma coleção de itens em uma única variável.

## Criando uma lista

Para criar uma lista em Python, usamos colchetes e separamos os itens com vírgulas. Por exemplo:

```python
frutas = ['maçã', 'banana', 'laranja']

```

## Acessando itens da lista

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

## Fatiando listas

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

## Modificando itens da lista

Podemos modificar itens individuais em uma lista usando seu índice. Por exemplo:

```
frutas = ['maçã', 'banana', 'laranja']
frutas[1] = 'uva'
print(frutas)  # Saída: ['maçã', 'uva', 'laranja']

```

## Adicionando itens a uma lista

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

## Removendo itens de uma lista

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

## Compreensões de lista

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

## Compreensões de lista

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

### **Dicionário**

## Dicionários em Python

Dicionários são uma estrutura de dados em Python que permite armazenar valores associados a chaves. Em outras palavras, é como se fosse uma lista de pares chave-valor. A sintaxe para criar um dicionário é a seguinte:

```
meu_dict = {"chave1": "valor1", "chave2": "valor2", "chave3": "valor3"}

```

As chaves são strings ou números, e os valores podem ser qualquer tipo de dado em Python, incluindo outros dicionários. Por exemplo:

```
meu_dict = {"nome": "João", "idade": 25, "telefones": {"celular": "1234-5678", "residencial": "4321-8765"}}

```

Podemos acessar os valores do dicionário através das suas chaves. Por exemplo:

```
print(meu_dict["nome"])
# Saída: João

print(meu_dict["telefones"]["celular"])
# Saída: 1234-5678

```

Também podemos adicionar, modificar e remover itens do dicionário. Para adicionar um novo item, basta criar uma nova chave e atribuir um valor a ela:

```
meu_dict["email"] = "joao@email.com"

```

Para modificar um item existente, basta atribuir um novo valor à chave correspondente:

```
meu_dict["idade"] = 26

```

Para remover um item, podemos usar o método `pop()`:

```
meu_dict.pop("telefones")

```

Por fim, podemos percorrer um dicionário usando o loop `for`. Por exemplo:

```
for chave, valor in meu_dict.items():
    print(chave + ": " + str(valor))

```

A saída seria:

```
nome: João
idade: 26
email: joao@email.com
```

## **Pandas**

### **Iniciando**

Pandas é a biblioteca focada em BANCO DE DADOS. Sua sintaxe básica é a seguinte:

```python
import pandas as pd
```

Lembrando que o pd ali escrito, pode ser qualquer outra coisa, mas sempre que uma sintaxe dando call em algo do pandas for escrito, precisará fazer essa alteração 

Exemplo:

```python
import pandas as pandas
```

```python
import pandas as pan
```

O mais comum é usar pd como no primeiro exemplo 

### **Criando dados do zero:**

Para fazer isso, podemos usar a seguinte linha:

```python
pd.DataFrame({'Yes':[50,21],'No':[131,2]})
```

Output:

|  | Yes | No |
| --- | --- | --- |
| 0 | 50 | 131 |
| 1 | 21 | 2 |

```python
Abreviaçãodadaaopacote.DataFrame({'nome da coluna 1':[conteúdo coluna 1],'nome coluna 2':[conteúdo coluna 2]})
```

Porém, podemos ver uma certa peculiaridade que quero apontar:

A contagem começa a partir da linha zero, uma diferença considerável do Excel que começa na linha 1, o que em certos momentos de selecionar x números de linhas pode induzir a erro, então é importante atenção nesse detalhe

As colunas no código criado tem nome, as linhas não mas isso pode ser mudado:

```python
pd.DataFrame({'Yes':[50,21],'No':[131,2]},index='oferta A','oferta B')
```

Output:

|  | Yes | No |
| --- | --- | --- |
| Oferta A | 50 | 131 |
| Oferta B | 21 | 2 |

Basicamente, a sintaxe é a seguinte:

```python
abreviaçãodonomedopacote.DataFrame({'nome coluna 1':[conteudos coluna 1],'nome coluna 2':[conteúdos coluna 2]},index='nome linha 1')
```

### **Ler arquivos**

O mais interessante dessa pacote é a forma de tratar os dados, o Pandas consegue buscar esses arquivos. É bom lembrar que o Python vai buscar os dados, ou seja, não quer dizer que não vá puxar tabelas dinâmicas ou gráficos, mas ele vira em um formato ilegível, por isso é importante tentar buscar planilhas apenas com os dados

Bom, como podemos ler os arquivos no Python com o Pandas? E para visualizar esse arquivo?

Bom, aí temos a ideia mais básica do Python:

Salvar dados em variáveis e visualizar, nos dois exemplos acima vemos que o arquivo Excel está dentro de uma variável “df”

```python
import pandas as pd
variavel = abreviaçãodonomedopacote.read_formato (r'caminho para o arquivo\nome do arquivo.formato excel')
print(df)
```

Um exemplo:

```python
import pandas as pd
df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx')
print(df)
```

Ao tentar rodar, é possível que aconteça um erro:

ImportError: Missing optional dependency ‘xlrd’

Nesse caso, é preciso instalar um pacote a mais:

```python
pip install openpyxl
```

Nao se preocupe, voltaremos nesse pacote mais tarde, ele será relevante para outras funcionalidades.

### **Selecionar planilhas dentro de um arquivo, colunas,filtros e substituição de dados**

Aqui é onde as coisas começam a ficar interessantes, o Pandas é uma ótima ferramenta para automação, até mais que o VBA, podendo ser mais rápido e mais preciso para TRABALHAR DADOS

Sabemos que não vivemos em um mundo ideal e perfeito em que simplesmente vão enviar\produzir um Excel que não tenha algum tipo de planilha dentro dele além da que precisamos, a planilha com banco de dados necessários, uma com tabelas dinâmicas, outra com gráficos e por aí vai, ou seja, com mais de uma aba!!!

Aqui vou apresentar duas formas de fazer essa “seleção” da(s) abas que estamos buscando, pelo nome da planilha e pelo número que ela representa dentro dela:

```python
df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2'))

#ou

df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name=2))

#ou

df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name=None))
```

O que está ocorrendo nos exemplos acima?

Basicamente o mesmo que no capítulo anterior “Ler arquivos”,mas, com uma diferença fundamental, está selecionando qual aba da planilha está “puxando”

A única exceção é a terceira linha do exemplo acima, nela, ele vai puxar todas as abas mas não necessariamente elas estarão utilizáveis 

```python
variavel = abreviaçãodonomedopacote.read_formato (r'caminho para o arquivo\nome do arquivo.formato excel',sheet_name=nome da aba ou número índice correspondente))
print(df)
```

Lembrando que: se puxar por número, a contagem começa por 0, então o python vai identificar a primeira aba como zero, a segunda como 1, a terceira como 2 e por aí vai.

Da mesma forma que conseguimos selecionar as abas, podemos selecionar as colunas que desejamos, é interessante pois a partir daqui, conseguimos diminuir o uso de memória do computador, são os primeiros passos da análise de dados.

A linha de raciocínio não mudou, o código continua praticamente o mesmo, com a diferença que passaremos a selecionar as colunas.

```python
df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2', usecol=[3,4))

#ou

df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2', usecol=[3,4:7))

#ou

df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2', usecol="Coluna 3, Coluna 4"))

#ou

df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2', usecol="Coluna 3, Coluna 4:Coluna 7"))
```

Bom, o que mostram os exemplos acima?

As duas primeiras linhas estão selecionando, na “Aba 2”, certas colunas específicas baseadas em seus números de colunas. No primeiro caso, as colunas 3 e 4 (lembrando que a contagem no python começa no zero, na prática são as colunas 4 e 5), enquanto o segundo caso seleciona as colunas 3 e as do intervalo de 4 a 7 ( novamente reafirmo, a contagem no python começa no zero, ou seja, está selecionando na prática as colunas 4 e as que estiverem no intervalo das colunas 5 a 8).

A lógica é como essa abaixo:

| Coluna\linha Python | Coluna\linha Excel |
| --- | --- |
| 0 | 1 |
| 1 | 2 |
| 2 | 3 |
| 3 | 4 |

E a sintaxe é a seguinte:

```python
variavel = abreviaçãodonomedopacote.read_formato (r'caminho para o arquivo\nome do arquivo.formato excel',sheet_name=nome da aba ou número índice correspondente, usecol= nome ou números das colunas)
```

Algo legal, nesse mesmo formato que podemos usar é a função nrows, nela selecionamos um x números de linhas para pularmos. Pode ser interessante usar em database que se começa fora da primeira linha.

Nesse exemplo, estamos dizendo o seguinte ao python:

Variável df, acesse o caminho “C:user\Lucas\downloads\file\” e abra o receba as colunas 3 e 4 da Aba 2, mas, pule as 11 primeiras linhas. Ou seja, apenas a partir da 12ª linha.

Lembrando que a contagem no python começa na linha zero

Para finalizar esse capítulo, vamos tratar filtros:

```python
df = pd.read_excel (r'C:user\Lucas\downloads\file\File name.xlsx',sheet_name='Aba 2', usecol=[3,4),nrows=11)
```

Por fim, filtragem!

Fazer filtros com os databases é uma das formas mais básicas de trabalhar dados, obviamente que conseguimos fazer isso python, antes e chegarmos nisso, é interessante saber, como selecionar linhas e colunas de uma base de dados.

Para selecionar colunas, temos 2 modos:

```python
df.dados
```

```python
df['dados']
```

No que digitei acima, parto da ideia da existência de um banco de dados/data frame chamado **df** e que ele tem uma coluna chama **dados**, dessa forma estamos selecionando ela. 

E para selecionar a primeira linha de **df**? E para selecionar a primeira linha de **df** da coluna dados?

```python
df.dados[0]
```

```python
df['dados'][0]
```

Basicamente a sintaxe é o seguinte:

```python
dataframe.coluna[linha]

#ou

dataframe['coluna'][linha]
```

O interessante é, isso tudo que foi explicado, vem diretamente das filtragem de python como língua nativa e não do pandas, algumas vezes nem será necessário usar o Pandas para filtragens mas em outras será extremamente necessário

Então, vamos ao pandas. Ele usa duas ferramentas, loc e iloc e diferente dos esquemas anteriores, ele usa linhas primeiro e colunas depois

Vamos a alguns exemplos com iloc em que suas explicações estarei comentadas em ######

```python
df.iloc[0]
##nesse primeiro caso, o iloc estará trazendo a primeira linha de frutas as colunas

df.iloc[:,0]
##nesse segundo, o iloc traz todas as kinhas da primeira coluna
##lembrando que quando usamos ":" podemos trazer uma série de intervalos
## ":"traz tudo do intervalo
## "0:10"traz tudo do intervalo entre as linhas 1 e 10
## "10:" traz tudo a partir da linha 10
## ":10" traz tudo anterior a linha 10

df.iloc[1:33,0]
#nesse exemplo, ele estará trazendo tudo da linha 1 a 32 da primeira coluna

df.iloc[:44,2:4]
#nesse outro, estamos trazendo tudo a partir da primeira linha até a linha 43, das colunas 1 a 
```

Com relação as colunas, obviamente não precisamos trazer tudo a partir de números, podemos usar os nomes delas

```python
df.iloc[1:33,'dados']
#Aqui estamos selecionando tudo da linha 1 a 32 da coluna dados

```

Mas então, qual a diferença entre loc e iloc?

Bom, loc é costumeiramente mais usado para seleção de valores quando os rótulos tem importância

Além disso, ele seleciona exatamente o intervalo solicitado. Ou seja, vamos usar o intervalo de 0:1000

 

```python
df.iloc[0:1000]
```

Ele irá contar 1000 linhas, mas em python a contagem começa a partir da linha 0, ou seja, ele mostrará até a linha 999

```python
df.loc[0:1000]
```

O python não vai fazer a contagem de linhas mas sim, selecionar o intervalo pré-definido, ou seja, novamente, como a contagem começa no 0, ele vai parar na linha 1000, tendo assim 1001 linhas

Então, vamos partir para o loc, agora tendo uma ou mais condições para filtrar os dados

Se fizermos o seguinte:

```python
df.dados == 'Brasil'
```

Vamos fingir que a coluna dados são países, nesse caso acima, a filtragem funcionará? Bom, a resposta é sim e não!

Conseguiremos ver os valores que são Brasil, mas em formato bool booleano (TRUE & FALSE), além disso, teremos apenas essa coluna.

Então, como poderíamos fazer um filtro como do Excel? Bom, aí já fica um pouco mais complicado

Vamos as sintaxes:

```python
df.loc[df.dados == 'Brasil']
```

Bom, para fazer a filtragem básica, usamos desse modo acima, a sintaxe básica é essa

```python
nomedodataframe.loc[nomedodataframe.nomedacoluna == input desejado]
```

Para filtrar mais de uma coluna

```python
df.loc[(df.dados == 'Brasil') & (df.numeros >= 15)]
```

```python
nomedodataframe.loc[(nomedodataframe.nomedacoluna == input desejado) & (nomedodataframe.nomedacoluna2 == input desejado)]
```

Para filtrar uma coluna ou outra

```python
df.loc[(df.dados == 'Brasil') | (df.numeros >= 15)]
```

```python
nomedodataframe.loc[(nomedodataframe.nomedacoluna == input desejado) | (nomedodataframe.nomedacoluna2 == input desejado)]
```

Para filtrar mais de um valor na mesma coluna

```python
df.loc[df.dados.isin(['Brasil','Portugal'])
```

```python
nomedodataframe.loc[nomedodataframe.nomedacoluna.isin([input desejado])
```

Para filtrar todos os valores, menos x ou y

```python
df.loc[~df.dados.isin(['Brasil','Portugal'])
```

```python
nomedodataframe.loc[~nomedodataframe.nomedacoluna.isin([input desejado])
```

Por fim, para substituir dados:

De toda uma coluna

```python
df['dados']='Umdoistres'
```

Com esse código, todos os dados da coluna dados serão substituídos por umdoistres

```python
df['dados']['Brasil']='Umdoistres'
```

E com o código acima, apenas as linhas onde estiver escrito Brasil na coluna dados, serão substituídos por umdoistres

```python
nome do dataframe[nome da coluna][dado a ser substituido]= novo dado
```

### **Funções summary e maps**

No capítulo anterior vimos como manipular dados, selecionando colunas e aplicando filtros, obviamente foi apenas o começo. Aqui, vamos ver um pouco mais sobre tratamento de dados com as funções summary e maps

Por limitações do Notion, não temos como rodar códigos aqui, então será algo mais teórico

```python
df.coluna1.describe()
```

Bom, a função describe vai extrair da coluna de um dataframe algumas informações, como contagem, média, máximo, mínimo, frequência,tipo de dados, etc. Mas isso pode depender se os dados forem strings ou numéricos

Alguns outros exemplos que podemos usar são mean, unique e value_counts(). Ficaria algo mais ou menos assim:

```python
df.coluna1.mean()

df.coluna1.unique()

df.coluna1.value_counts()
```

Então, vamos falar um pouco sobre a função maps, a principal idéia relacionado a essa função é que ela mapeie e aplique um certo critério linha a linha. Isso  possível se utilizando de um loop e dando call em uma função ou utilizando lambda

Vamos ver as duas formas utilizando o seguinte exemplo

```python
precos = [1000,1400,1125,2250]

def adicionar_imposto(preco):
   return preco × 1.1

precos_com_imposto=[]
for precos in precos:
   precos_com_imposto.append(adicionar_imposto(preco))
print(precos_com_imposto)
```

O código acima está aplicando um método de adicionar impostos em certos valores de uma variável pré definida, para isso, criou-se uma função para adicionar esses impostos.

Em seguida, para vermos os impostos aplicados em todos os preços, foi usado um laço for dando call nessa função anterior, junto ao append e em seguida, o print

Agora, como essa função ficaria com o map?

```python
precos = [1000,1400,1125,2250]
def adicionar_imposto(preco):   
   return preco × 1.1

precos_com_imposto=list(map(adicionar_imposto,precos))
print(precos_com_imposto)
```

A função lambda vem com a missão de simplificar ainda mais o que a map já faz, a diferença, não vamos precisar definir uma função anterior

Lambda tem a seguinte sintaxe

```python
lambda x:x*1,1
```

Ela recebe o valor desejado no x anterior aos : e o valor dado como resposta será o segundo x

Aplicando a função map, o resultado é o seguinte

```python
precos = [1000,1400,1125,2250]
precos_com_imposto=list(map(lambda x:x*1.1, precos))
print(precos_com_imposto)
```

É uma forma mais rápida e mais prática de fazer o resultado acontecer

### **Agrupamento e ordenação**

Agrupar é uma forma de conseguir organizar os dados de acordo com a visualização e ordem que você deseja trazer. 

A ideia é usar o “groupby()” atrelado com algo mais, com valores, médias, contagem, enfim.

Vou tentar passar a usar esse arquivo abaixo para os exemplos

[Database.xlsx](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Database.xlsx)

Após fazer o download desse arquivo, ajuste o caminho dele na linha 2 de acordo com o local que o salvou.

```python
import pandas as pd
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
dados=dados.groupby('Item').Item.count()

print(dados)
```

Esse é um exemplo bem simples, o resultado será um agrupamento dos itens pelas quantidades

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled.png)

Da mesma forma que fizemos esse agrupamento pela contagem dos itens, podemos fazer também usando outras ferramentas, nos dois próximos códigos usaremos o valor minimo e máximo3 atrelado a região

```python
import pandas as pd
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
dados=dados.groupby('Region').Cost.min()

print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%201.png)

```python
import pandas as pd
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
dados=dados.groupby('Region').Cost.max()

print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%202.png)

Mais um método interessante usando o groupby é com o a função agg, que permite a nós rodarmos várias funções diferentes de forma simultânea 

```python
from statistics import mean
import pandas as pd
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
dados=dados.groupby('Region').Cost.agg([len,max,min,mean])

print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%203.png)

Além disso, podemos usar uma, duas, três colunas, quantas quisermos no groupby, segue o exemplo

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
print(type(dados.Cost))

dados1=dados.groupby(['Region','Item']).Total.agg([len])
display(dados1)

print(dados1)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%204.png)

E para finalizar, podemos definir as ordens que queremos dos números, o código abaixo colocamos para organiza-los a partir de Região e Len, de forma que seja do maior para o menor (para isso serve o código ascending mas que por padrão, vem como True no código)

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados1=dados.groupby(['Region','Item']).Total.agg([len])
dados1=dados1.sort_values(by=['Region','len'], ascending=False)
display(dados1)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%205.png)

### **Tipos de dado, Valores NA e Renomear**

Para conseguir pegar os tipos de dados de uma coluna, usamos uma função bem simples chamada “dtype”. Além disso, é possível converter todos os dados de uma coluna

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

print(dados.Total.dtype)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%206.png)

Além disso, podemos ver todos os tipos de dados de um DataFrame usando a mesma função

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

print(dados.dtypes)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%207.png)

Podemos também mudar todos os tipos de dados de uma função, é bem simples

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados.Units=dados.Units.astype('float64')

print(dados.dtypes)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%208.png)

Os missing values, ou os conhecidos NA’s possuem formas de serem tratados, podemos seleciona-los e substitui-los.

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

print(dados[pd.isnull(dados.Rep)])
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%209.png)

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados.Rep=dados.Rep.fillna("Desconhecido")
print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2010.png)

Para finalizar esse assunto, da mesma forma que podemos preencher e mudar linhas com NA’s, podemos também substituir outros valores, no exemplo abaixo, estaremos substituindo “East” por Leste na coluna região, mantendo o código que escreve desconhecido na coluna “REP”

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados.Rep=dados.Rep.fillna("Desconhecido")
dados.Region=dados.Region.replace("East","Leste")
print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2011.png)

Outro ponto, podemos renomear as colunas e até mesmo linhas. No exemplo abaixo estamos mudando os nomes das colunas “orderDate” e “Rep”. Como está sob colchetes, precisamos apenas separar por virgula, sem precisar de outros simbolos como ( ) ou [ ].  Usamos a função rename e dentro dela podemos definir se a usaremos em colunas ou linhas, no caso, para colunas usamos o argumento: “columns={’nome atual’:’novo nome’} enquanto para linhas é bem parecido, usamos o argumento “index={’número da linha’:’nome da linha’}. Seguem os exemplos

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados=dados.rename(columns={'Rep':'Nomes','OrderDate':'Data'})
print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2012.png)

```python
import pandas as pd
from IPython.display import display
dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)

dados=dados.rename(index={0:'Primeira',1:'Segunda'})
print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2013.png)

### **Combinações**

Combinações são basicamente formas de fazer de-para, ou uma forma na programação de fazer procv/procx.

Temos dois métodos que são bem conhecidos, Join e Merge, além do concat.

- **Concat**
    
    Vamos começar pela Concat, ela vem de concaternar ou seja, juntar as bases. Caso tenha uma base com os mesmos nomes de colunas e que deseje juntar, é possível fazer isso usando concat
    
    No exemplo abaixo, usaremos a mesma base, juntando ela com ela mesma. Como assim? Basicamente, estamos apenas renomeando uma nova variável puxando a mesma base, apenas para servir de exemplo
    
    ```python
    import pandas as pd
    from IPython.display import display
    dados=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
    dados1=pd.read_excel('C:\\Users\\lucas\\Downloads\\Database.xlsx',sheet_name=1)
    
    dados=pd.concat([dados,dados1])
    print(dados)
    ```
    
    ![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2014.png)
    
    Apesar de no exemplo acima termos apenas até a linha 42, o Python deixa claro que o DataFrame tem 86 linhas. E para concaternar lado a lado, basta usar pd.concat([dataframe1,dataframe2],axis=1)
    
- **Merge**
    
    O `merge` em Python é uma função utilizada para combinar/juntar dois DataFrames em uma única estrutura, semelhante a um JOIN em SQL. A função `merge()` é parte da biblioteca Pandas, amplamente usada para manipulação e análise de dados. Ela permite unir DataFrames de acordo com colunas ou índices em comum.
    
    ### 1. **Funcionamento do `merge`**
    
    A função `merge()` combina linhas de dois DataFrames com base em colunas ou índices comuns. Ele suporta diferentes tipos de join:
    
    - **Inner Join**: Combina apenas as linhas onde há correspondência entre os DataFrames.
    - **Left Join**: Combina todas as linhas do DataFrame da esquerda, e apenas as correspondentes do DataFrame da direita.
    - **Right Join**: Combina todas as linhas do DataFrame da direita, e apenas as correspondentes do DataFrame da esquerda.
    - **Outer Join**: Combina todas as linhas de ambos os DataFrames, preenchendo os valores ausentes com NaN.
    
    ### 2. **Utilizações**
    
    - **Unir Dados de Fontes Diferentes**: Combinar tabelas relacionadas por meio de colunas comuns.
    - **Enriquecer um DataFrame**: Adicionar colunas com informações adicionais de outro DataFrame.
    - **Realizar Análises Cruzadas**: Fazer comparações e análises entre diferentes conjuntos de dados.
    
    ### 3. **Exemplos Práticos**
    
    ### **Exemplo Básico: Inner Join**
    
    Vamos supor que temos dois DataFrames contendo informações sobre clientes e suas ordens de compra.
    
    ```python
    import pandas as pd
    
    # DataFrame de clientes
    df_clientes = pd.DataFrame({
        'cliente_id': [1, 2, 3, 4],
        'nome': ['Ana', 'Bruno', 'Carlos', 'Daniela']
    })
    
    # DataFrame de ordens
    df_ordens = pd.DataFrame({
        'ordem_id': [101, 102, 103, 104],
        'cliente_id': [1, 2, 3, 3],
        'valor': [250, 120, 310, 150]
    })
    
    # Inner Join com base na coluna 'cliente_id'
    df_merged = pd.merge(df_clientes, df_ordens, on='cliente_id')
    print(df_merged)
    
    ```
    
    **Resultado:**
    
    ```
       cliente_id    nome  ordem_id  valor
    0           1     Ana       101    250
    1           2   Bruno       102    120
    2           3  Carlos       103    310
    3           3  Carlos       104    150
    
    ```
    
    ### **Exemplo Intermediário: Left Join**
    
    Agora, queremos garantir que todos os clientes apareçam no resultado, mesmo que não tenham feito compras.
    
    ```python
    # Left Join para incluir todos os clientes
    df_merged_left = pd.merge(df_clientes, df_ordens, on='cliente_id', how='left')
    print(df_merged_left)
    
    ```
    
    **Resultado:**
    
    ```
       cliente_id    nome  ordem_id  valor
    0           1     Ana     101.0  250.0
    1           2   Bruno     102.0  120.0
    2           3  Carlos     103.0  310.0
    3           3  Carlos     104.0  150.0
    4           4  Daniela       NaN    NaN
    
    ```
    
    ### **Exemplo Avançado: Merge em Múltiplas Colunas e com Suporte a Índices**
    
    Você pode querer unir DataFrames em mais de uma coluna ou até mesmo usando índices.
    
    ```python
    # DataFrame com índice
    df_produtos = pd.DataFrame({
        'produto_id': [1, 2, 3, 4],
        'categoria': ['Eletrônicos', 'Roupas', 'Roupas', 'Móveis']
    }).set_index('produto_id')
    
    # DataFrame de vendas
    df_vendas = pd.DataFrame({
        'produto_id': [1, 2, 2, 3, 3],
        'cliente_id': [1, 2, 2, 3, 4],
        'quantidade': [1, 2, 3, 1, 2]
    })
    
    # Merge usando a coluna e o índice
    df_merged_advanced = pd.merge(df_vendas, df_produtos, left_on='produto_id', right_index=True)
    print(df_merged_advanced)
    
    ```
    
    **Resultado:**
    
    ```
       produto_id  cliente_id  quantidade    categoria
    0           1           1           1  Eletrônicos
    1           2           2           2      Roupas
    2           2           2           3      Roupas
    3           3           3           1      Roupas
    4           3           4           2      Roupas
    
    ```
    
    ### **Exemplo com `suffixes`**
    
    Quando você está unindo DataFrames que possuem colunas com o mesmo nome, o `merge` adiciona sufixos para diferenciar as colunas duplicadas.
    
    ```python
    import pandas as pd
    
    # DataFrame de funcionários
    df_empregados = pd.DataFrame({
        'id': [1, 2, 3],
        'nome': ['Alice', 'Bob', 'Charlie'],
        'departamento': ['TI', 'RH', 'Financeiro']
    })
    
    # DataFrame de gestores
    df_gestores = pd.DataFrame({
        'id': [1, 2, 4],
        'nome': ['Daniel', 'Emma', 'Frank'],
        'departamento': ['TI', 'RH', 'Vendas']
    })
    
    # Realizando o merge com suffixes
    df_merged_suffixes = pd.merge(df_empregados, df_gestores, on='departamento', suffixes=('_emp', '_gestor'))
    print(df_merged_suffixes)
    
    ```
    
    **Resultado:**
    
    ```
       id_emp    nome_emp departamento  id_gestor nome_gestor
    0       1       Alice          TI          1      Daniel
    1       2         Bob          RH          2        Emma
    
    ```
    
    Nesse exemplo, as colunas `id` e `nome`, que aparecem em ambos os DataFrames, são diferenciadas pelos sufixos `_emp` e `_gestor`.
    
    ### **Tratamento de Duplicatas com `drop_duplicates`**
    
    Após um merge, você pode acabar com duplicatas que precisam ser removidas. O método `drop_duplicates()` é útil para isso.
    
    ```python
    # DataFrame de vendas
    df_vendas = pd.DataFrame({
        'cliente_id': [1, 2, 2, 3],
        'produto_id': [101, 102, 102, 103],
        'quantidade': [1, 2, 2, 1]
    })
    
    # DataFrame de clientes
    df_clientes = pd.DataFrame({
        'cliente_id': [1, 2, 3],
        'nome': ['Ana', 'Bruno', 'Carlos']
    })
    
    # Realizando o merge
    df_merged_duplicates = pd.merge(df_vendas.drop_duplicates(subset="produto_id"), df_clientes, on='cliente_id')
    
    # Removendo duplicatas
    print(df_merged_duplicates )
    
    ```
    
    **Resultado:**
    
    ```
       cliente_id  produto_id  quantidade    nome
    0           1        101           1    Ana
    1           2        102           2  Bruno
    3           3        103           1 Carlos
    
    ```
    
    Aqui, as duplicatas foram removidas após o merge.
    
    ### **Seleção de Colunas Durante o `merge`**
    
    Às vezes, você não precisa de todas as colunas do DataFrame após o merge. Você pode selecionar apenas as colunas desejadas diretamente na operação.
    
    ```python
    # DataFrame de produtos
    df_produtos = pd.DataFrame({
        'produto_id': [101, 102, 103],
        'nome_produto': ['Notebook', 'Camiseta', 'Cadeira'],
        'preco': [3000, 50, 200]
    })
    
    # DataFrame de vendas
    df_vendas = pd.DataFrame({
        'venda_id': [1, 2, 3],
        'produto_id': [101, 102, 103],
        'quantidade': [2, 5, 1]
    })
    
    # Realizando o merge e selecionando colunas específicas
    df_merged_selected_columns = pd.merge(df_vendas, df_produtos[['produto_id', 'nome_produto']], on='produto_id')
    print(df_merged_selected_columns)
    
    ```
    
    **Resultado:**
    
    ```
       venda_id  produto_id  quantidade nome_produto
    0         1        101           2     Notebook
    1         2        102           5     Camiseta
    2         3        103           1      Cadeira
    
    ```
    
    Neste exemplo, após o merge, apenas as colunas `produto_id` e `nome_produto` do DataFrame `df_produtos` foram selecionadas.
    
    ### **Exemplo Combinado: `suffixes`, `drop_duplicates`, e Seleção de Colunas**
    
    Você pode combinar todas essas técnicas para manipular seus DataFrames de forma eficiente.
    
    ```python
    # DataFrame de produtos
    df_produtos = pd.DataFrame({
        'produto_id': [101, 102, 103, 104],
        'nome_produto': ['Notebook', 'Camiseta', 'Cadeira', 'Mesa'],
        'categoria': ['Eletrônicos', 'Roupas', 'Móveis', 'Móveis'],
        'preco': [3000, 50, 200, 350]
    })
    
    # DataFrame de vendas
    df_vendas = pd.DataFrame({
        'venda_id': [1, 2, 3, 4, 5],
        'produto_id': [101, 102, 102, 103, 104],
        'quantidade': [2, 5, 5, 1, 2]
    })
    
    # Realizando o merge com suffixes e selecionando colunas
    df_merged_combined = pd.merge(
        df_vendas,
        df_produtos[['produto_id', 'nome_produto', 'categoria']].drop_duplicates(subset='produto_id'),
        on='produto_id',
        suffixes=('_venda', '_produto')
    )
    
    print(df_merged_combined)
    
    ```
    
    **Resultado:**
    
    ```
       venda_id  produto_id  quantidade nome_produto   categoria
    0         1        101           2     Notebook  Eletrônicos
    1         2        102           5     Camiseta      Roupas
    3         4        103           1      Cadeira      Móveis
    4         5        104           2         Mesa      Móveis
    
    ```
    
    Neste exemplo, usamos `suffixes` para diferenciar colunas, `drop_duplicates` para remover duplicatas, e selecionamos apenas as colunas necessárias para o resultado final.
    
    ### 4. **Combinações de Merge**
    
    Além dos exemplos básicos, você pode explorar combinações complexas utilizando o `merge()` com parâmetros como `suffixes` para lidar com colunas de mesmo nome, ou combinando diferentes tipos de join para diferentes DataFrames.
    
    Vamos explorar algumas funcionalidades avançadas do `merge()` em Python, incluindo o uso de `suffixes`, tratamento de duplicatas, e a seleção de colunas diretamente na operação de merge.
    
- **Join**
    
    O `join` em Python, especificamente no contexto do Pandas, é uma operação que permite combinar dois DataFrames com base em um índice comum. Enquanto o `merge` é mais flexível e permite unir DataFrames com base em colunas, o `join` é mais adequado para combinações baseadas em índices.
    
    ### 1. **Funcionamento do `join`**
    
    A função `join()` no Pandas é utilizada para combinar dois DataFrames com base em seus índices. Você pode especificar o tipo de junção (inner, left, right, outer) e como lidar com colunas duplicadas.
    
    ### 2. **Utilizações**
    
    - **Unir DataFrames Baseados em Índices**: Ideal para combinar DataFrames que compartilham um índice comum.
    - **Adicionar Informações a um DataFrame**: Similar ao `merge`, mas mais conveniente quando as tabelas já estão indexadas.
    
    ### 3. **Exemplos Práticos**
    
    ### **Exemplo Básico: Left Join**
    
    Neste exemplo, vamos combinar dois DataFrames usando um `left join` com base nos índices.
    
    ```python
    import pandas as pd
    
    # DataFrame de empregados
    df_empregados = pd.DataFrame({
        'nome': ['Ana', 'Bruno', 'Carlos', 'Daniela'],
        'departamento': ['TI', 'RH', 'Financeiro', 'TI']
    }, index=[1, 2, 3, 4])
    
    # DataFrame de salários
    df_salarios = pd.DataFrame({
        'salario': [7000, 6000, 5000],
        'bonus': [500, 400, 300]
    }, index=[1, 2, 3])
    
    # Left Join
    df_join_left = df_empregados.join(df_salarios, how='left')
    print(df_join_left)
    
    ```
    
    **Resultado:**
    
    ```
          nome departamento  salario  bonus
    1      Ana           TI   7000.0  500.0
    2    Bruno           RH   6000.0  400.0
    3   Carlos   Financeiro   5000.0  300.0
    4  Daniela           TI      NaN    NaN
    
    ```
    
    ### **Exemplo Intermediário: Inner Join**
    
    Um `inner join` combina apenas as linhas em que os índices estão presentes em ambos os DataFrames.
    
    ```python
    # Inner Join
    df_join_inner = df_empregados.join(df_salarios, how='inner')
    print(df_join_inner)
    
    ```
    
    **Resultado:**
    
    ```
         nome departamento  salario  bonus
    1     Ana           TI   7000.0  500.0
    2   Bruno           RH   6000.0  400.0
    3  Carlos   Financeiro   5000.0  300.0
    
    ```
    
    ### **Exemplo Avançado: Join com `suffixes`**
    
    Se os DataFrames tiverem colunas com os mesmos nomes, você pode adicionar sufixos para diferenciá-las.
    
    ```python
    # DataFrame de horas trabalhadas
    df_horas = pd.DataFrame({
        'horas_trabalhadas': [160, 150, 120, 140],
        'departamento': ['TI', 'RH', 'Financeiro', 'TI']
    }, index=[1, 2, 3, 4])
    
    # Join com sufixes
    df_join_suffixes = df_empregados.join(df_horas, lsuffix='_emp', rsuffix='_horas')
    print(df_join_suffixes)
    
    ```
    
    **Resultado:**
    
    ```
          nome_emp departamento_emp  horas_trabalhadas departamento_horas
    1        Ana               TI               160                  TI
    2      Bruno               RH               150                  RH
    3     Carlos      Financeiro               120           Financeiro
    4    Daniela              TI               140                  TI
    
    ```
    
    ### **Tratamento de Duplicatas e Seleção de Colunas no Join**
    
    Você pode tratar duplicatas e selecionar colunas específicas após a operação de join.
    
    ```python
    # Join com seleção de colunas específicas e tratamento de duplicatas
    df_join_selected = df_empregados.join(df_horas[['horas_trabalhadas']], how='left').drop_duplicates(subset=['nome'])
    print(df_join_selected)
    
    ```
    
    **Resultado:**
    
    ```
          nome departamento  horas_trabalhadas
    1      Ana           TI               160
    2    Bruno           RH               150
    3   Carlos   Financeiro               120
    4  Daniela           TI               140
    
    ```
    
    ### 4. **Exemplo Combinado: Join Complexo**
    
    Agora, vamos combinar várias técnicas: sufixes, tratamento de duplicatas e seleção de colunas em um único join.
    
    ```python
    # Join combinado com sufixes e seleção de colunas
    df_join_combined = df_empregados.join(
        df_horas[['horas_trabalhadas', 'departamento']],
        how='outer',
        lsuffix='_emp',
        rsuffix='_horas'
    ).drop_duplicates(subset=['nome_emp'])
    
    # Seleção de colunas específicas
    df_join_final = df_join_combined[['nome_emp', 'departamento_emp', 'horas_trabalhadas']]
    print(df_join_final)
    
    ```
    
    **Resultado:**
    
    ```
          nome_emp departamento_emp  horas_trabalhadas
    1        Ana               TI               160
    2      Bruno               RH               150
    3     Carlos      Financeiro               120
    4    Daniela              TI               140
    
    ```
    
    - **Combinações - Join e Map**
        
        Combinar a operação de `join` com `map` no Pandas pode ser muito útil para aplicar transformações ou adicionar informações em colunas de DataFrames antes ou depois do `join`. Vamos ver alguns exemplos práticos dessa combinação.
        
        ### 1. **Exemplo Básico: Usando `map` Antes do `join`**
        
        Suponha que você tem um DataFrame com IDs e deseja substituir esses IDs pelos nomes correspondentes usando um dicionário de mapeamento.
        
        ```python
        import pandas as pd
        
        # DataFrame de vendas com IDs de clientes
        df_vendas = pd.DataFrame({
            'cliente_id': [1, 2, 3, 4],
            'produto': ['Notebook', 'Camiseta', 'Cadeira', 'Mesa'],
            'quantidade': [1, 2, 3, 1]
        })
        
        # Dicionário de mapeamento de IDs para nomes de clientes
        cliente_map = {
            1: 'Ana',
            2: 'Bruno',
            3: 'Carlos',
            4: 'Daniela'
        }
        
        # Aplicando map para substituir IDs por nomes
        df_vendas['cliente_nome'] = df_vendas['cliente_id'].map(cliente_map)
        
        print(df_vendas)
        
        ```
        
        **Resultado:**
        
        ```
           cliente_id   produto  quantidade cliente_nome
        0           1  Notebook          1         Ana
        1           2  Camiseta          2       Bruno
        2           3   Cadeira          3      Carlos
        3           4      Mesa          1     Daniela
        
        ```
        
        Neste exemplo, usamos `map` para substituir os IDs dos clientes pelos seus nomes antes de realizar um `join`.
        
        ### 2. **Exemplo Intermediário: Usando `join` e `map` Juntos**
        
        Agora, vamos fazer um `join` e, em seguida, aplicar `map` para criar uma nova coluna com base nas informações combinadas.
        
        ```python
        # DataFrame de departamentos
        df_departamentos = pd.DataFrame({
            'departamento_id': [1, 2, 3],
            'departamento': ['TI', 'RH', 'Financeiro']
        }, index=[1, 2, 3])
        
        # DataFrame de empregados com IDs de departamentos
        df_empregados = pd.DataFrame({
            'nome': ['Ana', 'Bruno', 'Carlos', 'Daniela'],
            'departamento_id': [1, 2, 3, 1]
        })
        
        # Join para combinar informações
        df_empregados_completo = df_empregados.join(df_departamentos, on='departamento_id')
        
        # Usando map para criar uma nova coluna de descrições
        descricao_map = {
            'TI': 'Tecnologia da Informação',
            'RH': 'Recursos Humanos',
            'Financeiro': 'Departamento Financeiro'
        }
        
        df_empregados_completo['descricao'] = df_empregados_completo['departamento'].map(descricao_map)
        
        print(df_empregados_completo)
        
        ```
        
        **Resultado:**
        
        ```
              nome  departamento_id departamento                 descricao
        0      Ana               1           TI  Tecnologia da Informação
        1    Bruno               2           RH          Recursos Humanos
        2   Carlos               3   Financeiro  Departamento Financeiro
        3  Daniela               1           TI  Tecnologia da Informação
        
        ```
        
        Aqui, após o `join`, aplicamos um `map` para adicionar uma coluna com a descrição completa do departamento.
        
        ### 3. **Exemplo Avançado: Mapeamento Condicional após um Join**
        
        Suponha que você precise criar uma coluna que atribua um valor baseado em condições complexas após um `join`.
        
        ```python
        # DataFrame de funcionários
        df_funcionarios = pd.DataFrame({
            'funcionario_id': [1, 2, 3, 4],
            'nome': ['Ana', 'Bruno', 'Carlos', 'Daniela'],
            'departamento': ['TI', 'TI', 'RH', 'Financeiro']
        })
        
        # DataFrame de salários por departamento
        df_salarios = pd.DataFrame({
            'departamento': ['TI', 'RH', 'Financeiro'],
            'salario_base': [7000, 6000, 5000]
        })
        
        # Join baseado no departamento
        df_funcionarios_completo = df_funcionarios.join(df_salarios.set_index('departamento'), on='departamento')
        
        # Aplicando map para criar uma nova coluna de bônus baseado no departamento
        bonus_map = {
            'TI': lambda x: x * 0.1,      # 10% de bônus para TI
            'RH': lambda x: x * 0.15,     # 15% de bônus para RH
            'Financeiro': lambda x: x * 0.2  # 20% de bônus para Financeiro
        }
        
        df_funcionarios_completo['bonus'] = df_funcionarios_completo.apply(
            lambda row: bonus_map[row['departamento']](row['salario_base']), axis=1
        )
        
        print(df_funcionarios_completo)
        
        ```
        
        **Resultado:**
        
        ```
           funcionario_id     nome departamento  salario_base  bonus
        0               1      Ana           TI          7000   700.0
        1               2    Bruno           TI          7000   700.0
        2               3   Carlos           RH          6000   900.0
        3               4  Daniela   Financeiro          5000  1000.0
        
        ```
        
        Neste exemplo, usamos `apply` em conjunto com `map` para aplicar uma função condicional baseada no departamento de cada funcionário após o `join`.
        
        ### 4. **Exemplo Combinado: Join, Map, e Tratamento de Duplicatas**
        
        Podemos combinar tudo: realizar um `join`, aplicar um `map`, e tratar duplicatas em um único fluxo de trabalho.
        
        ```python
        # DataFrame de projetos
        df_projetos = pd.DataFrame({
            'projeto_id': [1, 2, 3, 4],
            'departamento': ['TI', 'TI', 'RH', 'Financeiro'],
            'horas_trabalhadas': [120, 150, 100, 110]
        })
        
        # DataFrame de departamentos com IDs
        df_departamentos = pd.DataFrame({
            'departamento_id': [1, 2, 3],
            'departamento': ['TI', 'RH', 'Financeiro']
        }, index=[1, 2, 3])
        
        # Join para combinar informações
        df_projetos_completo = df_projetos.join(df_departamentos.set_index('departamento'), on='departamento', lsuffix='_proj', rsuffix='_dept')
        
        # Map para atribuir custo por hora baseado no departamento
        custo_hora_map = {
            'TI': 100,
            'RH': 80,
            'Financeiro': 90
        }
        
        df_projetos_completo['custo_total'] = df_projetos_completo['horas_trabalhadas'] * df_projetos_completo['departamento'].map(custo_hora_map)
        
        # Removendo duplicatas (se houvesse)
        df_projetos_final = df_projetos_completo.drop_duplicates()
        
        print(df_projetos_final)
        
        ```
        
        **Resultado:**
        
        ```
           projeto_id departamento_proj  horas_trabalhadas departamento_dept  departamento_id  custo_total
        0           1                TI                120                TI               NaN        12000
        1           2                TI                150                TI               NaN        15000
        2           3                RH                100                RH               NaN         8000
        3           4        Financeiro                110        Financeiro               NaN         9900
        
        ```
        
        Nesse exemplo, aplicamos o `map` para calcular o custo total com base nas horas trabalhadas e no custo por hora de cada departamento após o `join`, e removemos duplicatas no final.
        
        Esses exemplos mostram como você pode combinar `join` e `map` para criar fluxos de trabalho poderosos e flexíveis no Pandas. Se precisar de mais exemplos ou quiser explorar outras possibilidades, estou à disposição!
        
    

### **Adicional: Funções para colunas**

**** [python - How can I use the apply() function for a single column? - Stack Overflow](https://stackoverflow.com/questions/34962104/how-can-i-use-the-apply-function-for-a-single-column)

Bom, qual a ideia aqui: Basicamente, você tem colunas com valor x, y e z. Mas a coluna z1 deverá ser a soma das colunas y e z, isso é possível ser feito? De quais formas podemos fazer isso?

Bom, a mais interessante é usar a função lambda

- Lambda com apply
    
    Bom, diferentemente do anterior, a mesma coisa pode ser feita mas em menos linhas, são as chamadas funções anônimas, sem necessariamente precisarmos nomear.
    
    ```jsx
    import pandas as pd
    
    df = pd.read_csv("C:\\Users\\lucas\\Downloads\\insurance.csv")
    
    df["nova coluna"]=df.apply(lambda x: x['age']*x['bmi'],axis=1)
    
    print(df["nova coluna"])
    ```
    
    Quando você adaptar o caminho do arquivo para seu computador e testa-lo, vai ter o seguinte retorno:
    
    ![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2015.png)
    
    Outra forma, ainda usando lambda, é aplicando uma função pré-definida, como no código abaixo:
    
    ```jsx
    import pandas as pd
    
    df = pd.read_csv("C:\\Users\\lucas\\Downloads\\insurance.csv")
    
    def applyfunc1(x,y):
        return x*y
    
    df["col1"] = df.apply(lambda x: applyfunc1(x['age'],x['bmi']),axis=1)
    
    print(df["col1"])
    ```
    
    Aqui, definimos que 2 colunas (x e y) iriam se multiplicar por meio de uma função separada, em seguida utilizamos o lambda para fazer sua aplicação na nova coluna que definimos
    

## **Datavis**

### **Gráficos de linhas**

- **Arquivos**
    
    [fifa.csv](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/fifa.csv)
    

Datavis vem de Data Visualization e possui algumas bibliotecas, nos exemplos da trilha, são usadas as bibliotecas a seguir:

```python
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
print("Setup Complete")
```

Porém não consegui fazer a seaborn rodar no Jupyter que eu havia criado, assim como a %matplotlib não rodou nos offlines (Pycharm e Visual Studio) e não encontrei soluções pra isso, mas pelo menos até então, não me atraapalhou em nada.

Vamos usar o mesmo exemplo da trilha

```python
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\fifa.csv', index_col='Date', parse_dates=True)
print(dados.head())

# Set the width and height of the figure
plt.figure(figsize=(16,6))

# Line chart showing how FIFA rankings evolved over time 
sns.lineplot(data=dados)
plt.show()
```

![Figure_1.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Figure_1.png)

Como podemos ver, os dados estão bagunçados… Como podemos selecionar 2 ou mais países dessa lista para analisarmos? Bom, a resposta é simples, veja no exemplo abaixo

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\fifa.csv', index_col='Date', parse_dates=True)
print(dados.head())

# Set the width and height of the figure
plt.figure(figsize=(16,6))

# Line chart showing how FIFA rankings evolved over time from Brazil and Argentina
sns.lineplot(data=dados['ARG'],label='Argentina')
sns.lineplot(data=dados['BRA'],label='Brasil')
plt.show()
```

O segredo está nas últimas linhas, selecionamos quais colunas queremos usar, da mesma forma que fizemos com o Pandas algumas vezes. Além disso, temos um novo fator chamado “Label”, ele serve para inserirmos a legenda e dizermos o que significa a linha que ele está plotando

### **Gráficos** **de Colunas**

- Arquivos
    
    [flight_delays.csv](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/flight_delays.csv)
    

Bom, como sugerido, vamos aprender um pouco sobre gráfico de colunas!!!

A sintaxe é simples, quase a mesma que do anterior, a diferença é que usaremos sns.barplot

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\flight_delays.csv', index_col='Month')
print(dados.head())

# Set the width and height of the figure
plt.figure(figsize=(16,6))

# Line chart showing how FIFA rankings evolved over time 
plt.title('Average Arrival Delay for Spirit Airlines Flights, by Month')

sns.barplot(x=dados.index ,y=dados['NK'])
plt.ylabel("Arrival delay (in minutes)")
plt.xlabel('Mês')

plt.show()
```

Vamos lá, o que está acontecendo no código acima? 

Bom, como esperado está criando um gráfico de colunas, além do já padronizado linha de dados, somos apresentados a dois novos fatores, a nomear titulo, coluna Y e coluna x

A sintaxe, como esperada é bem simples, você define qual eixo vai nomear e simplesmente digita as strings. O resultado é o gráfico abaixo

![Airplanes.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Airplanes.png)

### **Mapa de Calor**

Seguindo a mesma linha dos gráficos de colunas, além disso, usando os mesmos dados, vamos criar um mapa de calor para conseguirmos analisar os dados de atraso de todas as empresas aéreas que lá estão listadas

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\flight_delays.csv', index_col='Month')
print(dados.head())

# Set the width and height of the figure
plt.figure(figsize=(16,6))

# Heatmap showing average arrival delay for each airline by month
sns.heatmap(data=dados, annot=True)

# Add label for horizontal axis
plt.xlabel("Aérea")
plt.ylabel("Mês")

plt.show()
```

Como podemos analisar até aqui, os códigos para plotagem de gráficos são muito semelhantes, porém gostaria de chamar atenção para um detalhe em especial do mapa de calor, a função “Annot”.

Ela torna fundamental a visualização dos dados de forma mais clara, os números passam a ficar visiveis com sua função sendo True, como nos exemplos abaixo

Annot = False

![Annot False.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Annot_False.png)

Annot True

![Annot True.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Annot_True.png)

Fica claro quando aberta a imagem, o grande impacto dessa função em particular

### **Gráficos de Dispersão**

- Arquivo
    
    [insurance.csv](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/insurance.csv)
    

Os gráficos de dispersão são relacionados a estatística, eles mostram de forma visual relações entre uma ou mais variáveis. Entender esse tipo de gráfico força com que pelo menos um mínimo no domínio de estatística tenha que ter sido aprendido

O banco de dados que estaremos usando para esses exemplos é composto por “Idade, sexo, bmi (imc), filhos, fumante, região, taxas”

A primeira análise que faremos será usando as taxas pagas a companhia de seguro junto ao imc, para identificarmos se existe alguma correlação

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\insurance.csv')
print(dados.head())

plt.figure(figsize=(16,6))

sns.scatterplot(x=dados['bmi'], y=dados['charges'])
plt.title("IMC x Taxas")
plt.show()
```

![IMC x Taxas 1.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/IMC_x_Taxas_1.png)

Clicando na imagem, podemos fazer uma primeira análise preeliminar, nela vemos que existe uma tendência do pagamento de taxas mais altas para qual o aumento do IMC, então podemos considerar uma correlação positiva. Podemos enxergar melhor traçando uma linha nesse gráfico

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\insurance.csv')
print(dados.head())

plt.figure(figsize=(16,6))

sns.regplot(x=dados['bmi'], y=dados['charges'])
plt.title("IMC x Taxas")
plt.show()
```

![IMC x Taxas 2.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/IMC_x_Taxas_2.png)

Dentro desse tipo de modelo, podemos segmentar um pouco mais, como foi dito acima, existe uma coluna para pessoas que fumam ou não fumam, afinal, será que existe alguma influência? Visualmente conseguimos fazer essa análise

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\insurance.csv')
print(dados.head())

plt.figure(figsize=(16,6))

sns.scatterplot(x=dados['bmi'], y=dados['charges'], hue=dados["smoker"])
plt.title("IMC x Taxas X Fumantes")
plt.show()
```

Antes de continuarmos, usamos um novo fator na construção do gráfico, o “Hue”. Ele vem diretamente do inglês, em tradução literal pode ser algo relacionado a tom/tonalidade, por isso é usado para coloração desses pontos que estaremos apresentando no gráfico abaixo

![IMC x Taxas 3.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/IMC_x_Taxas_3.png)

Focando na análise, já sabíamos que existia uma correlação entre o aumento do IMC e quanto as pessoas pagam pelos seguros, agora vemos uma clara relação não apenas entre as variáveis anteriores mas com os fumantes, eles claramente a medida que o IMC aumenta, começam a pagar valores ainda maiores  

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\insurance.csv')
print(dados.head())

plt.figure(figsize=(16,6))

sns.lmplot(x='bmi', y='charges', hue='smoker', data=dados)
plt.title("IMC x Taxas X Fumantes")
plt.show()
```

![IMC x Taxas 4.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/IMC_x_Taxas_4.png)

Esse gráfico foi usada uma outra função mas a ideia continua sendo a mesma, a principal diferença é que estávamos selecionando dentro das variáveis que compõe o gráfico suas informações, puxando elas de sua variável original diretamente para visualização

Nessa a única diferença é que precisamos deixar claro para função de onde ela estará puxando as informações, pois não teremos como fazer no mesmo formato dos anteriores

Isso explicado, vamos a uma pequena análise do que nos foi printado, como foi explicado, ficou clara a correlação dos fumantes e não fumantes, agora para mostra-la de forma mais clara, inserimos 2 linhas, uma para cada categoria

### **Funções SNS dos gráficos**

- **Trends**- Uma tendência é definida como um padrão de mudança.
    - `sns.lineplot` - **Gráficos de linha** são melhores para mostrar tendências ao longo do tempo, e várias linhas podem ser usadas para mostrar tendências em mais de um grupo.
- **Relationship** - Existem muitos tipos diferentes de gráficos que você pode usar para entender as relações entre variáveis em seus dados.
    - `sns.barplot` - **Gráficos de barras** são úteis para comparar quantidades correspondentes a diferentes grupos.
    - `sns.heatmap` - **Mapas de calor** podem ser usados para encontrar padrões codificados por cores em tabelas de números.
    - `sns.scatterplot` - **Gráficos de dispersão** mostram a relação entre duas variáveis contínuas; se codificados por cores, também podemos mostrar a relação com uma terceira [variável categórica](https://en.wikipedia.org/wiki/Categorical_variable).
    - `sns.regplot` - Incluir uma **linha de regressão** no gráfico de dispersão facilita a visualização de qualquer relação linear entre duas variáveis.
    - `sns.lmplot` - Este comando é útil para desenhar várias linhas de regressão, se o gráfico de dispersão contiver múltiplos grupos codificados por cores.
    - `sns.swarmplot` - **Gráficos de dispersão categóricos** mostram a relação entre uma variável contínua e uma variável categórica.
- **Distribution** - Visualizamos distribuições para mostrar os valores possíveis que podemos esperar ver em uma variável, juntamente com a probabilidade deles ocorrerem.
    - `sns.histplot` - **Histogramas** mostram a distribuição de uma única variável numérica.
    - `sns.kdeplot` - **Gráficos KDE** (ou **gráficos KDE 2D**) mostram uma distribuição estimada e suavizada de uma única variável numérica (ou duas variáveis numéricas).
    - `sns.jointplot` - Este comando é útil para exibir simultaneamente um gráfico KDE 2D com os gráficos KDE correspondentes para cada variável individual.
    
    Vale lembrar disso aqui: Esta função abaixo altera os estilos (cor de fundo)
    
    ```python
    # Alterar o estilo da figura para o tema "dark"
    sns.set_style("dark")
    
    ```
    
    E os temas disponíveis são:
    
    - darkgrid
    - whitegrid
    - dark
    - white
    - ticks
    
    **Exemplo**: Tema normal
    
    ![](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Figura_tema_normal.png)
    
    **Exemplo**: Tema escuro
    
    ![](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Figura_tema_dark.png)
    

## **Tratamento de dados**

### **Data Cleaning**

- Arquivos

Vamos trabalhar aqui um básico para tratamento de dados, principalmente dados vazios.

Basicamente, vamos tratar de 2 formas, substituindo os valores vazios e, digamos, os “abandonando”, retirando eles do dataframe

A primeira forma, extremamente viável para termos uma noção de como os dados estão, é usar uma soma.

Como assim? Bom, podemos simplesmente fazer a contagem, tanto de todo o dataframe quanto de uma coluna especifica. Então, vamos lá demonstrar isso 🙂

```python
from cProfile import label
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
import seaborn as sns

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\NFL Play by Play 2009-2018 (v5).csv')
print(dados.head())

var=dados.isnull().sum()
print(var[0:10])
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2016.png)

O código acima, como pode ver esta pegando o arquivo e somando o número de células brancas, nesse caso, selecionamos as 11 primeiras colunas e vemos que são valores consideraveis

No exemplo abaixo, buscamos somar todas as porcentagens das colunas relacionados aos valores vazios e trazer os dados de suas porcentagens

```python
import pandas as pd
import numpy as np

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\NFL Play by Play 2009-2018 (v5).csv')
print(dados.head())

var=dados.isnull().sum()

total=np.product(dados.shape)
por=(var/total)*100
print(sum(por))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2017.png)

Vemos que o total é de 38,5% de dados vazios, mais de 1/3.

Bom, e como podemos remover esses dados vazios?

Temos 2 formas, substituindo esses dados ou dando drop.

Vamos para a alternativa do Drop

```python
import pandas as pd
import numpy as np

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\NFL Play by Play 2009-2018 (v5).csv')
print(dados.head())

print(dados.dropna())
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2018.png)

Como podemos ver, o resultado foi um dataframe vazio. O motivo é simples, o dropna() da drop em todas as linhas com algum NaN, ou seja, todas as linhas tinham pelo menos um NaN em alguma coluna, uma alternativa interessante é inverter e invés de utilizarmos as linhas, vamos usar as colunas usando axis=1

```python
import pandas as pd
import numpy as np

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\NFL Play by Play 2009-2018 (v5).csv')
print(dados.head())

print(dados.dropna(axis=1))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2019.png)

Agora, para substituirmos dados, usamos o fillna() e dentro do parenteses usamos o valor que desejamos que o python substitua 

No exemplo abaixo, demos print em uma coluna que possuia um NA e substituimos esse valor por zero

```python
import pandas as pd
import numpy as np

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\NFL Play by Play 2009-2018 (v5).csv')
print(dados.head())
print(dados['posteam'])

dados=dados.fillna(0)
print(dados['posteam'])
```

DataFrame original, sem o fillna()

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2020.png)

DataFrame com o fillna(0)

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2021.png)

### **Trabalhando com datas**

- **Arquivos**

Bom, quando carregamos dados dentro do Python, não é incomum termos alguma coluna com datas, e não datas no sentido de dados (em inglês data) mas sim realmente datas, como dd/mm/yy ou em outros formatos.

Porém nós sabermos que tal coluna são datas quer dizer que o Python vai conseguir identificar da mesma forma? 

A resposta para essa pergunta é não, então vamos precisar fazer esse apontamento a ele. Vejamos no exemplo abaixo:

```python
import pandas as pd
import numpy as np
import seaborn as sns
import datetime

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\catalog.csv')

np.random.seed(0)

print(dados.iloc[:7,:4])
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2022.png)

Aqui estamos printando as 7 primeiras linhas e 4 primeiras colunas mas a única que nos interessa é a coluna date, vamos tentar identificar como o Python está identificando essa coluna, e isso podemos fazer de dois jeitos, usando .head() e .dtype. As duas formas estarão abaixo

```python
import pandas as pd
import numpy as np
import seaborn as sns
import datetime

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\catalog.csv')

np.random.seed(0)

print(dados['date'].head())

print(dados['date'].dtype)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2023.png)

O .head() está indo até a linha escrito “Name:date, dtype:object” 

A linha logo abaixo é a do dtype, ambas elas funcionam para aquilo que precisamos. 

Agora, bom notarmos, temos o resultado do tipo de dado, no caso, “object”. Então para trabalharmos com datas, devemos converter.

```python
import pandas as pd
import numpy as np
import seaborn as sns
import datetime

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\catalog.csv')

np.random.seed(0)

dados['date']=pd.to_datetime(dados['date'])

print(dados['date'].head())
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2024.png)

Agora, conseguimos ver que o Python identifica a coluna date como uma coluna com datas.

### **Entradas de dados inconsistentes**

- Arquivos
    
    [pakistan_intellectual_capital.csv](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/pakistan_intellectual_capital.csv)
    

Como sabemos, ao estarmos usando uma base de dados, podemos ter inconsistências. Nesse caso em especifico, me refiro a inconsistências como nomes sem letras maiúsculas ou com e sem espaço, para isso existem formas de tratar esses dados.

Então, vamos começar com o código abaixo:

```python
import pandas as pd
import numpy as np
import fuzzywuzzy
from fuzzywuzzy import process
import chardet

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\pakistan_intellectual_capital.csv')

np.random.seed(0)

print(dados.head())
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2025.png)

No caso desse arquivo, vamos trabalhar com a coluna “Country”, vamos tentar padronizar os nomes e entender se pode ter acontecido digitações erradas do nome dos países. Então, vamos lá

```python
import pandas as pd
import numpy as np
import fuzzywuzzy
from fuzzywuzzy import process
import chardet

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\pakistan_intellectual_capital.csv')

np.random.seed(0)

Country=dados['Country']
Country=Country.unique()
print(Country)
print(sorted(Country))
```

Nesse código, estamos puxando a coluna Country e usando a função Unique para termos apenas dados não repetidos, após isso os deixamos em ordem alfabética. O primeiro print abaixo, servirá para mostrar a função unique, o segundo o sorted(ordem alfabética) e o terceiro os dois juntos no compilador do Python junto com algumas explicações

Função Unique

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2026.png)

Função sorted

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2027.png)

Ambos juntos:

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2028.png)

Bom, agora que temos a visão completa tem algo legal para percebermos, apesar de estar em ordem alfabética, Germany, New Zealand, Swaden e USA estão antes de Australia. O motivo disso é apenas um, espaços em branco antes da primeira letra, enquanto também temos germany em último, depois de Urbana, o motivo é que não tem letra maiúscula 

Como podemos tratar isso? Bom, podemos deixar tudo maisculo ou minusculo e remover os espaços em branco

Vamos fazer os dois casos mas vou continuar com minúsculo (Simplesmente pq eu quero 🙂)

```python
import pandas as pd
import numpy as np
import fuzzywuzzy
from fuzzywuzzy import process
import chardet

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\pakistan_intellectual_capital.csv')

np.random.seed(0)

dados['Country']=dados['Country'].str.upper()
print(dados['Country'])

dados['Country']=dados['Country'].str.lower()
print(dados['Country'])

dados['Country']=dados['Country'].str.strip()

Country=dados['Country']
Country=Country.unique()
print(Country)
print(sorted(Country))
```

Podemos ver aqui a diferença de aplicação entre maiúsculas e minúsculas com .upper (maiúsculas) e .lower(minúsculas).

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2029.png)

Na imagem abaixo, conseguimos ver melhor a aplicação da função .lower junto da unique(), com a função strip() que remove os espaços em branco tanto do começo de uma string quanto do final

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2030.png)

E por fim, sorted()

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2031.png)

Como podemos ver, os problemas anteriormente registrados, foram corrigidos!!

Mas ainda temos uma outra situação. “South korea” e “SouthKorea”. Claro, poderiamos substituir usando pandas como vimos acima em outros módulos, mas podemos fazer de uma forma um pouco mais complexa e que permitirá fazer mais de uma vez usando uma função

Nesse cenário, é de fácil análise pq não são muitos dados e são apenas de paises, por isso a idéia da função é recomendada, então vamos começar a análise 

A fuzzywyzzy ajuda a entender strings que sejam próximas uma da outra com um certo tipo de relação, ajudando a poupar algum tempo

```python
import pandas as pd
import numpy as np
import fuzzywuzzy
from fuzzywuzzy import process
import chardet

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\pakistan_intellectual_capital.csv')

np.random.seed(0)

dados['Country']=dados['Country'].str.lower()
dados['Country']=dados['Country'].str.strip()

Country=dados['Country']
Country=Country.unique()

matches = fuzzywuzzy.process.extract("south korea", Country, limit=10, scorer=fuzzywuzzy.fuzz.token_sort_ratio)
print(matches)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2032.png)

Essa é a saída, 100 é o valor máximo e a medida que vai diminuindo, encontramos strings sem nenhuma relação, com relação a southkorea com 48. Podemos partir então de que o valor minimo dessaa relação é 47

Então, vamos criar uma função que faça todo o trabalho acima e mais do que isso, também nos permita substituir southkorea por south korea.

```python
import pandas as pd
import numpy as np
import fuzzywuzzy
from fuzzywuzzy import process
import chardet

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\pakistan_intellectual_capital.csv')

np.random.seed(0)

def replace_matches(df,column,string_to_match,min_ratio=47):

    #Ajustando padrão dos dados para minusculas e sem espaços em brancos no começo e final
    df[column]=df[column].str.lower()
    df[column]=df[column].str.strip()
    
    #criando um data frame para usar o fuzzywuzzy
    strings=df[column].unique()

    #Cria a lista que mostrei no código anterior
    matches=fuzzywuzzy.process.extract(string_to_match, strings, limit=10, scorer=fuzzywuzzy.fuzz.token_sort_ratio)

    #Adiciona em uma váriavel os matches, os resultados do fuzzywuzzy próximo do valor pré-definido
    close_matches = [matches[0] for matches in matches if matches[1] >= min_ratio]

    #Seleciona as linhas com esses matches
    rows_with_matches = df[column].isin(close_matches)

    #Substitui southkorea por shouth korea
    df.loc[rows_with_matches, column] = string_to_match

    print("Pronto")

replace_matches(df=dados,column='Country',string_to_match='south korea')

country=dados['Country'].unique()
print(sorted(country))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2033.png)

## **Machine Learning - Int**

### **Decision Tree**

- Arquivos
    
    [melb_data.csv](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/melb_data.csv)
    

Bom, vamos tentar trazer, primeiramente, uma ideia do que é Machine Learning. Basicamente, é um método de análise de dados que busca automatizar modelos analíticos, uma ideia de que as máquinas podem aprender com o algoritmo, sendo basicamente uma vertente da inteligência artificial.

Aqui, não chegaremos tão longe quanto inteligência artifical mas veremos um modelo para usarmos previsão e o modelo que usaremos se chama “Decision Tree”.

Basicamente, teremos diversas variaveis e baseadas nelas, quando tivermos x tipos de informação, o modelo conseguirá prever o que desejamos

Ex visual de uma “Decision Tree”:

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2034.png)

Bom, nos arquivos que enviei podemos ver que são relacionados a casas, pode ser de uma imobiliária, de um corretor, um especulador, enfim. Com isso temos uma idéia, devemos tentar prever o preço de casas de acordo com algumas variáveis, então vamos lá!

Nesse caso, estamos apenas mostrando a ideia de um primeiro modelo, não vamos trabalhar esses dados de forma profunda

```python
import pandas as pd

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\melb_data.csv')

dados=dados.dropna()

print(dados)
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2035.png)

Vamos definir o que queremos prever, ou seja, o preço. Ela deverá ser armazenada na variável Y enquanto os demais itens que vão compor a previsão, aqueles que podem ter algum tipo de relevância para o que estamos fazendo, deve estar presente na variável X

```python
import pandas as pd
from sklearn.tree import DecisionTreeRegressor

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\melb_data.csv')

dados=dados.dropna()

print(dados)

y=dados['Price']

x=pd.concat((dados['Rooms'],dados['Bathroom'],dados['Landsize'],dados['Lattitude'],dados['Longtitude']),axis=1)

print(x)
print(y)

Arv=DecisionTreeRegressor(random_state=1)
Arv.fit(x,y)
print(Arv)

print("previsão de 5 casas")
print(x.head())
print('Previsões:')
print(Arv.predict(x.head()))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2036.png)

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2037.png)

Bom, na realidade esse primeiro modelo tem a função de mostrar como estruturar o modelo em sí. Ainda não estamos prevendo mas agora já temos uma pequena base em como fazer isso

- **Define:** What type of model will it be? A decision tree? Some other type of model? Some other parameters of the model type are specified too.
- **Fit:** Capture patterns from provided data. This is the heart of modeling.
- **Predict:** Just what it sounds like
- **Evaluate**: Determine how accurate the model's predictions are.

### **Validação de modelo**

Quase todos os modelos de previsão que for montado, vamos querer que ele seja preciso (óbvio), a medida relevante da qualidade do modelo é a precisão preditiva, basicamente, se as previsões do modelo vão estar próximas do que realmente acontece.

Um erro comum, importante de ser mencionado, é que muitas pessoas fazem a validação usando os valores que estamos buscando, é confuso, mas logo mais vai ficar mais claro

A várias formas de fazer essa mensuração, uma delas é usando a Média do Erro Absuluto, ou Mean Absolute Errot (MAE)

```python
import pandas as pd
from sklearn.metrics import mean_absolute_error
from sklearn.tree import DecisionTreeRegressor

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\melb_data.csv')

dados=dados.dropna()

print(dados)

y=dados['Price']

x=pd.concat((dados['Rooms'],dados['Bathroom'],dados['Landsize'],dados['BuildingArea'],dados['YearBuilt'],dados['Lattitude'],dados['Longtitude']),axis=1)

print(x)
print(y)

arv=DecisionTreeRegressor()
arv.fit(x,y)

#######Calculo do Mean Absolute Error

previsao=arv.predict(x)
print(previsao)
print(mean_absolute_error(y,previsao))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2038.png)

Bom, por esse teste temos um modelo de grande qualidade, afinal, o erro está em algo próximo de apenas 500 dólares. Esse tipo de modelo é chamado de modelo “In-Sample”, porém temos um problema!

Usamos uma única amostra de dados para avaliar esse modelo, uma única amostra tanto para construir o modelo quanto para avaliá-lo

Imagine que, no grande mercado imobiliário, a cor da porta não tem relação com o preço da casa.

No entanto, na amostra de dados que você usou para construir o modelo, todas as casas com portas verdes eram muito caras. O trabalho do modelo é encontrar padrões que prevejam os preços das casas, para que ele veja esse padrão e sempre preveja preços altos para casas com portas verdes.

Como esse padrão foi derivado dos dados de treinamento, o modelo parecerá preciso nos dados de treinamento.

Mas se esse padrão não se mantiver quando o modelo vir novos dados, o modelo será muito impreciso quando usado na prática.

Como o valor prático dos modelos vem de fazer previsões em novos dados, medimos o desempenho em dados que não foram usados para construir o modelo. A maneira mais direta de fazer isso é excluir alguns dados do processo de construção do modelo e usá-los para testar a precisão do modelo em dados que ele não viu antes. Esses dados são chamados de dados de validação.

Para verificarmos isso, vamos usar uma função da sklern.model_selection chamada train_test_split. A função dela é quebrar os dados em 2 pedaços e uma parte será usada para treinar o modelo e a outra para calcular a MAE

```python
import pandas as pd
from sklearn.metrics import mean_absolute_error
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import train_test_split

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\melb_data.csv')

dados=dados.dropna()

print(dados)

y=dados['Price']

x=pd.concat((dados['Rooms'],dados['Bathroom'],dados['Landsize'],dados['BuildingArea'],dados['YearBuilt'],dados['Lattitude'],dados['Longtitude']),axis=1)

print(x)
print(y)

train_x,val_x,train_y,val_y=train_test_split(x,y, random_state=0)

arv=DecisionTreeRegressor()
arv.fit(train_x,train_y)

#######Calculo do Mean Absolute Error

previsao=arv.predict(val_x)
print(previsao)
print(mean_absolute_error(val_y,previsao))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2039.png)

Pois bem, esse tipo de modelo que fizemos agora se chama modelo “Out-of-Sample”, vemos agora o valor no final e conseguimos perceber que o modelo não estava tão correto assim, ou seja, no modelo in-sample o erro era de 500 dólares enquanto agora é mais de 25000, uma grande diferença já que trabalhamos os dados e incluimos de forma que servisse como um novo dado para validar o modelo.

Então, legal comentar, uma casa de um milhão de dólares teria uma taxa de erro de 250000, ou seja, quase um quarto do seu valor

### **Over e Under**

Basicamente, overfitting e underfitting são contrários um do outro, se você souber inglês, já deve ter uma mínima ideia do que isso quer dizer

**Overfitting**

Imagine que você montou seu banco de dados e seu modelo de machine learning, a medida que a arvore vai se aprofundando, mais “folhas” são geradas. Bom, isso teoricamente é bom pq as características das casas seriam extremamente abrangidas e os valores ficariam próximos da realidade pelos treinos mas, quando novos dados fossem entrar, a validação seria pobre pois teríamos muitos poucos valores dentro de cada folha

**Underfitting**

Pelo lado contrário, se dividirmos em poucos grupos, teríamos uma grande número de casas dentro de cada grupo, mas, por termos poucos grupos, possivelmente não teríamos como estimar os valores corretamente pois muitas caracteristicas seriam ignoradas pelo modelo

### **Floresta Aleatória/Random Forest**

A ideia de árvore vem diretamente das Decision Trees, afinal, se tivermos uma árvore com muitas ou com poucas folhas, podemos ter resultados que não serão interessantes para nós, como já explicado mais acima.

Bom, o que são as Random Forests? Bom, ela usamuitas árvores e faz a previsão calculando a média de previsão de cada árvore, o que geralmente leva a ter modelos melhores

```python
import pandas as pd
from sklearn.metrics import mean_absolute_error
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor

dados=pd.read_csv('C:\\Users\\lucas\\Downloads\\melb_data.csv')

dados=dados.dropna()

print(dados)

y=dados['Price']

x=pd.concat((dados['Rooms'],dados['Bathroom'],dados['Landsize'],dados['BuildingArea'],dados['YearBuilt'],dados['Lattitude'],dados['Longtitude']),axis=1)

print(x)
print(y)

train_x,val_x,train_y,val_y=train_test_split(x,y, random_state=0)

arv=DecisionTreeRegressor()
arv.fit(train_x,train_y)

previsao=arv.predict(val_x)
print(previsao)
print(mean_absolute_error(val_y,previsao))

#Floresta aleatória

forest_model = RandomForestRegressor(random_state=1)
forest_model.fit(train_x, train_y)
melb_preds = forest_model.predict(val_x)
print(mean_absolute_error(val_y, melb_preds))
```

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2040.png)

![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2041.png)

Bom, podemos ver que o resultado do modelo anterior era de 261724 aproximadamente, usando as árvores, temos um erro menor, agora sendo de aproximadamente 191700, uma grande evolução

## **Deep Learning**

### **O que é Deep Learning**

Alguns dos avanços mais impressionantes em inteligência artificial nos últimos anos foram no campo do aprendizado profundo. Tradução de linguagem natural, reconhecimento de imagem e jogabilidade são tarefas em que os modelos de aprendizado profundo se aproximaram ou até superaram o desempenho em nível humano.

Então, o que é aprendizado profundo? O aprendizado profundo é uma abordagem de aprendizado de máquina caracterizada por pilhas profundas de cálculos. Essa profundidade de computação é o que permitiu que os modelos de aprendizado profundo separassem os tipos de padrões complexos e hierárquicos encontrados nos conjuntos de dados do mundo real mais desafiadores.

Por meio de seu poder e escalabilidade, as redes neurais se tornaram o modelo definidor de aprendizado profundo. As redes neurais são compostas por neurônios, onde cada neurônio realiza individualmente apenas uma simples computação. O poder de uma rede neural vem da complexidade das conexões que esses neurônios podem formar.

- **Unidade Linear**
    
    ![Untitled](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%2042.png)
    
    *Unidade Linear: y = wx+b*
    
    Bom, unidade linear é bem parecido com equações de primeiro grau. A entrada dos dados é X e elas possuem um peso W, ou seja, o que seja ao neurônio (nome dessa figura) é w*x. A rede neural “aprende” modificando seus pesos
    
    O B é um tipo de peso especial chamado viés, ele não possui nenhum dado de entrada, então colocamos 1 e multiplicamos pelo b, confuso? Sim, mas tente se orientar pela imagem, acho que é possivel ficar mais claro.Por fim, o y é o valor que o neurônio finalmente produz
    

## **Dash - Plotly**

### **Básico**

- **O que é Dash py?**
    
    Dash é uma biblioteca de python, o foco dela é, como podemos imaginar pelo nome, criar visuais interativos para os dados com os quais você estiver trabalhando. 
    
    Ela busca fazer isso em um servidor offline, é interessante a analise dessa lib, pois é uma grande facilitadora. Caso não tivessemos ela, seria necessário a utilização de alguma lib para criar uma estrutura e de outra para criação de um servidor, por fim combinar com java.
    
- **Componentes e instalação**
    
    Dash possui 3 bibliotecas distintas: dash (que como j´a citamos ´e uma extens˜ao do Servidor Web), core (seus elementos principais) e html (como o nome diz são as tags HTML que utilizaremos para
    estruturar nosso Dashboard).
    
    ```python
    import dash
    import dash_core_components as dcc
    import dash_html_components as html
    ```
    
    - Primeiro programa
        
        Bom, tendo isso em mente, vamos ver como seria um primeiro programa de Dash
        
- **Layout e tratamentos de dados**
- **Callbacks simples**

### **Intermediário**

- **Aplicação de gráficos**
    - Tipos de gráficos
    - Componentes dos gráficos
- **Callbacks avançados e Dropdown**
- **Mais sobre layout e Div’s (Bootstrap)**

## **Engenharia de Dados - Sua jornada**

## **GitHub, Poetry e PIPX**

### PIPX:

pip é do próprio python, é uma ferramenta bem estável mas que as novidades demoram para chegar no pip

```python
$ pipx install NOME DO PACOTE
```

### Git:

Apagar todas as pastas:

```powershell
pip freeze | Where-Object { $_ -notmatch "^-e" } | Set-Content packages.txt
pip uninstall -y (Get-Content packages.txt)
Remove-Item packages.txt

```

Criar pasta:

```jsx
$ mkdir Nome_Pasta
```

Acessar pasta:

```jsx
$ cd Nome_Pasta
```

Instalar Versão do python

```jsx
$ pyenv install x.xx.x
```

Criar ambiente Virtual:

```python
$ python -m venv Nome_Ambiente

#por padrão:#

$ python -m venv .venv
```

Para ativar o ambiente virtual:

```python
$ source .venv/Scripts/activate
```

para Desativar:

```python
$ deactivate
```

para voltar a pasta anterior:

```python
$ cd ..
```

Para remover um diretório:

```python
$ rm -r Nome_diretório
```

### Poetry:

Logo na tela inicial do Bash:

```python
lucas.brecht@LFNTBSPITP115 MINGW64
$ poetry config virtualenvs.in-project true
```

Para criar a pasta:

```python
$ poetry new nome pasta
```

Definindo a versão python

```python
$ pyenv local x.xx.x
```

Dizendo ao poetry qual versão usar:

```python
$ poetry env use x.xx.x
#Ele cria automaticamente a pasta do venv após esse comando
```

E para instalar pacotes:

```python
$ poetry add xxx
```

## **Docker**

## CHAT GPT

## 📦 O que é Docker?

**Docker** é uma plataforma que permite criar, implantar e executar aplicações em **containers** — ambientes isolados que empacotam uma aplicação com todas as suas dependências, bibliotecas e configurações.

## ✅ Vantagens do Docker

- Portabilidade (roda em qualquer sistema com Docker instalado)
- Facilidade de versionamento de ambientes
- Consistência entre ambientes de desenvolvimento, teste e produção
- Isolamento de aplicações
- Automatização com Dockerfiles e Compose

## 🚀 Como instalar o Docker

## Windows

1. Baixe o **Docker Desktop**:
    
    👉 https://www.docker.com/products/docker-desktop
    
2. Instale e reinicie o sistema, se necessário.
3. Habilite a **virtualização** no BIOS, se for solicitado.
4. Docker CLI pode ser acessado via terminal (PowerShell, CMD, ou WSL).

## macOS

1. Baixe o Docker Desktop para Mac:
    
    👉 https://www.docker.com/products/docker-desktop
    
2. Instale normalmente (arraste o ícone para “Aplicações”).
3. Pode usar via terminal (Terminal.app ou iTerm).

## Linux (Ubuntu/Debian)

```bash
bash
CopiarEditar
sudo apt update
sudo apt install -y \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

# Adiciona chave GPG
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

# Adiciona o repositório
echo \
  "deb [arch=$(dpkg --print-architecture) \
  signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Instala o Docker Engine
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Habilita uso do Docker sem sudo
sudo usermod -aG docker $USER
newgrp docker

```

## ⚙️ Principais comandos do Docker

### Containers

```bash
bash
CopiarEditar
docker run hello-world                      # Roda container de teste
docker run -it ubuntu bash                 # Abre shell bash em Ubuntu
docker ps                                  # Lista containers em execução
docker ps -a                               # Lista todos os containers
docker stop <container_id>                # Para container
docker rm <container_id>                  # Remove container

```

### Imagens

```bash
bash
CopiarEditar
docker images                              # Lista imagens locais
docker pull python:3.10                    # Baixa imagem do Python
docker rmi <image_id>                      # Remove imagem

```

### Dockerfile

Crie um arquivo `Dockerfile`:

```
Dockerfile
CopiarEditar
FROM python:3.10

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

CMD ["python", "main.py"]

```

### Build e run com Dockerfile

```bash
bash
CopiarEditar
docker build -t minha-app .
docker run minha-app

```

### Volumes (para persistência)

```bash
bash
CopiarEditar
docker run -v /meu/diretorio:/app -it python bash

```

## 🧰 Docker Compose

Docker Compose é uma ferramenta para orquestrar múltiplos containers com um arquivo YAML.

### Exemplo: `docker-compose.yml`

```yaml
yaml
CopiarEditar
version: '3.8'

services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/app
    depends_on:
      - redis

  redis:
    image: redis:alpine

```

Comandos:

```bash
bash
CopiarEditar
docker-compose up        # Sobe os containers
docker-compose down      # Derruba os containers

```

## 🐍 Integração com Python

## 1. Criando containers para rodar scripts Python

Com um Dockerfile como este:

```
Dockerfile
CopiarEditar
FROM python:3.10-slim

WORKDIR /app
COPY . .

RUN pip install -r requirements.txt

CMD ["python", "script.py"]

```

Você consegue rodar:

```bash
bash
CopiarEditar
docker build -t meu-script-python .
docker run meu-script-python

```

## 2. Usando bibliotecas Python para se comunicar com o Docker

### Usando `docker-py`

```bash
bash
CopiarEditar
pip install docker

```

```python
python
CopiarEditar
import docker

client = docker.from_env()

# Lista containers
for container in client.containers.list(all=True):
    print(container.name, container.status)

# Roda container com imagem Python
container = client.containers.run("python:3.10", "echo hello from container", remove=True)

```

## 3. Criando APIs Python (FastAPI, Flask) e empacotando com Docker

```
Dockerfile
CopiarEditar
FROM python:3.10

WORKDIR /app
COPY . .

RUN pip install fastapi uvicorn

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

```

## 4. Com Jupyter Notebook

Rodar Jupyter dentro do container:

```bash
bash
CopiarEditar
docker run -p 8888:8888 -v $PWD:/app -w /app jupyter/base-notebook

```

Ou criar seu próprio Dockerfile com o Jupyter:

```
Dockerfile
CopiarEditar
FROM python:3.10

RUN pip install notebook pandas matplotlib

WORKDIR /app
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--allow-root"]

```

## 🧠 Boas práticas

- Use `.dockerignore` (evita copiar arquivos desnecessários)
- Crie imagens leves (use `python:slim`)
- Sempre fixe as versões de dependências (`requirements.txt`)
- Use **multi-stage builds** para imagens menores
- Use volumes nomeados para persistência de dados

## 📚 Exemplos de uso no mundo real

- Criar ambientes para rodar ETLs Python
- Empacotar notebooks para ciência de dados
- Criar APIs para análises em produção
- Automatizar jobs com containers
- Integração contínua (CI/CD)
- Orquestração com Kubernetes (avançado)

## Alguns códigos

```powershell
# Exemplo 1: Script Python simples em Docker
# Estrutura:
# .
# ├── Dockerfile
# ├── requirements.txt
# └── script.py

# script.py
print("Hello from Docker + Python!")

# requirements.txt
# (vazio, já que esse exemplo não usa libs externas)

# Dockerfile
FROM python:3.10-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "script.py"]

# Exemplo 2: API com FastAPI + Docker
# Estrutura:
# .
# ├── app
# │   └── main.py
# ├── requirements.txt
# └── Dockerfile

# app/main.py
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def root():
    return {"message": "Hello from FastAPI + Docker!"}

# requirements.txt
fastapi
uvicorn

# Dockerfile
FROM python:3.10
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY ./app ./app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

# Exemplo 3: Python + Pandas + SQLite
# Estrutura:
# .
# ├── app.py
# ├── requirements.txt
# └── Dockerfile

# app.py
import pandas as pd
import sqlite3

conn = sqlite3.connect('data.db')
df = pd.DataFrame({"nome": ["Ana", "João"], "idade": [28, 34]})
df.to_sql('pessoas', conn, if_exists='replace', index=False)

resultado = pd.read_sql('SELECT * FROM pessoas', conn)
print(resultado)

# requirements.txt
pandas

# Dockerfile
FROM python:3.10-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "app.py"]

# Exemplo 4: Jupyter Notebook com Docker
# Comando para rodar:
# docker run -p 8888:8888 -v "$PWD":/app -w /app jupyter/base-notebook

# Ou criando seu próprio Dockerfile:
# Dockerfile
FROM python:3.10
RUN pip install notebook pandas matplotlib
WORKDIR /app
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--allow-root"]

# Exemplo 5: Docker Compose com FastAPI + Redis
# Estrutura:
# .
# ├── docker-compose.yml
# ├── app
# │   └── main.py
# └── requirements.txt

# app/main.py
from fastapi import FastAPI
import redis

app = FastAPI()
r = redis.Redis(host='redis', port=6379)

@app.get("/")
def read_root():
    r.incr('visitas')
    return {"visitas": int(r.get('visitas'))}

# requirements.txt
fastapi
uvicorn
redis

# Dockerfile
FROM python:3.10
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY ./app ./app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

# docker-compose.yml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "8000:8000"
    volumes:
      - .:/app
    depends_on:
      - redis

  redis:
    image: redis:alpine

```

## Curso

A idéia do Docker é ser uma virtualização, o Docker surgiu como um complemento a uma maquina virtual, é basicamente, utilizar o computador da melhor forma possível.

![image.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/image.png)

Imagina que temos um Servidor rodando 40 aplicações

Na VM teria que instalar 40 linux, enquanto no Docker você vai ter a engine Docker com o Linux e vai espelhar para todos eles.

![image.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/image%201.png)

Docker já da alguns tutoriais, então já começa com: O que é um container?

Dentro do Container, na aba exec, ele é um “Bash”, funciona da mesma forma e com a mesma lingagem, ls, mkdis, cd, etc, etc…

O Docker hub tem varias imagens e programas prontos, funciona de forma meio parecida que o Git Hub, ele tem o docker pull, docker build, docker run, etc, etc

![image.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/image%202.png)

Ok vamos lá:
No python, elaborei esse código:

```python
import streamlit as st

def hello_world():
    return "Hello, World!"

def main():
    st.write(hello_world())

if __name__ == '__main__':
    main()
```

Apenas lembrando, estou usando o poetry no 3.11.3, preciso comeeçar a fazer git pushs

Agora, se uma outra pessoa fosse utilizar o meu arquivo, ela conseguiria? 

Bom, sim, pelo git, ela faria um git clone do meu respositório, em seguida, teria que seguir uma sequência de passos, coomo pip install pipx, pipx install poetry, poetry add isso, poetry tal coisa aquilo

Bom, será que nenhuma alma caridosa pensou em uma forma de automatizar isso? Pois bem, obviamente que sim

Seguindo o passo a passo da imagem acima (A que tem DockerFile, Code, Image e Container), o código acima é simplesmente, o Code.

No Dockerfile, podemos configurar para que ele puxe TUDO isso que usamos para desenvolver essa aplicação, com essa linha abaixo:

```docker
FROM python:3.11.3
RUN pip install poetry
COPY . /src
WORKDIR /src
RUN poetry install 
EXPOSE 8501
ENTRYPOINT [ "poetry", "run", "streamlit", "run", "app/app.py", "--server.port=8501", "--server.aaddress=0.0.0.0" ]
```

No próprio Docker, temos como se fosse uma “biblioteca” que puxa o python e a versão que está usando, quando ele for executado, automaticamente vai dar o pip install necessário (desde que você defina). 

O terceiro, o Copy, ele copia todo o conteúdo da pasta e joga na pasta source do Docker que estamos criando, é como se fosse um linux já com uma pasta source, com todo o código + o python, funcionando da melhor forma possível

O WorkDir não entendi muito bem, mas o código geralmente vai abrir na pasta raiz do Docker, configurando dessa forma, ele vai abrir na pasta source (não sei o pq isso é bom ou ruim)

Run poetry install para ele instalar as bibliotecas do poetry

O Docker, o container vai fechar para todos, vai retirar do mundo a execução do meu código, configurando o EXPOSE 8501, ele vai permitir que consiga acessar essa aplicação pela porta 8501

A última linha, basicamente, estou dizendo pra ele executar essa linha de código do python:

```python
poetry run streamlit run app.py
```

Dizendo qual porta vai ser acessada e qual o endereço do servidor, como é o servidor local, então é o 0.0.0.0

Agora vamos buildar a imagem, entenda o build como se fosse um Zip

```docker
docker build -t minha-primeira-imagem
```

Com isso, a imagem é criada. Ela é meio pesada, nessa execução ele vai bauxar todo o python, todo o poetry, as bibliotecas junto ao projeto, etc,etc,etc

Com isso tendo sido rodado, ele já vai aparecer no Docker Desktop

![image.png](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/image%203.png)

Ok, recebemos a imagem, mas com haviamos falado, a imagem é como se fosse um Zip, como isso vira um container? 

Executando esse código:

```docker
$ docker run -d -p 8501:8501 --name meu-primeiro-container minha-primeira-imagem

```

-d significa deatachment, basicamente, pra ele rodar em segundo plano pra não prender o terminal

-p significa porta, meio que é a forma dele conversar com a aplicação, o streamlit configuramos pra 8501 ser a porta pra acessarmos ele, no docker image dizemos qual porta precisa ficar aberta para o mundo, aqui é quando abrimos ela

—name definimos o nome do container

Em seguida passamos o nome da imagem

Para criar um Docker Compose, que nada mais é do que várias imagens de docker para criar um container, ou seja, mais de uma imagem por container

No exemplo abaixo, temos um caso para criarmos um Docker Compose com o Postgres e Pgadmin

```docker
version: '3'

services:
  teste-postgres-compose:
    image: postgres
    environment:
      POSTGRES_PASSWORD: "Postgres2019!"
    ports:
      - "15432:5432"
    volumes:
      - /home/renatogroffe/Desenvolvimento/Docker-Compose/PostgreSQL:/var/lib/postgresql/data 
    networks:
      - postgres-compose-network
      
  teste-pgadmin-compose:
    image: dpage/pgadmin4
    environment:
      PGADMIN_DEFAULT_EMAIL: "renatogroff@yahoo.com.br"
      PGADMIN_DEFAULT_PASSWORD: "PgAdmin2019!"
    ports:
      - "16543:80"
    depends_on:
      - teste-postgres-compose
    networks:
      - postgres-compose-network

networks: 
  postgres-compose-network:
    driver: bridge
```

## **Airflow**

O Apache Airflow é uma plataforma open-source que permite criar, agendar e monitorar workflows de dados programaticamente. É amplamente utilizado para orquestrar processos complexos de ETL (Extract, Transform, Load), pipelines de dados e outras operações automatizadas.

- **1.** **Documentação Oficial**
    
    A documentação do Apache Airflow é extensa e cobre diversos aspectos, incluindo:
    
    - **Instalação e Configuração**: Como instalar o Airflow em diferentes ambientes (local, Docker, Kubernetes) e configurar as dependências.
    - **Conceitos Básicos**: Introdução aos principais conceitos como DAGs (Directed Acyclic Graphs), Tasks, Operadores, e Schedulers.
    - **Referência de API**: Detalhamento das funções, classes e módulos disponíveis para uso.
    - **Tutoriais e Exemplos**: Passo a passo para criar seus primeiros workflows e exemplos de casos de uso comuns.
    - **Guia de Desenvolvimento**: Como contribuir para o projeto, estender funcionalidades e trabalhar com o código-fonte do Airflow.
    
    Você pode acessar a documentação oficial [aqui](https://airflow.apache.org/docs/).
    
- **2.** **Funcionalidades Principais**
    - **DAGs (Directed Acyclic Graphs)**: A estrutura central do Airflow, representando workflows. Cada DAG é composto por uma coleção de tarefas organizadas em uma sequência específica.
    - **Operadores**: Componentes que executam tarefas específicas dentro dos DAGs. Existem operadores para várias funções, como execução de scripts Python, operações em bancos de dados, interações com APIs, etc.
    - **Tarefas e Dependências**: As tarefas dentro de um DAG podem ser dependentes umas das outras. O Airflow garante que as dependências sejam respeitadas e executadas na ordem correta.
    - **Scheduler**: O componente responsável por monitorar os DAGs e acionar a execução das tarefas conforme programado.
    - **UI Web**: Uma interface web amigável para visualizar DAGs, monitorar a execução de tarefas, ver logs e depurar erros.
    - **Plugins e Extensões**: O Airflow é altamente extensível, permitindo a adição de operadores personalizados, sensores, hooks, etc.
    - **Logs e Monitoramento**: Logs detalhados e recursos de monitoramento integrados para acompanhar o estado de execução dos workflows.
- **3. Formas de Uso**
    - **Criação de DAGs**: Você pode criar DAGs utilizando Python. O código define as tarefas e as relações de dependência entre elas.
    - **Agendamento de Workflows**: Workflows podem ser agendados para serem executados em intervalos regulares, como diariamente, semanalmente, ou em horários específicos.
    - **Integração com Outros Sistemas**: O Airflow pode se integrar com vários sistemas, como bancos de dados, serviços de nuvem (AWS, GCP), ferramentas de Big Data (Hadoop, Spark), e muito mais.
    - **Execução Local e em Produção**: O Airflow pode ser executado tanto em ambiente local para desenvolvimento quanto em clusters distribuídos para processamento em larga escala.
- **Exemplos de Casos de Uso**
    - **Pipeline de ETL**: Extração de dados de um banco de dados, transformação em um formato adequado, e carregamento em um data warehouse.
    - **Orquestração de Processos de Machine Learning**: Automação de fluxos de trabalho de treinamento, validação e implantação de modelos de ML.
    - **Automação de Processos de Negócio**: Agendamento e execução de processos críticos de negócios, como geração de relatórios ou sincronização de dados entre sistemas.
- **Exemplos Práticos**
    
    Vou te fornecer alguns exemplos práticos em Python para criar e agendar workflows (DAGs) no Apache Airflow. Isso inclui a criação de uma DAG simples, a definição de tarefas, operadores básicos e a configuração de dependências.
    
    ### 1. **Instalação do Airflow**
    
    Antes de tudo, você precisa instalar o Apache Airflow. Aqui está o comando para instalar o Airflow utilizando o pip:
    
    ```bash
    pip install apache-airflow
    
    ```
    
    ### 2. **Exemplo 1: Criando uma DAG Simples**
    
    Neste exemplo, vamos criar uma DAG simples que executa três tarefas sequenciais: a primeira imprime uma mensagem, a segunda dorme por 5 segundos e a terceira imprime outra mensagem.
    
    ```python
    from airflow import DAG
    from airflow.operators.python_operator import PythonOperator
    from datetime import datetime, timedelta
    
    # Funções Python que serão executadas como tarefas
    def print_start():
        print("Iniciando o processo...")
    
    def sleep_for_a_while():
        import time
        time.sleep(5)
    
    def print_end():
        print("Processo concluído!")
    
    # Configurações padrão da DAG
    default_args = {
        'owner': 'airflow',
        'depends_on_past': False,
        'start_date': datetime(2024, 8, 20),
        'email_on_failure': False,
        'email_on_retry': False,
        'retries': 1,
        'retry_delay': timedelta(minutes=5),
    }
    
    # Definindo a DAG
    with DAG(
        'exemplo_dag_simples',
        default_args=default_args,
        description='Uma DAG simples com três tarefas',
        schedule_interval=timedelta(days=1),
        catchup=False
    ) as dag:
    
        # Tarefas
        start_task = PythonOperator(
            task_id='print_start',
            python_callable=print_start,
        )
    
        sleep_task = PythonOperator(
            task_id='sleep_for_a_while',
            python_callable=sleep_for_a_while,
        )
    
        end_task = PythonOperator(
            task_id='print_end',
            python_callable=print_end,
        )
    
        # Definindo a sequência de execução
        start_task >> sleep_task >> end_task
    
    ```
    
    ### 3. **Exemplo 2: Utilizando BashOperator**
    
    Agora, vamos criar uma DAG que utiliza o `BashOperator` para executar comandos do shell.
    
    ```python
    from airflow import DAG
    from airflow.operators.bash_operator import BashOperator
    from datetime import datetime, timedelta
    
    default_args = {
        'owner': 'airflow',
        'depends_on_past': False,
        'start_date': datetime(2024, 8, 20),
        'email_on_failure': False,
        'email_on_retry': False,
        'retries': 1,
        'retry_delay': timedelta(minutes=5),
    }
    
    with DAG(
        'exemplo_bash_operator',
        default_args=default_args,
        description='Uma DAG que usa BashOperator',
        schedule_interval=timedelta(days=1),
        catchup=False
    ) as dag:
    
        # Tarefa que imprime a data atual
        print_date_task = BashOperator(
            task_id='print_date',
            bash_command='date',
        )
    
        # Tarefa que dorme por 10 segundos
        sleep_task = BashOperator(
            task_id='sleep',
            bash_command='sleep 10',
        )
    
        # Tarefa que imprime "Airflow é legal!"
        echo_task = BashOperator(
            task_id='echo',
            bash_command='echo "Airflow é legal!"',
        )
    
        # Definindo a sequência de execução
        print_date_task >> sleep_task >> echo_task
    
    ```
    
    ### 4. **Exemplo 3: Transferência de Dados Entre Tarefas**
    
    Neste exemplo, vamos transferir dados de uma tarefa para outra utilizando o `XComs` do Airflow. A primeira tarefa gera um valor e a segunda tarefa o utiliza.
    
    ```python
    from airflow import DAG
    from airflow.operators.python_operator import PythonOperator
    from datetime import datetime, timedelta
    
    def generate_data(**kwargs):
        value = 42
        kwargs['ti'].xcom_push(key='my_value', value=value)
    
    def consume_data(**kwargs):
        ti = kwargs['ti']
        value = ti.xcom_pull(key='my_value', task_ids='generate_data_task')
        print(f"O valor recebido foi: {value}")
    
    default_args = {
        'owner': 'airflow',
        'depends_on_past': False,
        'start_date': datetime(2024, 8, 20),
        'email_on_failure': False,
        'email_on_retry': False,
        'retries': 1,
        'retry_delay': timedelta(minutes=5),
    }
    
    with DAG(
        'exemplo_xcoms',
        default_args=default_args,
        description='Uma DAG que usa XComs para passar dados entre tarefas',
        schedule_interval=timedelta(days=1),
        catchup=False
    ) as dag:
    
        generate_data_task = PythonOperator(
            task_id='generate_data_task',
            python_callable=generate_data,
            provide_context=True,
        )
    
        consume_data_task = PythonOperator(
            task_id='consume_data_task',
            python_callable=consume_data,
            provide_context=True,
        )
    
        generate_data_task >> consume_data_task
    
    ```
    
    ### Como Executar
    
    1. Salve os códigos acima em arquivos `.py` dentro da pasta de DAGs configurada no Airflow (geralmente `~/airflow/dags`).
    2. Acesse a interface web do Airflow (`http://localhost:8080` por padrão).
    3. Ative e execute as DAGs criadas. Você verá as tarefas sendo executadas conforme programado.
    
    Esses exemplos fornecem uma boa base para entender como criar DAGs no Airflow. Se precisar de mais detalhes ou de exemplos mais complexos, estou à disposição!
    

## **Rest/Fast API**

## **Kafka**

## **Data WareHouse**

## **Streamlit**

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

# **Lean**

Anotações que fiz enquanto fazia a trilha

[view?usp=drivesdk](https://drive.google.com/file/d/1GuiKmSYpoQ6kT8hSQOjJEpXPcwh2H7eW/view?usp=drivesdk)

# **Livros**

- **Data Science do Zero: Primeiras Regras com Python**
    
    [Data Science do Zero - Primeiras Regras com Python.pdf](https://drive.google.com/file/d/1HEMwWnn_qD18-3avsmlKaJIJEm-yxN_o/view?usp=drivesdk)
    
- **R for Data Science (Material em Inglês)**
    
    [R for Data Science.pdf](https://drive.google.com/file/d/1BgMrYIQ-uRlkpEnPmjQ4h3OL6G9IEzK9/view?usp=drivesdk)
    
- **Estatística Pratica para Cientistas de Dados**
    
    [Estatistica Pratica para Cientistas de Dados.pdf](https://drive.google.com/file/d/1ojhaaqa8zU2nEjpCJuaQXNcwbPfp9_gQ/view?usp=drivesdk)
    
- **Gestão de Força de Vendas**
    
    [view?usp=share_link](https://drive.google.com/file/d/1BE6zxZhYeeFVowjWKXmzrX2yF4tqzWRP/view?usp=share_link)
    
- **Administração de Vendas**
    
    [ADMINISTRAÇÃO DE VENDAS - 2ª edição.pdf](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/ADMINISTRAO_DE_VENDAS_-_2_edio.pdf)
    

[](Escolinha%20%F0%9F%AB%95%203ff711aeae3f4f1593cf2585e5e5b498/Untitled%20502ca13295624315b91df25e5a097695.md)