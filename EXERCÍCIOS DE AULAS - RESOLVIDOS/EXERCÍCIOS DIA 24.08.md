# 📚 EXERCÍCIOS PRÁTICOS PARA FIXAÇÃO

---

# 🟦 BLOCO 1 — DERIVAÇÃO

Dada a gramática:

`G1: S → aS | b`

---

## 🅰️ A) Gere a palavra `aaab`.

### ✅ RESPOSTA

Começamos pelo símbolo inicial `S`.

`S`

`→ aS`

`→ aaS`

`→ aaaS`

`→ aaab`

Portanto, a palavra `aaab` pode ser gerada pela gramática.

---

## 🅱️ B) Explique como você sabe que a derivação terminou.

### ✅ RESPOSTA

A derivação terminou porque não aparece mais nenhum símbolo não terminal.

No começo temos o símbolo `S`, que é um não terminal.

Depois de aplicar a regra `S → aS` algumas vezes, usamos a regra `S → b`.

Assim chegamos em:

`aaab`

Nesse ponto só existem símbolos terminais, ou seja, `a` e `b`.

Por isso a derivação terminou.

---

# 🟦 BLOCO 2 — GLC

Dada a gramática:

`G2: S → aSb | ε`

---

## 🅰️ A) Gere a palavra `aaabbb`.

### ✅ RESPOSTA

Começamos com `S`.

`S`

`→ aSb`

`→ aaSbb`

`→ aaaSbbb`

`→ aaabbb`

Para finalizar, usamos:

`S → ε`

Assim, a derivação completa pode ser escrita como:

`S`

`→ aSb`

`→ aaSbb`

`→ aaaSbbb`

`→ aaabbb`

Portanto, a palavra `aaabbb` pode ser gerada.

---

## 🅱️ B) É possível gerar a palavra `aabbb`? Justifique.

### ✅ RESPOSTA

Não, não é possível gerar `aabbb`.

Isso acontece porque a regra:

`S → aSb`

sempre acrescenta um `a` no começo e um `b` no final ao mesmo tempo.

Então a quantidade de `a` e `b` precisa ser igual.

Por exemplo:

`S`

`→ aSb`

`→ aaSbb`

`→ aaaSbbb`

Podemos gerar:

- `ab`
- `aabb`
- `aaabbb`
- `aaaabbbb`
- `...`

Mas não podemos gerar:

`aabbb`

porque essa palavra possui **2 letras `a`** e **3 letras `b`**.

Portanto:

`aabbb ∉ L(G2)`

---

# 🟦 BLOCO 3 — CLASSIFICAÇÃO

Classifique a gramática como **REGULAR** ou **LIVRE DE CONTEXTO**:

`S → aA`

`A → b`

---

## ✅ RESPOSTA

A gramática é **REGULAR**.

Isso porque as produções seguem o formato de uma gramática regular.

Temos:

`S → aA`

e:

`A → b`

Na primeira regra aparece um terminal `a` seguido de um único não terminal `A`.

Na segunda regra aparece apenas o terminal `b`.

A palavra gerada pela gramática é:

`S`

`→ aA`

`→ ab`

Portanto, a gramática é:

**REGULAR**

---

# 📋 RESUMO DAS RESPOSTAS

---

# 🟦 BLOCO 1

### A) `aaab` pode ser gerada.

Derivação:

`S`

`→ aS`

`→ aaS`

`→ aaaS`

`→ aaab`

### B) A derivação termina quando não existem mais símbolos não terminais.

---

# 🟦 BLOCO 2

### A) `aaabbb` pode ser gerada.

Derivação:

`S`

`→ aSb`

`→ aaSbb`

`→ aaaSbbb`

`→ aaabbb`

### B) `aabbb` não pode ser gerada.

A gramática sempre produz a mesma quantidade de `a` e `b`.

---

# 🟦 BLOCO 3

A gramática é:

# ✅ REGULAR

Produções:

`S → aA`

`A → b`

Palavra gerada:

`ab`

---

# 🧠 RESUMO PARA FIXAÇÃO

| Conceito | Explicação |
|---|---|
| **Derivação** | Processo de aplicar as regras da gramática |
| **Símbolo não terminal** | Símbolo que ainda pode ser substituído |
| **Símbolo terminal** | Símbolo que permanece na palavra final |
| **Derivação completa** | Quando não existem mais não terminais |
| **GLC** | Gramática Livre de Contexto |
| **Gramática Regular** | Gramática com produções em formato regular |
| `ε` | Palavra vazia |
| `→` | Regra de produção |
| `|` | OU |

---

# 📌 DICA IMPORTANTE

