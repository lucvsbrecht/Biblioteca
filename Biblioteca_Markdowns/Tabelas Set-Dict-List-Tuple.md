
---

| Característica         | `set`                                   | `list`                  | `dict`                         | `tuple`                                  |
| ---------------------- | --------------------------------------- | ----------------------- | ------------------------------ | ---------------------------------------- |
| **Ordenação**          | ❌ Não                                   | ✅ Sim                   | ✅ Sim (desde Python 3.7)       | ✅ Sim                                    |
| **Mutável**            | ✅ Sim                                   | ✅ Sim                   | ✅ Sim                          | ❌ Não                                    |
| **Permite duplicatas** | ❌ Não                                   | ✅ Sim                   | ❌ (apenas nas chaves)          | ✅ Sim                                    |
| **Indexado**           | ❌ Não                                   | ✅ Sim (por posição)     | ✅ Sim (por chave)              | ✅ Sim (por posição)                      |
| **Hashável**           | ❌ Não                                   | ❌ Não                   | ❌ Não                          | ✅ Sim (se conter apenas itens imutáveis) |
| **Uso comum**          | Conjuntos únicos, operações matemáticas | Sequências mutáveis     | Pares chave-valor, dicionários | Sequências imutáveis                     |
| **Tipo de acesso**     | Iteração ou pertencimento               | Índices (0, 1, 2...)    | Chaves (`dict["chave"]`)       | Índices (0, 1, 2...)                     |
| **Criação com**        | `{1, 2, 3}` ou `set()`                  | `[1, 2, 3]` ou `list()` | `{"a": 1, "b": 2}` ou `dict()` | `(1, 2, 3)` ou `tuple()`                 |

---
