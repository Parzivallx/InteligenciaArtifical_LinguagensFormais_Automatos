
# 📚 EXERCÍCIOS — LINGUAGENS FORMAIS E AUTÔMATOS

> Material de estudo com exercícios resolvidos sobre **alfabetos, palavras, linguagens, gramáticas e derivações**.

---

# 🟦 EXERCÍCIO 1 — ALFABETO

Considere:

```text
Σ = {a, b, c}
````

 ## Perguntas

 1. Quantos símbolos existem no alfabeto?
2. Quais são os símbolos?
3. O símbolo `a` pertence ao alfabeto?
4. O símbolo `d` pertence ao alfabeto?
5. Escreva uma palavra formada por símbolos desse alfabeto.

 ## ✅ Respostas

 ### 1\. Quantos símbolos existem no alfabeto?

 Existem **3 símbolos** no alfabeto.

 ### 2\. Quais são os símbolos?

```
a, b, c
```

 ### 3\. O símbolo `a` pertence ao alfabeto?

 ✅ **Sim**, porque:

```
a ∈ Σ
```

 ### 4\. O símbolo `d` pertence ao alfabeto?

 ❌ **Não**, porque:

```
d ∉ Σ
```

 ### 5\. Escreva uma palavra formada por símbolos desse alfabeto

 Exemplos:

```
a
aa
ab
b
bb
ba
abc
```

---

 # 🟦 EXERCÍCIO 2 — PALAVRAS SOBRE UM ALFABETO

 Considere:

```
Σ = {0, 1}
```

 Classifique cada sequência como **PALAVRA VÁLIDA** ou **NÃO VÁLIDA**.

 | Sequência | Classificação | Explicação |
| --- | --- | --- |
| `0101` | ✅ VÁLIDA | Todos os símbolos são `0` ou `1`. |
| `00110` | ✅ VÁLIDA | Todos os símbolos pertencem a `Σ`. |
| `012` | ❌ NÃO VÁLIDA | O símbolo `2` não pertence a `Σ`. |
| `111` | ✅ VÁLIDA | Todos os símbolos pertencem a `Σ`. |
| `10a` | ❌ NÃO VÁLIDA | O símbolo `a` não pertence a `Σ`. |

 ## 💡 Explicação

 A palavra `0101` é válida porque todos os seus símbolos pertencem ao alfabeto:

```
0 ∈ Σ
1 ∈ Σ
0 ∈ Σ
1 ∈ Σ
```

 Já `012` não é válida porque:

```
2 ∉ Σ
```

---

 # 🟦 EXERCÍCIO 3 — PERTINÊNCIA DE SÍMBOLOS E PALAVRAS

 Considere:

```
Σ = {0, 1}
```

 Determine se as afirmações são **VERDADEIRAS** ou **FALSAS**.

 | Afirmação | Resultado | Explicação |
| --- | --- | --- |
| `0 ∈ Σ` | ✅ VERDADEIRO | `0` está no alfabeto. |
| `1 ∈ Σ` | ✅ VERDADEIRO | `1` está no alfabeto. |
| `01 ∈ Σ` | ❌ FALSO | `01` é uma sequência de dois símbolos. |
| `01 ∈ Σ*` | ✅ VERDADEIRO | `01` é uma palavra formada por símbolos de `Σ`. |
| `2 ∈ Σ` | ❌ FALSO | `2` não pertence ao alfabeto. |
| `101 ∈ Σ*` | ✅ VERDADEIRO | `101` é formada somente por `0` e `1`. |

 ## ⚠️ Atenção

 É importante diferenciar:

```
Σ   → conjunto de símbolos

Σ*  → conjunto de todas as palavras formadas por esses símbolos
```

 Por exemplo:

```
0 ∈ Σ

01 ∉ Σ

