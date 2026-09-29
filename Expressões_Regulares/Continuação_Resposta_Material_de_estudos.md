# 🧪 10. Atividade prática no Regex Learn — 0,5 ponto

> 🔎 **Objetivo:** verificar, na prática, se a expressão regular desenvolvida para o desafio final atende corretamente a todas as regras da especificação.

---

## 🔤 Expressão utilizada

A expressão utilizada para o desafio final foi:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

A expressão foi testada no **Regex Learn Playground** utilizando os exemplos válidos, inválidos e quatro novos casos de teste.

---

## 🧪 Registro dos testes

| **Entrada** | **Esperado** | **Obtido** | **Regra verificada** |
|:---|:---:|:---:|:---|
| `CCO-2024-0001-M` | ✅ aceita | ✅ aceita | Curso, limite inferior e formato |
| `ESW-2026-1042-N` | ✅ aceita | ✅ aceita | Formato geral |
| `SIS-2029-9999-T` | ✅ aceita | ✅ aceita | Curso, limite superior e formato |
| `CCO-2027-0100-N` | ✅ aceita | ✅ aceita | Formato geral |
| `ESW-2025-4321-M` | ✅ aceita | ✅ aceita | Formato geral |
| `SIS-2028-5678-M` | ✅ aceita | ✅ aceita | Formato geral |
| `CCO-2025-0042-T` | ✅ aceita | ✅ aceita | Formato geral |
| `ADS-2026-0001-N` | ❌ rejeita | ❌ rejeita | Curso |
| `CCO-2030-0001-M` | ❌ rejeita | ❌ rejeita | Ano |
| `SIS-2027-123-N` | ❌ rejeita | ❌ rejeita | Número com três algarismos |
| `esw-2026-1042-N` | ❌ rejeita | ❌ rejeita | Curso em minúsculas |
| `CCO/2026/0001/M` | ❌ rejeita | ❌ rejeita | Separador incorreto |
| `CCO-2026-0001-X` | ❌ rejeita | ❌ rejeita | Turno inexistente |
| `CCO-2026-0001-M-EXTRA` | ❌ rejeita | ❌ rejeita | Caracteres extras |
| `SIS-2024-5678-M` | ✅ aceita | ✅ aceita | 🆕 Limite inferior 2024 |
| `CCO-2029-0001-T` | ✅ aceita | ✅ aceita | 🆕 Limite superior 2029 |
| `ESW-2026-123-N` | ❌ rejeita | ❌ rejeita | 🆕 Caso quase correto |
| `SIS-2028-5678-M-EXTRA` | ❌ rejeita | ❌ rejeita | 🆕 Caracteres extras |

---

## 🧩 Justificativa por blocos

A expressão pode ser dividida em partes para facilitar a compreensão:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

| **Bloco** | **Função** |
|:---|:---|
| `(CCO\|ESW\|SIS)` | 🎓 Permite os cursos CCO, ESW e SIS |
| `202[4-9]` | 📅 Permite os anos de 2024 a 2029 |
| `[0-9]{4}` | 🔢 Exige exatamente quatro algarismos |
| `(M\|T\|N)` | 🌙 Permite os turnos M, T ou N |
| `-` | ➖ Separa os blocos da matrícula |
| `^` | 🔰 Indica o início da cadeia |
| `$` | 🛑 Indica o fim da cadeia |

### 🔍 Entendendo a estrutura

```text
^(CCO|ESW|SIS) - 202[4-9] - [0-9]{4} - (M|T|N)$
       ↓              ↓          ↓           ↓
     Curso            Ano      Número       Turno
```

Dessa forma, cada parte da Regex corresponde diretamente a uma regra definida para o código de matrícula.

---

## 📊 Resultado da validação

Os testes realizados apresentaram os resultados esperados:

- ✅ Os exemplos válidos foram aceitos.
- ❌ Os exemplos inválidos foram rejeitados.
- 📅 Os limites de ano `2024` e `2029` foram validados.
- 🔢 O número foi limitado a exatamente quatro algarismos.
- 🎓 Apenas os cursos `CCO`, `ESW` e `SIS` foram aceitos.
- 🌙 Apenas os turnos `M`, `T` e `N` foram aceitos.
- 🚫 Caracteres extras foram rejeitados.
- ⚠️ Casos quase corretos também foram rejeitados corretamente.

---

## 📝 Conclusão

