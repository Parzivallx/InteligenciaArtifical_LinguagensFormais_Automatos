# 📚 8. Exercício Guiado

Antes de escrever a expressão, siga estes passos:

1. Defina o alfabeto.
2. Separe a palavra em blocos.
3. Identifique escolhas e repetições.
4. Crie exemplos válidos e inválidos.
5. Escreva a expressão.

---

## 🔹 Exercício 1 — Sufixo `00`

Sobre **Σ = {0, 1}**, construa uma ER para todas as palavras que terminam em `00`.

### ✏️ Expressão

    ^[01]*00$

### 💡 Explicação

| Parte | Significado |
| --- | --- |
| `[01]*` | Qualquer quantidade de `0` e `1` |
| `00` | Garante que a palavra termina em `00` |
| `^` | Início da cadeia |
| `$` | Fim da cadeia |

---

## 🔹 Exercício 2 — Exatamente dois `a`

Sobre **Σ = {a, b}**, construa uma ER para palavras que possuem exatamente dois símbolos `a` e qualquer quantidade de `b`.

### ✏️ Expressão

    ^b*ab*ab*$

### 💡 Explicação

A estrutura da expressão é:

    b*  a  b*  a  b*

| Parte | Significado |
| --- | --- |
| `b*` | Qualquer quantidade de `b` |
| `a` | Primeiro `a` |
| `b*` | Qualquer quantidade de `b` |
| `a` | Segundo `a` |
| `b*` | Qualquer quantidade de `b` |

Dessa forma, a palavra possui exatamente dois `a`.

---

## 🔹 Exercício 3 — Identificador Acadêmico

O identificador deve:

- começar com duas letras maiúsculas;
- possuir três algarismos;
- terminar opcionalmente com uma letra minúscula;
- não possuir caracteres extras.

### ✏️ Expressão

    ^[A-Z]{2}[0-9]{3}[a-z]?$

### 💡 Explicação

| Parte | Significado |
| --- | --- |
| `[A-Z]{2}` | Exatamente duas letras maiúsculas |
| `[0-9]{3}` | Exatamente três algarismos |
| `[a-z]?` | Uma letra minúscula opcional |
| `^` | Início da cadeia |
| `$` | Fim da cadeia |

### ✅ Exemplos

| Exemplo | Resultado |
| --- | --- |
| `AB123` | ✅ |
| `XY456a` | ✅ |
| `A123` | ❌ |
| `ABC123` | ❌ |
| `AB12` | ❌ |
| `ab123` | ❌ |

---

# 🏆 9. Desafio Final — Código de Matrícula

## 📋 Formato

    CURSO-ANO-NÚMERO-TURNO

## 📌 Regras

- **CURSO:** CCO, ESW ou SIS;
- **ANO:** de 2024 a 2029;
- **NÚMERO:** exatamente quatro algarismos;
- **TURNO:** M, T ou N;
- os blocos são separados por `-`;
- não são permitidos caracteres extras.

---

## 🔎 Regex

    ^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$

---

## 🧩 Estrutura

    (CCO|ESW|SIS) - 202[4-9] - [0-9]{4} - (M|T|N)
           ↓              ↓            ↓          ↓
         Curso            Ano        Número      Turno

---

## 🔤 Conjuntos

    C = {CCO, ESW, SIS}

    A = {2024, 2025, 2026, 2027, 2028, 2029}

    D = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}

    T = {M, T, N}

A linguagem é:

    L = {c-a-d₁d₂d₃d₄-t | c ∈ C, a ∈ A, dᵢ ∈ D, t ∈ T}

---

## 🧩 Explicação da Regex

### 1. Curso

    (CCO|ESW|SIS)

Permite somente:

    CCO
    ESW
    SIS

O operador `|` representa alternativas.

---

### 2. Ano

    202[4-9]

Permite somente os anos de 2024 até 2029.

---

### 3. Número

    [0-9]{4}

Exige exatamente quatro algarismos.

`{4}` exige exatamente quatro ocorrências, enquanto `+` significa uma ou mais ocorrências.

---

### 4. Turno

    (M|T|N)

Permite somente:

    M
    T
    N

---