01 ∈ Σ*
```

---

 # 🟦 EXERCÍCIO 4 — LINGUAGEM

 Considere:

```
L = {0, 01, 011, 0111}
```

 Determine se cada palavra pertence à linguagem.

 | Palavra | Pertence a `L`? |
| --- | --- |
| `0` | ✅ SIM |
| `01` | ✅ SIM |
| `0111` | ✅ SIM |
| `10` | ❌ NÃO |
| `111` | ❌ NÃO |
| `011` | ✅ SIM |

 ## 💡 Explicação

 Uma palavra pertence à linguagem quando ela está presente no conjunto `L`.

 Por exemplo:

```
011 ∈ L
```

 porque `011` aparece em `L`.

 Já:

```
10 ∉ L
```

 porque `10` não aparece em `L`.

---

 # 🟦 EXERCÍCIO 5 — DESCREVENDO UMA LINGUAGEM POR PADRÃO

 Considere:

```
L = {bⁿ | n ≥ 1}
```

 ## 1\. Escreva as cinco primeiras palavras

```
b
bb
bbb
bbbb
bbbbb
```

 ## 2\. Explique o significado de `bⁿ`

 `bⁿ` significa que temos `n` símbolos `b` juntos.

 Exemplos:

```
b¹ = b
b² = bb
b³ = bbb
b⁴ = bbbb
```

 ## 3\. A palavra `bbbbbb` pertence à linguagem?

 ✅ **SIM.**

 A palavra possui 6 símbolos `b`:

```
bbbbbb = b⁶
```

 Como:

```
6 ≥ 1
```

 então:

```
bbbbbb ∈ L
```

 ## 4\. A palavra vazia `ε` pertence à linguagem?

 ❌ **NÃO.**

 A palavra vazia possui comprimento `0`:

```
|ε| = 0
```

 Mas a condição da linguagem é:

```
n ≥ 1
```

 Portanto:

```
ε ∉ L
```

---

 # 🟦 EXERCÍCIO 6 — LINGUAGEM VAZIA E PALAVRA VAZIA

 Explique a diferença entre:

 ## A) Conjunto vazio

```
L = ∅
```

 Nesse caso, a linguagem **não possui nenhuma palavra**.

 ## B) Linguagem contendo a palavra vazia

```
L = {ε}
```

 Nesse caso, a linguagem possui **uma palavra**, que é a palavra vazia.

 ## ✅ Respostas

 | Pergunta | Resposta |
| --- | --- |
| Qual delas possui uma palavra? | `{ε}` |
| Qual delas não possui nenhuma palavra? | `∅` |
| Qual é o comprimento da palavra `ε`? | `0` |

 ## ⚠️ Muito importante

 Não confunda:

```
∅
```

 com:

```
{ε}
```

 São coisas diferentes.

```
∅     → não possui nenhuma palavra

{ε}   → possui uma palavra: ε
```

 E:

```
|ε| = 0
```

---

 # 🟦 EXERCÍCIO 7 — ESTRUTURA DE UMA GRAMÁTICA

 Considere:

```
G = ({S, A}, {0, 1}, P, S)
```

 com:

```
P = {S → 0A, A → 1}
```

 ## 1\. Conjunto de variáveis

```
V = {S, A}
```

 ## 2\. Conjunto de terminais

```
T = {0, 1}
```

 ## 3\. Conjunto de produções

```
P = {S → 0A, A → 1}
```

 ## 4\. Símbolo inicial

```
S
```

 ## 5\. Qual palavra pode ser gerada?

 A palavra gerada é:

```
01
```

 ## Derivação

```
S
→ 0A
→ 01
```

 Portanto:

```
01 ∈ L(G)
```

---

 # 🟦 EXERCÍCIO 8 — COMO APLICAR UMA PRODUÇÃO

 Considere:

```
S → 0S
```

 Começando com `S`:

 ## 1\. Aplique a regra uma vez

```
S
→ 0S
```

 ## 2\. Aplique a regra duas vezes

```
S
→ 0S
→ 00S
```

 ## 3\. Aplique a regra três vezes

```
S
→ 0S
→ 00S
→ 000S
```

 ## 4\. Escreva a sequência completa de derivação

```
S
→ 0S
→ 00S
→ 000S
```

 ## ⚠️ Observação

 A derivação ainda **não terminou**, porque o símbolo `S` continua aparecendo.

 Enquanto houver uma variável na sentença, ainda podemos aplicar uma produção.

---

 # 🟦 EXERCÍCIO 9 — DERIVAÇÃO COMPLETA DE UMA PALAVRA

 Utilizando a gramática:

```
S → aS
S → b
```

 Gere:

```
aaab
```

 ## Derivação

 Começando pelo símbolo inicial `S`:

```
S
→ aS
→ aaS
→ aaaS
```

 Agora utilizamos a regra:

```
S → b
```

 Então:

```
aaaS
→ aaab
```

 ## ✅ Derivação completa

```
S
→ aS
→ aaS
→ aaaS
→ aaab
```

 Portanto:

```
aaab ∈ L(G)
```

---

 # 🟦 EXERCÍCIO 10 — IDENTIFICANDO PALAVRAS GERADAS POR UMA GRAMÁTICA

 Considere:

```
S → 0S
S → 1
```

 Determine se cada palavra pode ser gerada.

 | Palavra | Pode ser gerada? |
| --- | --- |
| `1` | ✅ SIM |
| `01` | ✅ SIM |
| `001` | ✅ SIM |
| `0001` | ✅ SIM |
| `101` | ❌ NÃO |
| `1001` | ❌ NÃO |

 ## 1\. Palavra `1`

 ✅ **PODE SER GERADA**

```
S
→ 1
```

 ## 2\. Palavra `01`

 ✅ **PODE SER GERADA**

```
S
→ 0S
→ 01
```

 ## 3\. Palavra `001`

 ✅ **PODE SER GERADA**

```
S
→ 0S
→ 00S
→ 001
```

 ## 4\. Palavra `0001`

 ✅ **PODE SER GERADA**

```
S
→ 0S
→ 00S
→ 000S
→ 0001
```

 ## 5\. Palavra `101`

 ❌ **NÃO PODE SER GERADA**

 A gramática permite colocar vários `0`s antes de um único `1`.

 Exemplos:

```
1
01
001
0001
```

 Quando utilizamos:

```
S → 1
```

 a derivação termina.

 Por isso não é possível gerar:

```
101
```

 ## 6\. Palavra `1001`

 ❌ **NÃO PODE SER GERADA**

 O padrão dessa gramática é:

```
000...001
```

 Ou seja:

 > Zero ou mais `0`s seguidos de exatamente um `1`.

---

 # 🏆 DESAFIO FINAL

 Considere:

```
S → aS
S → b
```

 ## 1\. A palavra `b` pode ser gerada?

 ✅ **SIM**

```
S
→ b
```

---

 ## 2\. A palavra `ab` pode ser gerada?

 ✅ **SIM**

```
S
→ aS
→ ab
```

---

 ## 3\. A palavra `aab` pode ser gerada?

 ✅ **SIM**

```
S
→ aS
→ aaS
→ aab
```

---

 ## 4\. A palavra `aaab` pode ser gerada?

 ✅ **SIM**

```
S
→ aS
→ aaS
→ aaaS
→ aaab
```

---

 ## 5\. A palavra `aba` pode ser gerada?

 ❌ **NÃO**

 A regra:

```
S → b
```

 é utilizada para finalizar a derivação.

 Depois que `b` é produzido, não existe outra regra para continuar a derivação.

 Portanto:

```
aba ∉ L(G)
```

---

 ## 6\. Derivação completa de `aaaab`

```
S
→ aS
→ aaS
→ aaaS
→ aaaaS
→ aaaab
```

 Portanto:

```
aaaab ∈ L(G)
```

---

 ## 7\. Descreva o padrão das palavras geradas

 A gramática:

```
S → aS
S → b
```

 gera **zero ou mais letras `a`, seguidas de exatamente uma letra `b`**.

 Alguns exemplos:

```
b
ab
aab
aaab
aaaab
aaaaab
```

 O padrão pode ser representado por:

```
aⁿb, n ≥ 0
```

 Também podemos representar o mesmo padrão usando uma expressão regular:

```
a*b
```

---

 # 📖 RESUMO DOS CONCEITOS

 | Conceito | Significado |
| --- | --- |
| `Σ` | Alfabeto, conjunto de símbolos |
| **Símbolo** | Elemento individual do alfabeto |
| **Palavra** | Sequência finita de símbolos |
| **Linguagem** | Conjunto de palavras |
| `Σ*` | Todas as palavras possíveis sobre `Σ`, incluindo `ε` |
| `ε` | Palavra vazia |
| `∅` | Conjunto vazio |
| `w ∈ L` | A palavra `w` pertence à linguagem `L` |
| `w ∉ L` | A palavra `w` não pertence à linguagem `L` |
| `G` | Gramática |
| `V` | Variáveis ou não terminais |
| `T` | Terminais |
| `P` | Produções ou regras |
| `S` | Símbolo inicial |
| `→` | Regra de produção |
| **Derivação** | Processo de aplicação das regras da gramática |

---

 # 🧠 MAPA MENTAL

```
LINGUAGENS FORMAIS
│
├── ALFABETO (Σ)
│   └── Conjunto de símbolos
│
├── PALAVRA
│   └── Sequência de símbolos
│
├── LINGUAGEM (L)
│   └── Conjunto de palavras
│
├── Σ*
│   └── Todas as palavras possíveis
│       └── Inclui ε
│
├── ε
│   └── Palavra vazia
│       └── |ε| = 0
│
└── GRAMÁTICA (G)
    │
    ├── V → Variáveis
    ├── T → Terminais
    ├── P → Produções
    └── S → Símbolo inicial