Para saber se uma **derivação terminou**, procure os símbolos não terminais.

Se ainda existir algo como:

`S`

ou:

`A`

ou:

`B`

a derivação **ainda não terminou**.

Quando restarem somente terminais, como:

`a`, `b`, `0`, `1`

a derivação terminou.

### Exemplo

❌ Ainda não terminou:

`aaSbb`

Porque existe o não terminal `S`.

✅ Terminou:

`aaabbb`

Porque existem somente terminais `a` e `b`.

---

# 🎯 COMO PENSAR NAS DERIVAÇÕES

## Gramática `G1`

`S → aS | b`

O padrão é:

`aⁿb`

com:

`n ≥ 0`

Exemplos:

- `b`
- `ab`
- `aab`
- `aaab`
- `aaaab`
- `...`

---

## Gramática `G2`

`S → aSb | ε`

O padrão é:

`aⁿbⁿ`

com:

`n ≥ 0`

Exemplos:

- `ε`
- `ab`
- `aabb`
- `aaabbb`
- `aaaabbbb`
- `...`

A quantidade de `a` precisa ser igual à quantidade de `b`.

---

# 🔥 DIFERENÇA ENTRE AS DUAS GRAMÁTICAS

| Gramática | Regra | Padrão |
|---|---|---|
| `G1` | `S → aS \| b` | `aⁿb` |
| `G2` | `S → aSb \| ε` | `aⁿbⁿ` |

### G1

Cada aplicação de:

`S → aS`

adiciona somente um `a`.

Depois:

`S → b`

finaliza a palavra.

Exemplo:

`S → aS → aaS → aaaS → aaab`

---

### G2

Cada aplicação de:

`S → aSb`

adiciona simultaneamente:

- um `a` no começo;
- um `b` no final.

Exemplo:

`S → aSb → aaSbb → aaaSbbb → aaabbb`

Por isso:

`G2`

gera palavras com a mesma quantidade de `a` e `b`.

---

# 📚 CONCEITOS IMPORTANTES

## 1. TERMINAL

É um símbolo que aparece na palavra final.

Exemplos:

`a`

`b`

`0`

`1`

---

## 2. NÃO TERMINAL

É um símbolo que pode ser substituído através de uma regra da gramática.

Exemplos:

`S`

`A`

`B`

---

## 3. DERIVAÇÃO

É o processo de aplicar as regras da gramática.

Exemplo:

`S → aS → aaS → aab`

---

## 4. PALAVRA GERADA

Quando a derivação termina e restam somente símbolos terminais.

Exemplo:

`aab`

---

## 5. PALAVRA NÃO GERADA

Quando não existe uma sequência de aplicações das regras capaz de produzir a palavra desejada.

Exemplo:

`aabbb`

para a gramática:

`S → aSb | ε`

---

# 📝 EXEMPLO DE QUESTÃO DE PROVA

Considere:

`G: S → aS | b`

Pergunta:

A palavra `aaaab` pode ser gerada?

### Resolução

Começamos com:

`S`

Aplicamos `S → aS` quatro vezes:

`S`

`→ aS`

`→ aaS`

`→ aaaS`

`→ aaaaS`

Agora usamos:

`S → b`

Então:

`aaaaS`

`→ aaaab`

Portanto:

# ✅ SIM, `aaaab` PODE SER GERADA.

---

# 📝 OUTRO EXEMPLO

Considere:

`G: S → aSb | ε`

Pergunta:

A palavra `aaabb` pode ser gerada?

### Resolução

A palavra possui:

- 3 letras `a`;
- 2 letras `b`.

Mas a gramática sempre adiciona um `a` e um `b` juntos.

Logo, as quantidades precisam ser iguais.

Como:

`3 ≠ 2`

temos:

# ❌ NÃO, `aaabb` NÃO PODE SER GERADA.

---

# 🏆 RESUMÃO FINAL

### G1

`S → aS | b`

Gera:

`b`

`ab`

`aab`

`aaab`

`aaaab`

`...`

Padrão:

`aⁿb`

com:

`n ≥ 0`

---

### G2

`S → aSb | ε`

Gera:

`ε`

`ab`

`aabb`

`aaabbb`

`aaaabbbb`

`...`

Padrão:

`aⁿbⁿ`

com:

`n ≥ 0`

---

# 📌 PARA DECORAR

> **Derivação termina quando não existem mais símbolos não terminais.**

> **G1 adiciona `a` e termina com `b`.**

> **G2 adiciona `a` e `b` ao mesmo tempo.**

> **Na G2, a quantidade de `a` é sempre igual à quantidade de `b`.**

> **Terminal fica. Não terminal é substituído.**
