 # 📚 Exercícios Práticos para Fixação

 > Material de revisão sobre **Gramáticas Formais**, **Derivação**, **Gramáticas Livres de Contexto (GLC)** e **Gramáticas Regulares**.

---

 ## 📑 Sumário

 - 🔹 Bloco 1 — Derivação
  - A) Gere a palavra `aaab`
  - B) Explique como você sabe que a derivação terminou
- 🔹 Bloco 2 — GLC
  - A) Gere a palavra `aaabbb`
  - B) É possível gerar a palavra `aabbb`?
- 🔹 Bloco 3 — Classificação
- 📌 Resumo das Respostas
- 🧠 Conceitos Importantes
- 📝 Checklist de Revisão

---

 ## 🔹 BLOCO 1 — DERIVAÇÃO

 Dada a gramática:

```
G1: S -> aS | b
```

 ### A) Gere a palavra `aaab`

 ### Resposta

 Começamos pelo símbolo inicial `S`.

 A derivação é:

```
S
→ aS
→ aaS
→ aaaS
→ aaab
```

 Portanto:

 > **`aaab` pode ser gerada pela gramática G1.** ✅

---

 ### B) Explique como você sabe que a derivação terminou

 ### Resposta

 A derivação terminou porque **não aparece mais nenhum símbolo não terminal**.

 No início temos:

```
S
```

 O símbolo `S` é um **não terminal**.

 Aplicamos a regra:

```
S -> aS
```

 algumas vezes:

```
S
→ aS
→ aaS
→ aaaS
```

 Depois utilizamos:

```
S -> b
```

 Obtendo:

```
aaab
```

 Nesse ponto temos somente símbolos terminais:

```
a a a b
```

 Portanto, a derivação terminou.

 ### 💡 Regra importante

 > Uma derivação termina quando a sentença contém **somente símbolos terminais**.

---

 ## 🔹 BLOCO 2 — GLC

 Dada a gramática:

```
G2: S -> aSb | ε
```

 > **Observação:** `ε` representa a **palavra vazia**.

---

 ### A) Gere a palavra `aaabbb`

 ### Resposta

 Começamos pelo símbolo inicial `S`.

 Aplicamos a produção:

```
S -> aSb
```

 resultando em:

```
S
→ aSb
```

 Aplicamos novamente:

```
S
→ aSb
→ aaSbb
```

 Aplicamos mais uma vez:

```
S
→ aSb
→ aaSbb
→ aaaSbbb
```

 Agora precisamos eliminar o símbolo não terminal `S`.

 Para isso, utilizamos:

```
S -> ε
```

 Assim:

```
S
→ aSb
→ aaSbb
→ aaaSbbb
→ aaabbb
```

 Portanto:

 > **`aaabbb` pode ser gerada pela gramática G2.** ✅

---

 ### B) É possível gerar a palavra `aabbb`?

 ### Resposta

 **Não.** ❌

 A regra:

```
S -> aSb
```

 sempre adiciona:

 - um `a` no início;
- um `b` no final.

 Ou seja, cada aplicação da regra adiciona **um `a` e um `b` ao mesmo tempo**.

 Por exemplo:

```
S
→ aSb
→ aaSbb
→ aaaSbbb
```

 Podemos gerar:

```
ab
aabb
aaabbb
aaaabbbb
```

 Observe que a quantidade de `a` e `b` é sempre igual.

 | Palavra | Quantidade de `a` | Quantidade de `b` |
| --- | --- | --- |
| `ab` | 1 | 1 |
| `aabb` | 2 | 2 |
| `aaabbb` | 3 | 3 |
| `aaaabbbb` | 4 | 4 |

 Agora observe a palavra:

```
aabbb
```

 Ela possui:

 - **2** letras `a`;
- **3** letras `b`.

 Como as quantidades são diferentes, ela não pode ser gerada pela gramática.

 Portanto:

```
aabbb ∉ L(G2)
```

 > **`aabbb` não pertence à linguagem gerada por G2.** ❌

 ### 💡 Padrão da linguagem

 A gramática gera palavras no formato:

```
L(G2) = { aⁿbⁿ | n ≥ 0 }
```

 Alguns exemplos são:

```
ε
ab
aabb
aaabbb
aaaabbbb
aaaaabbbbb
...
```

---

 ## 🔹 BLOCO 3 — CLASSIFICAÇÃO

 Classifique a gramática como **REGULAR** ou **LIVRE DE CONTEXTO**:

```
S -> aA
A -> b
```

---

 ### Resposta

 A gramática é:

 > **REGULAR** 🟢

 Isso acontece porque suas produções seguem o formato de uma **gramática regular**.

 Temos a produção:

```
S -> aA
```

 Nela temos:

 - `a` → símbolo terminal;
