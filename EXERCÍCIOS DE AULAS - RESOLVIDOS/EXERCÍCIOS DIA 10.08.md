# 📚 AULA 1 — LINGUAGENS FORMAIS E GRAMÁTICAS

**Data:** 10/08/2026

---

# 🟦 ATIVIDADE 1 — PREFIXOS E SUFIXOS

Considere a palavra:

`ab`

## ❓ Pergunta

Liste os prefixos e os sufixos da palavra.

## ✅ RESPOSTA

### PREFIXOS

Os prefixos são as partes que começam no início da palavra.

`{ε, a, ab}`

### SUFIXOS

Os sufixos são as partes que terminam no final da palavra.

`{ε, b, ab}`

### 💡 Explicando

- `ε` representa a palavra vazia.
- `a` é prefixo porque começa a palavra.
- `ab` é prefixo porque é a palavra inteira.
- `b` é sufixo porque está no final da palavra.
- `ab` também é sufixo porque a palavra inteira pode ser considerada um sufixo.

---

# 🟦 ATIVIDADE 2 — GRAMÁTICA

Considere:

`G = ({S}, {a}, {S → aS | ε}, S)`

## ❓ Pergunta

Liste 3 palavras que podem ser geradas por essa gramática.

## ✅ RESPOSTA

Uma possibilidade é:

- `ε`
- `a`
- `aa`

### 🔎 Derivação

Para gerar `ε`:

`S → ε`

Para gerar `a`:

`S → aS → aε → a`

Para gerar `aa`:

`S → aS → aaS → aaε → aa`

Então algumas palavras geradas são:

- `ε`
- `a`
- `aa`

Também poderiam ser geradas outras palavras, por exemplo:

- `aaa`
- `aaaa`
- `aaaaa`
- `...`

Isso acontece porque a regra:

`S → aS`

pode ser aplicada várias vezes antes de usar:

`S → ε`

---

# 📖 13. RESUMO PARA PROVA

# 🔤 ALFABETO

`Σ` representa o conjunto de símbolos que podem ser usados.

## Exemplo

`Σ = {a, b}`

Nesse caso, os símbolos do alfabeto são:

- `a`
- `b`

---

# 📝 CADEIA OU PALAVRA

É uma sequência de símbolos que pertencem ao alfabeto.

Por exemplo, considerando:

`Σ = {a, b}`

A sequência:

`ab`

é uma palavra válida porque os dois símbolos pertencem ao alfabeto.

`a ∈ Σ`

`b ∈ Σ`

Portanto:

`ab ∈ Σ*`

---

# ⭕ PALAVRA VAZIA

A palavra vazia é representada por:

`ε`

Ela não possui nenhum símbolo.

Por isso:

`|ε| = 0`

## ⚠️ Atenção

A palavra vazia é uma palavra, mesmo não possuindo símbolos.

Ela não deve ser confundida com o conjunto vazio:

`∅`

Temos:

- `ε` → palavra vazia
- `∅` → conjunto vazio

---

# ⭐ SIGMA*

`Σ*` representa o conjunto de todas as cadeias finitas que podem ser formadas usando os símbolos de `Σ`.

Também inclui a palavra vazia.

## Exemplo

Se:

`Σ = {a, b}`

Então:

`Σ* = {ε, a, b, aa, ab, ba, bb, aaa, aab, ...}`

## 💡 Importante

O símbolo `*` significa que podemos formar palavras de diferentes tamanhos, incluindo tamanho `0`.

Por isso:

`ε ∈ Σ*`

---

# 🌐 LINGUAGEM

Uma linguagem é um conjunto de cadeias.

Podemos representar por:

`L ⊆ Σ*`

Isso significa que todas as palavras da linguagem pertencem a `Σ*`.

## Exemplo

Considere:

`Σ = {a, b}`

Uma possível linguagem é:

`L = {a, ab, abb, abbb}`

Nesse caso:

`L ⊆ Σ*`

porque todas as palavras de `L` são formadas usando apenas símbolos de `Σ`.

---

# 🔵 PREFIXO

Prefixo é uma parte da palavra que começa no primeiro símbolo.

Considerando:

`ab`

Os prefixos são:

`{ε, a, ab}`

## Exemplos

- `ε` é o prefixo vazio.
- `a` é prefixo porque começa no primeiro símbolo.
- `ab` é prefixo porque é a palavra inteira.

## 🧠 Regra para lembrar

> **PREFIXO → começa no início da palavra.**

---

# 🟢 SUFIXO

Sufixo é uma parte da palavra que termina no último símbolo.

Considerando:

`ab`

Os sufixos são:

`{ε, b, ab}`

## Exemplos

- `ε` é o sufixo vazio.
- `b` está no final da palavra.
- `ab` é sufixo porque é a palavra inteira.

## 🧠 Regra para lembrar

> **SUFIXO → termina no final da palavra.**

---

# 🧠 PREFIXO × SUFIXO

Para a palavra:

`ab`

Temos:

| Tipo | Conjunto |
|---|---|
| Prefixos | `{ε, a, ab}` |
| Sufixos | `{ε, b, ab}` |

## 💡 Forma fácil de lembrar

`PREFIXO → olha o começo`

`SUFIXO → olha o final`

---

# ⚙️ GRAMÁTICA

Uma gramática é usada para definir regras que permitem gerar palavras de uma linguagem.

Um exemplo é:

`S → aS | ε`

Nesse caso, podemos começar com `S` e ir aplicando as regras até chegar em uma palavra formada somente por símbolos terminais.

## Exemplo

`S → aS → aaS → aaaS → aaaε → aaa`

Portanto:

`aaa`