Depois de realizar os testes, foi possível verificar que a Regex funciona de acordo com as regras definidas para o código de matrícula.

Os exemplos válidos foram aceitos e os inválidos foram rejeitados, incluindo os testes com os anos de **2024** e **2029**, um caso quase correto e outro com **caracteres extras**.

Assim, a expressão:

```text
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$
```

representa corretamente o formato:

**CURSO - ANO - NÚMERO - TURNO**






# 🧠 11. Perguntas de Reflexão

---

## 1️⃣ Toda expressão regular formal representa uma linguagem regular?

**Sim.** Na teoria, uma expressão regular é usada justamente para representar uma linguagem regular.

---

## 2️⃣ Toda linguagem regular pode ser representada por uma expressão regular?

**Sim.** Toda linguagem regular pode ser descrita por alguma expressão regular equivalente.

---

## 3️⃣ Qual é a relação entre uma ER, um NFA e um DFA?

Os três conseguem representar as mesmas **linguagens regulares**.

Uma expressão regular pode ser transformada em um **NFA**, e o NFA pode ser transformado em um **DFA**.

```text
Expressão Regular (ER)
          ↓
         NFA
          ↓
         DFA
```

Apesar de serem modelos diferentes, os três possuem o mesmo poder de reconhecimento para linguagens regulares.

---

## 4️⃣ Qual é a diferença entre uma expressão regular teórica e as extensões de motores de programação?

A **expressão regular teórica** segue as regras estudadas na teoria de linguagens formais.

Já as **Regex utilizadas em programas** podem possuir recursos extras, como:

- 🔹 Grupos de captura
- 🔹 Lookahead
- 🔹 Lookbehind
- 🔹 Referências
- 🔹 Outras extensões específicas de cada motor

Esses recursos não fazem parte da definição básica de expressão regular estudada na teoria.

---

## 5️⃣ Por que um autômato finito reconhece paridade, mas não consegue contar arbitrariamente e comparar duas quantidades sem limite?

Porque um autômato finito possui apenas uma **quantidade limitada de estados**.

Ele consegue controlar situações simples, como saber se a quantidade de símbolos é **par ou ímpar**, porque precisa apenas manter poucas informações.

Porém, não consegue guardar uma quantidade qualquer de símbolos para comparar posteriormente.

> 💡 **Exemplo:** ele consegue identificar se a quantidade de `a` é par ou ímpar, mas não consegue guardar exatamente quantos `a` apareceram para depois comparar com a quantidade de `b`.

---

## 6️⃣ Por que `{aⁿbⁿ | n ≥ 0}` não é regular?

Porque é necessário contar os `a` e depois verificar se a quantidade de `b` é **exatamente a mesma**.

Como um autômato finito possui memória limitada, ele não consegue fazer essa comparação para qualquer valor de `n`.

```text
aaa → 3 símbolos a
bbb → 3 símbolos b

Quantidade igual ✅
```

O problema aparece quando `n` pode crescer indefinidamente, pois seria necessário guardar essa quantidade para fazer a comparação.

---

## 7️⃣ O que muda ao passarmos de linguagens regulares para linguagens livres de contexto?

A principal diferença é que as **linguagens livres de contexto** podem utilizar uma **pilha como memória**.

Isso permite resolver problemas que os autômatos finitos não conseguem, como verificar se a quantidade de `a` é igual à quantidade de `b` em:

```text
{aⁿbⁿ | n ≥ 0}
```

De forma simplificada:

```text
Linguagem Regular
       ↓
Autômato Finito
       ↓
Memória limitada


Linguagem Livre de Contexto
       ↓
Autômato com Pilha
       ↓
Memória por meio de uma pilha
```

---

# 📝 Síntese

De forma simples, as **linguagens livres de contexto** conseguem lidar com situações que precisam de mais memória.

No caso de `{aⁿbⁿ}`, é preciso guardar quantos `a` foram lidos para depois comparar com os `b`.

Um **DFA** não consegue fazer isso porque possui apenas uma quantidade limitada de estados.

Já um modelo com **pilha** consegue armazenar essa informação durante a leitura e utilizá-la posteriormente para realizar a comparação.

> 🎯 **Em resumo:** linguagens regulares trabalham com memória limitada, enquanto linguagens livres de contexto conseguem resolver problemas que exigem uma forma adicional de memória, como uma pilha.