- `A` → símbolo não terminal.

 E temos:

```
A -> b
```

 Nessa produção temos apenas um símbolo terminal.

---

 ### 🔄 Derivação

 Podemos verificar a geração da palavra utilizando:

```
S
→ aA
→ ab
```

 Portanto, a palavra gerada é:

```
ab
```

 Logo:

 > **A gramática é REGULAR.** ✅

---

 # 📌 Resumo das Respostas

 | Bloco | Questão | Resposta |
| --- | --- | --- |
| **1** | A | ✅ `aaab` pode ser gerada |
| **1** | B | ✅ A derivação termina quando não existem não terminais |
| **2** | A | ✅ `aaabbb` pode ser gerada |
| **2** | B | ❌ `aabbb` não pode ser gerada |
| **3** | Classificação | 🟢 A gramática é **REGULAR** |

---

 # 🧠 Conceitos Importantes

 ## 🔸 Símbolo Terminal

 Um **terminal** é um símbolo que aparece na palavra final e não precisa mais ser substituído.

 Exemplos:

```
a
b
```

---

 ## 🔸 Símbolo Não Terminal

 Um **não terminal** é um símbolo utilizado durante a derivação e que pode ser substituído através de uma produção.

 Exemplos:

```
S
A
```

---

 ## 🔸 Produção

 Uma **produção** é uma regra utilizada para transformar uma sentença durante uma derivação.

 Exemplo:

```
S -> aS
```

 Significa que podemos substituir `S` por `aS`.

---

 ## 🔸 Derivação

 A **derivação** é o processo de aplicar as produções de uma gramática até chegar a uma palavra formada somente por símbolos terminais.

 Exemplo:

```
S
→ aS
→ aaS
→ aaaS
→ aaab
```

---

 ## 🔸 Palavra Vazia

 A palavra vazia é representada pelo símbolo:

```
ε
```

 Ela representa uma palavra que possui **zero símbolos**.

---

 ## 🔸 Gramática Regular

 Uma gramática regular possui produções que seguem um formato específico, como:

```
A -> aB
A -> a
```

 Por exemplo:

```
S -> aA
A -> b
```

 é uma gramática regular.

---

 ## 🔸 Linguagem Gerada

 A linguagem gerada por uma gramática é o conjunto de todas as palavras que podem ser produzidas através de suas regras.

 Por exemplo, para:

```
G2: S -> aSb | ε
```

 temos:

```
L(G2) = { aⁿbⁿ | n ≥ 0 }
```

 Exemplos:

```
ε
ab
aabb
aaabbb
aaaabbbb
...
```

---

 # 🎯 Para Memorizar

 ### 1\. Quando uma derivação termina?

 > Quando **não existem mais símbolos não terminais**.

---

 ### 2\. O que `S -> aSb` faz?

 > Adiciona **um `a` no início** e **um `b` no final**.

---

 ### 3\. Qual é o padrão de `G2`?

```
aⁿbⁿ
```

 Ou seja:

 > A quantidade de `a` deve ser igual à quantidade de `b`.

---

 ### 4\. Por que `aabbb` não pode ser gerada?

 Porque:

```
aabbb
```

 possui:

```
2 a's
3 b's
```

 E a gramática exige:

```
quantidade de a = quantidade de b
```

---

 ### 5\. Como saber se uma gramática é regular?

 Verifique se suas produções seguem o formato permitido para uma **gramática regular**.

 Exemplo:

```
A -> aB
A -> a
```

---

 # 📝 Checklist de Revisão

 - [ ] Sei diferenciar terminal e não terminal.
- [ ] Sei identificar o símbolo inicial.
- [ ] Sei fazer uma derivação passo a passo.
- [ ] Sei identificar quando uma derivação termina.
- [ ] Sei interpretar `ε` como palavra vazia.
- [ ] Sei verificar se uma palavra pertence à linguagem.
- [ ] Sei identificar o padrão `aⁿbⁿ`.
- [ ] Sei classificar uma gramática regular.
- [ ] Sei justificar por que uma palavra pode ou não ser gerada.

---

 # 📚 Exercícios Resolvidos — Conclusão

 | Conceito | O que lembrar |
| --- | --- |
| **Derivação** | Aplicação das regras da gramática |
| **Terminal** | Não pode mais ser substituído |
| **Não terminal** | Pode ser substituído |
| **`ε`** | Palavra vazia |
| **`S -> aSb`** | Adiciona `a` e `b` simultaneamente |
| **`aⁿbⁿ`** | Mesma quantidade de `a` e `b` |
| **Gramática Regular** | Produções seguem o formato regular |

> 💡 **Dica de estudo:** tente refazer cada exercício sem consultar as respostas. Depois, compare sua derivação com as soluções deste material.
