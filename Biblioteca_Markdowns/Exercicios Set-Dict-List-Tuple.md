
---

## 🧪 Exercícios sobre `set`

### ✅ Teóricos

1. O que acontece quando você tenta adicionar um elemento duplicado em um `set`?
2. Quais operações matemáticas básicas podemos fazer com `sets` em Python?

### 🛠️ Práticos

3. Crie um set com os elementos: `"maçã"`, `"banana"`, `"uva"` e tente adicionar `"maçã"` novamente. Mostre o resultado.
4. Dado:

   ```python
   a = {1, 2, 3}
   b = {3, 4, 5}
   ```

   Realize a **união**, **interseção** e **diferença** entre esses conjuntos.

---

## 📋 Exercícios sobre `list`

### ✅ Teóricos

5. Listas em Python são mutáveis. O que isso significa?
6. Quais métodos você usaria para:

   * Adicionar um elemento no final?
   * Ordenar os elementos?
   * Contar quantas vezes um elemento aparece?

### 🛠️ Práticos

7. Crie uma lista com os números de 1 a 5. Remova o número 3.
8. Inverta essa lista (sem usar `[::-1]`).
9. Some todos os elementos da lista com um loop `for`.

---

## 📚 Exercícios sobre `dict`

### ✅ Teóricos

10. Quais são as duas formas principais de iterar por um dicionário?
11. É possível usar uma lista como chave em um dicionário? Justifique.

### 🛠️ Práticos

12. Crie um dicionário chamado `aluno` com as chaves: `"nome"`, `"idade"` e `"notas"`, sendo esta última uma lista de 3 notas.
13. Calcule a média das notas do dicionário `aluno`.
14. Adicione uma nova chave chamada `"aprovado"` com valor `True` se a média for maior ou igual a 7, caso contrário, `False`.

---

## 🔐 Exercícios sobre `tuple`

### ✅ Teóricos

15. Qual a principal diferença entre uma `tuple` e uma `list`?
16. Em que situação você preferiria usar uma `tuple` ao invés de uma `list`?

### 🛠️ Práticos

17. Crie uma `tuple` com três coordenadas de um ponto 3D: `(x, y, z)`.
18. Desempacote os valores da tupla em três variáveis e imprima-as separadamente.
19. Tente alterar o valor de um dos elementos da tupla (o que acontece?).

---

## ✅ Gabarito das Respostas

### `set`

1. Nada acontece; o elemento duplicado é ignorado.

2. União (`|`), interseção (`&`), diferença (`-`) e diferença simétrica (`^`).

3.

```python
frutas = {"maçã", "banana", "uva"}
frutas.add("maçã")
print(frutas)  # {'maçã', 'banana', 'uva'}
```

4.

```python
print(a | b)  # {1, 2, 3, 4, 5}
print(a & b)  # {3}
print(a - b)  # {1, 2}
```

---

### `list`

5. Significa que seus elementos podem ser modificados (adicionar, remover, reordenar, etc).
6.

* `.append()`
* `.sort()`
* `.count()`

7.

```python
numeros = [1, 2, 3, 4, 5]
numeros.remove(3)  # [1, 2, 4, 5]
```

8.

```python
numeros.reverse()  # [5, 4, 2, 1]
```

9.

```python
soma = 0
for num in numeros:
    soma += num
print(soma)  # 12
```

---

### `dict`

10. `.keys()` e `.items()`

11. Não, porque listas são mutáveis e chaves de dicionários precisam ser imutáveis (hasháveis).

12.

```python
aluno = {
    "nome": "Maria",
    "idade": 17,
    "notas": [8.5, 7.0, 9.0]
}
```

13.

```python
media = sum(aluno["notas"]) / len(aluno["notas"])
```

14.

```python
aluno["aprovado"] = media >= 7
```

---

### `tuple`

15. Tuplas são imutáveis, listas não.

16. Quando você não quer que os dados sejam alterados, como em coordenadas fixas ou dados de configuração.

17.

```python
ponto3d = (1.0, 2.0, 3.0)
```

18.

```python
x, y, z = ponto3d
print(x, y, z)
```

19.

```python
# ponto3d[0] = 5  ❌ TypeError: 'tuple' object does not support item assignment
```

---
