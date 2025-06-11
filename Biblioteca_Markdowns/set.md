
---

## 📚 `set` em Python – Teoria Profunda + Prática

### 🔍 O que é um `set`?

Um `set` é uma **estrutura de dados baseada em conjuntos da matemática**, ou seja, uma coleção **não ordenada**, **sem elementos duplicados** e **mutável**.

```python
meu_set = {1, 2, 3}
```

> Ideal para armazenar itens **únicos**, fazer testes de **pertença** e realizar **operações de conjuntos** (união, interseção, etc.).

---

## 🧠 Fundamentos Teóricos

### ⚙️ Como o `set` funciona internamente?

* `sets` são **implementados como tabelas hash** (assim como chaves de dicionários).
* Cada item precisa ser **hashable** (imutável e com função `__hash__()` válida).
* O Python calcula o hash de cada item e o armazena em uma **estrutura desordenada**, que permite **busca e inserção rápidas (O(1))**.

---

### ⚠️ Características principais

| Atributo         | Valor                                                                  |
| ---------------- | ---------------------------------------------------------------------- |
| Ordenada         | ❌ Não (não garante ordem)                                              |
| Mutável          | ✅ Sim                                                                  |
| Elementos únicos | ✅ Sim                                                                  |
| Indexável        | ❌ Não (não suporta índices)                                            |
| Hashável         | ❌ Não (sets são mutáveis, logo não são hashables, mas `frozenset` sim) |

---

## 🛠 Como criar um `set`

```python
# Com chaves
s1 = {1, 2, 3}

# Com função set()
s2 = set([1, 2, 2, 3, 3])
print(s2)  # {1, 2, 3}

# Set vazio
s3 = set()
```

⚠️ Atenção: `{}` cria um dicionário, não um `set`. Para um set vazio, use `set()`.

---

## 🎯 Principais operações e métodos

| Método           | Descrição                               |
| ---------------- | --------------------------------------- |
| `.add(elem)`     | Adiciona um elemento                    |
| `.remove(elem)`  | Remove (erro se não existir)            |
| `.discard(elem)` | Remove (sem erro se não existir)        |
| `.clear()`       | Remove todos os elementos               |
| `.copy()`        | Cria uma cópia do set                   |
| `.pop()`         | Remove e retorna um elemento aleatório  |
| `.update(iter)`  | Adiciona múltiplos elementos de uma vez |

```python
numeros = {1, 2, 3}
numeros.add(4)
numeros.discard(2)
print(numeros)  # {1, 3, 4}
```

---

## 🔄 Operações de conjunto

| Operação            | Sintaxe simbólica | Método equivalente          |              |
| ------------------- | ----------------- | --------------------------- | ------------ |
| União               | \`a               | b\`                         | `a.union(b)` |
| Interseção          | `a & b`           | `a.intersection(b)`         |              |
| Diferença           | `a - b`           | `a.difference(b)`           |              |
| Diferença simétrica | `a ^ b`           | `a.symmetric_difference(b)` |              |
| Inclusão total      | `a <= b`          | `a.issubset(b)`             |              |
| Inclusão reversa    | `a >= b`          | `a.issuperset(b)`           |              |
| Disjunção total     | `a.isdisjoint(b)` |                             |              |

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)  # {1, 2, 3, 4, 5}
print(a & b)  # {3}
print(a - b)  # {1, 2}
print(a ^ b)  # {1, 2, 4, 5}
```

---

## 🧾 Comparativo com outras estruturas

| Tipo    | Permite repetição | Mantém ordem  | Mutável | Indexável                |
| ------- | ----------------- | ------------- | ------- | ------------------------ |
| `list`  | ✅                 | ✅             | ✅       | ✅                        |
| `tuple` | ✅                 | ✅             | ❌       | ✅                        |
| `dict`  | ❌ (chaves únicas) | ✅ (desde 3.7) | ✅       | ❌ (mas acessa por chave) |
| `set`   | ❌                 | ❌             | ✅       | ❌                        |

---

## 🎓 Casos de uso ideais

* **Remover duplicatas** de uma lista:

  ```python
  nomes = ["Ana", "João", "Ana", "Carlos"]
  nomes_unicos = list(set(nomes))  # ['Carlos', 'Ana', 'João']
  ```

* **Verificar pertinência** com alta performance:

  ```python
  permitidos = {"pdf", "jpg", "png"}
  if "exe" in permitidos:
      print("Permitido")
  else:
      print("Bloqueado")
  ```

* **Comparar conjuntos** de permissões, acessos, usuários, etc.

---

## 🔐 `frozenset`: o set imutável

O `frozenset` é uma variante **imutável e hashável** do `set`:

```python
fs = frozenset([1, 2, 3])
# fs.add(4)  # ❌ Erro
```

Use `frozenset` quando precisar usar um conjunto como **chave em dicionários**, ou como **membro de outro set**.

---

## 🧪 Exemplos práticos reais

### 1. **Remoção de duplicatas**

```python
emails = ["a@x.com", "b@x.com", "a@x.com"]
emails_unicos = list(set(emails))
```

### 2. **Tags únicas de produtos**

```python
tags = set()
tags.update(["promoção", "verão"])
tags.update(["verão", "oferta"])
print(tags)  # {'promoção', 'oferta', 'verão'}
```

### 3. **Verificar interseção entre grupos**

```python
grupo_a = {"Ana", "João", "Carlos"}
grupo_b = {"João", "Maria"}

comuns = grupo_a & grupo_b  # {'João'}
```

---

## 📈 Complexidade das operações

| Operação               | Complexidade |
| ---------------------- | ------------ |
| Inserção               | `O(1)`       |
| Remoção                | `O(1)`       |
| Teste de pertencimento | `O(1)`       |
| União/interseção       | `O(n)`       |

---

## 📌 Conclusão teórica

O tipo `set` é ideal quando:

✅ Você quer **evitar duplicatas**
✅ Precisa de **verificações rápidas** (`in`)
✅ Vai realizar **operações de conjuntos**
✅ Precisa economizar memória em comparação com `list`

⚠️ Mas: **não serve para armazenar dados ordenados ou indexados**

---