```

---

 # 🎯 REGRAS DE OURO PARA A PROVA

 - **Alfabeto (`Σ`)** → conjunto de símbolos.
- **Palavra** → sequência de símbolos.
- **Linguagem (`L`)** → conjunto de palavras.
- **`Σ*`** → todas as palavras possíveis sobre o alfabeto, incluindo `ε`.
- **`ε`** → palavra vazia, com comprimento `0`.
- **`∅`** → conjunto que não possui nenhum elemento.
- **Gramática (`G`)** → conjunto de regras usado para gerar palavras.
- **Derivação** → aplicação das regras da gramática.
- **Variável** → símbolo que ainda pode ser substituído por uma produção.
- **Terminal** → símbolo que aparece na palavra final.
- Uma derivação está completa quando restam **somente terminais**.

---

 # 🚀 RESUMO FINAL

```
Σ
↓
Alfabeto
↓
Símbolos
↓
Formam palavras
↓
Palavras formam linguagens
↓
Gramáticas possuem regras
↓
Regras geram palavras
↓
Derivação mostra como a palavra foi gerada
```

 ## ⭐ Exemplo completo

 Gramática:

```
S → aS
S → b
```

 Gera:

```
b
ab
aab
aaab
aaaab
...
```

 Padrão:

```
aⁿb, n ≥ 0
```

 Expressão regular equivalente:

```
a*b
```

 ### 📌 Ideia principal

 > A gramática começa em `S`, adiciona quantos `a` forem necessários usando `S → aS` e termina obrigatoriamente com `b` usando `S → b`.

```

```
