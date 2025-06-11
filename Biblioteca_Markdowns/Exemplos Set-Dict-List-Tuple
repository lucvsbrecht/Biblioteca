
---

### ✅ **1. `set` – Conjunto**

```python
# Criação de um set (sem duplicatas e sem ordem)
frutas = {"maçã", "banana", "laranja", "maçã"}
print(frutas)  # {'banana', 'laranja', 'maçã'}

# Adicionar item
frutas.add("uva")

# Verificar existência
print("banana" in frutas)  # True

# Remover item
frutas.remove("laranja")

# União com outro set
tropicais = {"abacaxi", "banana"}
print(frutas | tropicais)  # união: {'maçã', 'banana', 'uva', 'abacaxi'}
```

> Usado quando você **precisa garantir unicidade** e fazer **operações de conjuntos**.

---

### 📋 **2. `list` – Lista ordenada e mutável**

```python
# Criação de uma lista
numeros = [10, 20, 30, 40]

# Acessar elementos
print(numeros[1])  # 20

# Modificar
numeros[2] = 35

# Adicionar
numeros.append(50)

# Remover
numeros.remove(10)

# Iterar
for n in numeros:
    print(n)
```

> Ideal para **sequências ordenadas** que **podem mudar** (adicionar, remover, etc).

---

### 📚 **3. `dict` – Dicionário com pares chave-valor**

```python
# Criação de dicionário
pessoa = {
    "nome": "Alice",
    "idade": 30,
    "email": "alice@email.com"
}

# Acessar valor por chave
print(pessoa["nome"])  # Alice

# Adicionar ou atualizar valor
pessoa["idade"] = 31
pessoa["cidade"] = "São Paulo"

# Remover item
pessoa.pop("email")

# Iterar por chave e valor
for chave, valor in pessoa.items():
    print(chave, "->", valor)
```

> Usado para armazenar dados **estruturados por nome**, como registros, configurações, objetos, etc.

---

### 🔐 **4. `tuple` – Sequência imutável e ordenada**

```python
# Criação
coordenadas = (10.5, 20.7)

# Acesso por índice
print(coordenadas[0])  # 10.5

# Desempacotamento
x, y = coordenadas
print(f"x={x}, y={y}")

# Tentativa de alteração (vai dar erro)
# coordenadas[0] = 12  # ❌ TypeError
```

> Boa escolha quando **os dados não devem ser alterados**, como **coordenadas, registros fixos, chaves de dicionários**, etc.

---

### 🧾 Resumo final com aplicação ideal

| Tipo    | Quando usar                                                                 |
| ------- | --------------------------------------------------------------------------- |
| `set`   | Quando você **precisa de elementos únicos** e faz **operações de conjunto** |
| `list`  | Quando você precisa de uma **coleção ordenada e mutável**                   |
| `dict`  | Quando os dados têm uma **estrutura de chave-valor**                        |
| `tuple` | Quando a **ordem importa, mas os dados não devem mudar**                    |