### 5. Âncoras

    ^
    $

Garantem que a Regex valide a cadeia inteira.

Assim, caracteres extras não são aceitos.

---

## ✅ Exemplos Válidos

| Código | Resultado |
| --- | --- |
| `CCO-2024-0001-M` | ✅ |
| `ESW-2026-1042-N` | ✅ |
| `SIS-2029-9999-T` | ✅ |
| `CCO-2027-0100-N` | ✅ |
| `ESW-2025-4321-M` | ✅ |
| `SIS-2028-5678-M` | ✅ |
| `CCO-2025-0042-T` | ✅ |

---

## ❌ Exemplos Inválidos

| Código | Motivo |
| --- | --- |
| `ADS-2026-0001-N` | Curso inexistente |
| `CCO-2030-0001-M` | Ano fora do intervalo |
| `SIS-2027-123-N` | Número com três algarismos |
| `esw-2026-1042-N` | Curso em minúsculas |
| `CCO/2026/0001/M` | Separador incorreto |
| `CCO-2026-0001-X` | Turno inexistente |
| `CCO-2026-0001-M-EXTRA` | Caracteres extras |

---

## 📝 Novos Casos

### ✅ Válidos

    SIS-2028-5678-M

    CCO-2025-0042-T

### ❌ Inválidos

    ESW-2023-1234-M

Ano fora do intervalo.

    SIS-2026-12345-N

Número possui cinco algarismos.

---

## ❓ Perguntas para Justificar

### 1. Qual parte representa a escolha entre os cursos?

    (CCO|ESW|SIS)

O operador `|` representa as alternativas possíveis.

---

### 2. Como o ano foi limitado?

    202[4-9]

Essa expressão permite somente os anos de 2024 a 2029.

---

### 3. Por que usar `{4}`?

    [0-9]{4}

Porque o número deve possuir exatamente quatro algarismos.

---

### 4. Qual é a função de `^` e `$`?

    ^
    $

Eles garantem que a Regex valide a cadeia inteira, impedindo caracteres extras.

---

### 5. A Regex permite uma matrícula fora das regras?

Não.

Ela limita:

- o curso;
- o ano;
- a quantidade de algarismos;
- o turno;
- os separadores;
- o início e o fim da cadeia.

---

# 🤖 Desafio Extra — DFA Equivalente

O DFA lê a matrícula da esquerda para a direita, verificando cada bloco na ordem.

## 🔄 Estados

| Estado | Função |
| --- | --- |
| `q0` | Estado inicial |
| `q1` | Curso |
| `q2` | Hífen após o curso |
| `q3` | Ano |
| `q4` | Hífen após o ano |
| `q5` | Quatro algarismos do número |
| `q6` | Hífen após o número |
| `q7` | Turno |
| `q8` | Estado de aceitação |
| `qd` | Estado sumidouro |

---

## 🌐 Fluxo Simplificado

    → q0
       │
       │ Curso
       ▼
      q1
       │
       │ -
       ▼
      q2
       │
       │ Ano
       ▼
      q3
       │
       │ -
       ▼
      q4
       │
       │ [0-9]{4}
       ▼
      q5
       │
       │ -
       ▼
      q6
       │
       │ M | T | N
       ▼
      q7
       │
       ▼
      q8 ★

Qualquer símbolo inválido leva ao estado sumidouro:

    qd

O estado `qd` permanece nele mesmo:

    qd → qd

---

## 🧠 Como o DFA Funciona?

### 📌 Curso

Aceita somente:

    CCO
    ESW
    SIS

### 📅 Ano

Aceita:

    2024
    2025
    2026
    2027
    2028
    2029

### 🔢 Número

Exige exatamente quatro algarismos:

    [0-9][0-9][0-9][0-9]

### 🌙 Turno

Aceita:

    M | T | N

### ⭐ Estado de Aceitação

`q8` é o único estado de aceitação.

Se houver qualquer símbolo inválido ou caractere extra, a cadeia vai para `qd`.

---

# ✅ Conclusão

A Regex final é:

    ^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$

Ela representa:

    CURSO - ANO - NÚMERO - TURNO

e garante que todos os requisitos da matrícula sejam respeitados.