é uma palavra gerada pela gramática.

---

# ➡️ SÍMBOLO `→`

Nas gramáticas, o símbolo:

`→`

indica uma produção ou regra de produção.

Por exemplo:

`S → aS`

Podemos ler como:

> "S produz aS"

ou:

> "S pode ser substituído por aS".

## Exemplo de aplicação

Se temos:

`S → aS`

e começamos com:

`S`

podemos fazer:

`S → aS`

---

# 🔀 SÍMBOLO `|`

Nas regras de produção, o símbolo:

`|`

significa **"ou"**.

Por exemplo:

`S → aS | ε`

Significa que existem duas possibilidades:

`S → aS`

OU

`S → ε`

## Portanto

A regra:

`S → aS | ε`

pode ser entendida como:

> `S` pode ser substituído por `aS` ou por `ε`.

---

# 🔎 EXEMPLO COMPLETO DA GRAMÁTICA

Considere:

`S → aS | ε`

Podemos escolher:

`S → ε`

Resultado:

`ε`

Ou podemos escolher:

`S → aS`

Depois:

`S → aS → aaS → aaaS → aaaε → aaa`

Também podemos gerar:

- `a`
- `aa`
- `aaa`
- `aaaa`
- `aaaaa`
- `...`

Portanto, essa gramática gera todas as palavras formadas por zero ou mais `a`.

Podemos representar a linguagem gerada por:

`L = {aⁿ | n ≥ 0}`

Ou, usando expressão regular:

`a*`

---

# ⚠️ OBSERVAÇÃO SOBRE O SÍMBOLO `→`

Em outros assuntos da matemática e da lógica, o símbolo:

`→`

pode ter outros significados.

Por exemplo, em lógica pode representar:

> **implica**

ou:

> **se... então**

Mas, quando estamos trabalhando com gramáticas, normalmente estamos usando `→` para indicar uma regra de produção.

## Exemplo

Na gramática:

`S → aS`

o símbolo `→` significa:

> "`S` pode ser substituído por `aS`."

---

# 🧩 ESTRUTURA DE UMA GRAMÁTICA

Uma gramática pode ser representada por:

`G = (V, T, P, S)`

Onde:

| Símbolo | Significado |
|---|---|
| `G` | Gramática |
| `V` | Conjunto de variáveis ou não terminais |
| `T` | Conjunto de terminais |
| `P` | Conjunto de produções |
| `S` | Símbolo inicial |

## Exemplo

`G = ({S}, {a}, {S → aS | ε}, S)`

Nesse exemplo:

`V = {S}`

`T = {a}`

`P = {S → aS | ε}`

`S = símbolo inicial`

---

# 🧠 RESUMO RÁPIDO PARA A PROVA

| Conceito | Significado |
|---|---|
| `Σ` | Alfabeto |
| Palavra | Sequência de símbolos |
| `ε` | Palavra vazia |
| `|ε|` | Comprimento da palavra vazia, igual a 0 |
| `Σ*` | Todas as palavras possíveis |
| `L` | Linguagem |
| `L ⊆ Σ*` | Linguagem formada por palavras de `Σ*` |
| Prefixo | Começa no início |
| Sufixo | Termina no final |
| `G` | Gramática |
| `V` | Variáveis |
| `T` | Terminais |
| `P` | Produções |
| `S` | Símbolo inicial |
| `→` | Regra de produção |
| `|` | OU |
| Derivação | Aplicação das regras para gerar uma palavra |

---

# 🎯 DICAS PARA NÃO CONFUNDIR

- **Alfabeto** → conjunto de símbolos.
- **Palavra** → sequência de símbolos.
- **Linguagem** → conjunto de palavras.
- **Prefixo** → começa no início.
- **Sufixo** → termina no final.
- **ε** → palavra vazia.
- **Σ*** → todas as palavras possíveis.
- **→** → regra de produção.
- **|** → OU.
- **Gramática** → conjunto de regras para gerar palavras.

---

# 🏆 EXEMPLO FINAL

Considere:

`Σ = {a, b}`

A palavra:

`ab`

possui:

## Prefixos

`{ε, a, ab}`

## Sufixos

`{ε, b, ab}`

Como `a` e `b` pertencem ao alfabeto:

`a ∈ Σ`

`b ∈ Σ`

a palavra:

`ab`

pertence a:

`Σ*`

Se tivermos a gramática:

`S → aS | ε`

podemos gerar:

- `ε`
- `a`
- `aa`
- `aaa`
- `aaaa`
- `aaaaa`
- `...`

Portanto, a ideia principal da aula é:

> **Um alfabeto possui símbolos. Símbolos formam palavras. Palavras formam linguagens. Gramáticas utilizam regras para gerar palavras.**

---

# 🚀 RESUMÃO

| Conceito | O que significa |
|---|---|
| `Σ` | Alfabeto |
| `a`, `b`, `0`, `1` | Símbolos |
| `ab` | Palavra |
| `ε` | Palavra vazia |
| `Σ*` | Todas as palavras possíveis |
| `L` | Linguagem |
| `L ⊆ Σ*` | Linguagem formada por palavras de `Σ*` |
| Prefixo | Parte que começa no início |
| Sufixo | Parte que termina no final |
| `G` | Gramática |
| `V` | Variáveis |
| `T` | Terminais |
| `P` | Produções |
| `S` | Símbolo inicial |
| `→` | Regra de produção |
| `|` | OU |
| Derivação | Aplicação das regras para gerar uma palavra |

---

# 📌 FRASES PARA DECORAR

> **Alfabeto → símbolos → palavras → linguagens.**

> **Gramática → regras → derivações → palavras.**
```
