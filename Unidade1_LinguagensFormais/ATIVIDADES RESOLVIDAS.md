# Atividades Resolvidas — Linguagens Formais e Autômatos

Material de estudo com resoluções comentadas sobre alfabetos, palavras, linguagens, gramáticas e derivações.

> **Objetivo:** apresentar as respostas de forma simples, direta e adequada para consulta no GitHub.

---

## 📝 Atividade 1 — Prefixos e Sufixos

Considere a palavra:

```
ab

```

### Pergunta

Liste os prefixos e sufixos.

**Prefixos:**

Prefixo é uma parte que começa no início da palavra.
(ab) = {ε, a, ab}

**Sufixos:**

Sufixo é uma parte que termina no final da palavra.
(ab) = {ε, b, ab}

---

## 📝 Atividade 2 — Gramática

Considere:

```
G = ({S}, {a}, {S → aS | ε}, S)

```

### Pergunta

Liste 3 palavras geradas.

S → ε
S → aS → aε
S → aS → aaS → aaε

às 3 palavras são: ε, a, aa
também pode gerar: aaa, aaaa, aaaaa, ...

# Resolução dos Exercícios — Aulas 01 e 02

1. Alfabeto Considere:

Σ = {a, b, c}

Perguntas

1. Quantos símbolos existem no alfabeto?

Existem 3 símbolos.

2. Quais são os símbolos?

a, b, c

3. O símbolo a pertence ao alfabeto?

Sim.

a ∈ Σ

Isso acontece porque a está dentro do conjunto {a, b, c}.

4. O símbolo d pertence ao alfabeto?

Não.

d ∉ Σ

O símbolo d não aparece no alfabeto.

5. Escreva uma palavra formada por símbolos desse alfabeto.

Podemos escolher qualquer sequência formada somente por a, b e c.

Por exemplo:

abc

Outros exemplos seriam:

a
bb
cab
abca

Resposta final
Quantidade de símbolos: 3

Símbolos: {a, b, c}

a ∈ Σ

d ∉ Σ

Exemplo de palavra: abc

Ideia principal: para uma palavra ser válida sobre um alfabeto, todos os seus símbolos precisam pertencer ao alfabeto.

2. Palavras sobre um alfabeto Considere:

Σ = {0, 1}

Classifique as sequências.

Sequência	Válida?	Justificativa
0101	Sim	Todos os símbolos são 0 ou 1.
00110	Sim	Todos os símbolos são 0 ou 1.
012	Não	O símbolo 2 não pertence ao alfabeto.
111	Sim	Todos os símbolos são 0 ou 1.
10a	Não	O símbolo a não pertence ao alfabeto.

Explicação
O alfabeto só permite:

0
1

Então podemos criar palavras como:

0
1
00
01
10
11
0101
111

Mas não podemos usar outros símbolos:

2
a
b

Por isso:

012

é inválida, pois contém 2.

E:

10a

é inválida porque contém a.

3. Pertinência de símbolos e palavras Considere:

Σ = {0, 1}

Determine se as afirmações são verdadeiras ou falsas.

1. 0 ∈ Σ Verdadeiro.

O símbolo 0 está no alfabeto.

0 ∈ Σ

2. 1 ∈ Σ Verdadeiro.

O símbolo 1 também pertence ao alfabeto.

1 ∈ Σ

3. 01 ∈ Σ Falso.

Aqui está uma diferença muito importante.

Σ contém símbolos, enquanto 01 possui dois símbolos.

Portanto, 01 é uma palavra, não um símbolo individual.

01 ∉ Σ

4. 01 ∈ Σ\* Verdadeiro.

Σ\* contém todas as palavras possíveis formadas com 0 e 1.

Como 01 é formada somente por esses símbolos:

01 ∈ Σ\*

5. 2 ∈ Σ Falso.

O alfabeto é:

Σ = {0, 1}

O símbolo 2 não está nele.

2 ∉ Σ

6. 101 ∈ Σ\* Verdadeiro.

A palavra 101 contém somente símbolos permitidos:

1 0 1

Portanto:

101 ∈ Σ\*

Resumo
0 ∈ Σ       → Verdadeiro
1 ∈ Σ       → Verdadeiro
01 ∈ Σ      → Falso
01 ∈ Σ\*     → Verdadeiro
2 ∈ Σ       → Falso
101 ∈ Σ\*    → Verdadeiro

Dica importante: Σ representa os símbolos do alfabeto. Já Σ\* representa as palavras que podemos construir com esses símbolos.

4. Linguagem Considere:

L = {0, 01, 011, 0111}

Determine se cada palavra pertence à linguagem.

Palavra	Pertence a L?
0	Sim
01	Sim
0111	Sim
10	Não
111	Não
011	Sim

Explicação
Uma linguagem é simplesmente um conjunto de palavras.

Nossa linguagem é:

L = {0, 01, 011, 0111}

Então basta verificar se a palavra aparece no conjunto.

Por exemplo:

01 ∈ L

porque 01 está escrito dentro de L.

Já:

10 ∉ L

porque 10 não aparece no conjunto.

Resposta final
0    ∈ L
01   ∈ L
0111 ∈ L
10   ∉ L
111  ∉ L
011  ∈ L

5. Descrevendo uma linguagem por padrão Considere:

L = {bⁿ | n ≥ 1}

1. Escreva as cinco primeiras palavras Precisamos ter pelo menos um b.

Assim:

b
bb
bbb
bbbb
bbbbb

2. Explique o significado de bⁿ O n representa quantas vezes o símbolo b aparece.

Por exemplo:

b¹ = b
b² = bb
b³ = bbb
b⁴ = bbbb

Portanto, bⁿ significa:

Uma palavra formada por n símbolos b.

Como temos:

n ≥ 1

precisamos ter pelo menos um b.

3. A palavra bbbbbb pertence à linguagem? Sim.

Ela possui seis símbolos b:

bbbbbb = b⁶

Como:

6 ≥ 1

então:

bbbbbb ∈ L

4. A palavra vazia ε pertence à linguagem? Não.

A palavra vazia possui zero símbolos:

|ε| = 0

Mas a linguagem exige:

n ≥ 1

Como 0 não é maior ou igual a 1:

ε ∉ L

Resposta final
Cinco primeiras palavras:

b
bb
bbb
bbbb
bbbbb

bⁿ = n ocorrências de b

bbbbbb ∈ L

ε ∉ L

Dica: quando aparecer algo como aⁿ | n ≥ 1, pense: "uma quantidade de a, começando com pelo menos um".

6. Linguagem vazia e palavra vazia Precisamos diferenciar:

∅

de:

ε

A) L = ∅
Isso significa que a linguagem não possui nenhuma palavra.

L = ∅

Quantidade de palavras:

0

B) L = {ε}
Aqui temos uma linguagem que possui uma palavra.

Essa única palavra é ε.

L = {ε}

Quantidade de palavras:

1

E o comprimento dessa palavra é:

|ε| = 0

Respostas
Qual delas possui uma palavra?

L = {ε}

possui uma palavra.

Qual delas não possui nenhuma palavra?

L = ∅

não possui nenhuma palavra.

Qual é o comprimento da palavra ε?

|ε| = 0

⚠️ Atenção
Não confunda:

∅

com:

ε

∅ significa nenhum elemento.

ε é uma palavra que possui zero símbolos.

Por isso:

∅ ≠ {ε}

7. Estrutura de uma gramática Considere:

G = (S, A, 0, 1, P, S)

com:

P = {S → 0A, A → 1}

1. Conjunto de variáveis As variáveis, ou não terminais, são:

V = {S, A}

2. Conjunto de terminais Os terminais são:

T = {0, 1}

São os símbolos que aparecerão na palavra final.

3. Conjunto de produções As regras são:

P = {S → 0A, A → 1}

4. Símbolo inicial O símbolo inicial é:

S

É por ele que começamos a derivação.

5. Qual palavra pode ser gerada? Começamos com:

S

Aplicamos:

S → 0A

Então:

S ⇒ 0A

Agora aplicamos:

A → 1

Logo:

0A ⇒ 01

Portanto:

S ⇒ 0A ⇒ 01

A palavra gerada é:

01

Resposta final
Variáveis:     V = {S, A}
Terminais:     T = {0, 1}
Produções:     P = {S → 0A, A → 1}
Inicial:       S
Palavra:       01

8. Como ler e aplicar uma produção Considere:

S → 0S

Começamos com:

S

Uma aplicação
S ⇒ 0S

Duas aplicações
Aplicamos novamente a regra:

S ⇒ 0S ⇒ 00S

Três aplicações
Aplicamos mais uma vez:

S ⇒ 0S ⇒ 00S ⇒ 000S

Resposta final
S ⇒ 0S ⇒ 00S ⇒ 000S

Atenção: a derivação ainda não terminou.

Por quê?

Porque ainda temos o símbolo S, que é um não terminal:

000S

Uma derivação termina quando não existem mais não terminais na palavra.

9. Derivação completa de uma palavra Considere:

G:
{
S → aS
S → b
}

Queremos gerar:

aaab

Precisamos produzir três a e depois terminar com b.

Passo 1
Começamos com:

S

Aplicamos S → aS:

S ⇒ aS

Passo 2
Aplicamos novamente:

aS ⇒ aaS

Então:

S ⇒ aS ⇒ aaS

Passo 3
Aplicamos novamente:

aaS ⇒ aaaS

Agora temos três a:

S ⇒ aS ⇒ aaS ⇒ aaaS

Passo 4
Agora precisamos terminar a palavra com b.

Usamos:

S → b

Então:

aaaS ⇒ aaab

Derivação completa
S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab

Portanto:

aaab ∈ L(G)

Como pensar: cada vez que usamos S → aS, acrescentamos um 
a. Quando já temos a quantidade desejada de a, usamos S → b para 
finalizar.

10. Identificando palavras geradas por uma gramática Considere:

G:
{
S → 0S
S → 1
}

A gramática produz vários 0 e, no final, um único 1.

Vamos analisar cada palavra.

1. 1 Sim.

Basta usar:

S ⇒ 1

Portanto:

1 ∈ L(G)

2. 01 Sim.

S ⇒ 0S ⇒ 01

Portanto:

01 ∈ L(G)

3. 001 Sim.

S ⇒ 0S ⇒ 00S ⇒ 001

Portanto:

001 ∈ L(G)

4. 0001 Sim.

S ⇒ 0S
⇒ 00S
⇒ 000S
⇒ 0001

Portanto:

0001 ∈ L(G)

5. 101 Não.

Podemos produzir:

S ⇒ 1

Mas quando usamos S → 1, a derivação termina.

Não podemos fazer:

S ⇒ 1

e depois acrescentar 01.

Portanto:

101 ∉ L(G)

6. 1001 Também não.

A palavra começa com 1, mas depois possui outros símbolos.

Quando usamos:

S → 1

a derivação termina imediatamente.

Portanto:

1001 ∉ L(G)

Resumo
Palavra	Pode ser gerada?	Derivação
1	Sim	S ⇒ 1
01	Sim	S ⇒ 0S ⇒ 01
001	Sim	S ⇒ 0S ⇒ 00S ⇒ 001
0001	Sim	S ⇒ 0S ⇒ 00S ⇒ 000S ⇒ 0001
101	Não	Não é possível continuar depois de produzir 1.
1001	Não	Não é possível colocar símbolos depois do 1 final.

Padrão da gramática
As palavras geradas possuem o formato:

000...001

Ou seja:

zero ou mais 0, seguidos de exatamente um 1 no final.

11. Desafio Final Considere:

G:
{
S → aS
S → b
}

Vamos resolver cada questão.

1. A palavra b pode ser gerada? Sim.

Usamos diretamente:

S ⇒ b

Portanto:

b ∈ L(G)

2. A palavra ab pode ser gerada? Sim.

Primeiro colocamos um a:

S ⇒ aS

Depois encerramos com b:

aS ⇒ ab

Derivação completa:

S ⇒ aS ⇒ ab

Portanto:

ab ∈ L(G)

3. A palavra aab pode ser gerada? Sim.

Precisamos colocar dois a antes do b:

S ⇒ aS
⇒ aaS
⇒ aab

Portanto:

aab ∈ L(G)

4. A palavra aaab pode ser gerada? Sim.

Precisamos colocar três a:

S ⇒ aS
⇒ aaS
⇒ aaaS
⇒ aaab

Portanto:

aaab ∈ L(G)

5. A palavra aba pode ser gerada? Não.

A gramática permite colocar vários a, mas o b precisa ser o último símbolo.

Para produzir b, fazemos:

S ⇒ b

E nesse momento a derivação termina.

Não existe uma regra que permita transformar:

b

em:

ba

Portanto:

aba ∉ L(G)

6. Derivação completa de aaaab Precisamos de quatro a antes do b.

Começamos:

S

Aplicamos S → aS quatro vezes:

S
⇒ aS
⇒ aaS
⇒ aaaS
⇒ aaaaS

Agora usamos:

S → b

Então:

aaaaS ⇒ aaaab

Derivação completa
S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaaaS ⇒ aaaab

Portanto:

aaaab ∈ L(G)

7. Qual é o padrão das palavras geradas? A gramática possui duas possibilidades:

S → aS

ou:

S → b

A primeira regra adiciona um a e permite continuar.

A segunda coloca b e encerra a derivação.

Por isso, podemos gerar:

b
ab
aab
aaab
aaaab
aaaaab
...

O padrão é:

aⁿb | n ≥ 0

Isso significa:

Qualquer quantidade de a, inclusive zero, seguida por exatamente um b.

Por isso:

b       → válida
ab      → válida
aab     → válida
aaab    → válida
aaaab   → válida

Mas:

aba     → inválida
abb     → inválida
baa     → inválida
aaba    → inválida

Resposta do desafio

1. b       → Sim
2. ab      → Sim
3. aab     → Sim
4. aaab    → Sim
5. aba     → Não
6. aaaab   → S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaaaS ⇒ aaaab
7. Padrão  → aⁿb, com n ≥ 0

🧠 Resumo para estudar
Os conceitos mais importantes deste material são:

Σ

Representa o alfabeto, ou seja, o conjunto de símbolos disponíveis.

Σ\*

Representa todas as palavras finitas que podem ser construídas usando os símbolos de Σ, incluindo ε.

ε

É a palavra vazia e possui comprimento zero:

|ε| = 0

∅

É o conjunto vazio, que não possui nenhum elemento.

L

Representa uma linguagem, que é um conjunto de palavras.

w ∈ L

Significa que a palavra w pertence à linguagem L.

w ∉ L

Significa que w não pertence à linguagem L.

Uma gramática pode ser representada por:

G = (V, T, P, S)

Onde:

V = variáveis / não terminais
T = terminais
P = produções
S = símbolo inicial

Uma regra como:

S → aS

significa que podemos substituir S por aS.

Já:

S ⇒ aS

representa que aplicamos uma regra de produção durante uma derivação.

---

# Exercícios Práticos para Fixação

## Bloco 1 — Derivação

Considere a gramática:

```text
G₁:
S → aS | b
```

### A) Gere a palavra `aaab`

Queremos formar três símbolos `a` e terminar com `b`.

Começamos pelo símbolo inicial:

```text
S
```

Aplicamos a regra `S → aS` três vezes:

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aaaS
```

Agora usamos a regra `S → b`:

```text
aaaS ⇒ aaab
```

Portanto, a derivação completa é:

```text
S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab
```

Logo:

```text
aaab ∈ L(G₁)
```

### B) Como sabemos que a derivação terminou?

A derivação termina quando não existe mais nenhum símbolo **não terminal** na palavra.

Na expressão:

```text
aaaS
```

ainda existe o não terminal `S`, então a derivação não terminou.

Depois da aplicação:

```text
aaaS ⇒ aaab
```

restam somente os símbolos terminais `a` e `b`.

Por isso, a derivação terminou.

---

## Bloco 2 — Gramática Livre de Contexto

Considere:

```text
G₂:
S → aSb | ε
```

A regra `S → aSb` coloca um `a` no início e um `b` no final.

A regra `S → ε` encerra a derivação.

### A) Gere a palavra `aaabbb`

Aplicamos `S → aSb` três vezes:

```text
S
⇒ aSb
⇒ aaSbb
⇒ aaaSbbb
```

Agora encerramos com:

```text
S → ε
```

Assim:

```text
aaaSbbb ⇒ aaaεbbb
```

Como `ε` representa a palavra vazia:

```text
aaaεbbb = aaabbb
```

Portanto:

```text
S ⇒ aSb ⇒ aaSbb ⇒ aaaSbbb ⇒ aaabbb
```

Logo:

```text
aaabbb ∈ L(G₂)
```

### B) É possível gerar `aabbb`?

**Não.**

Observe o comportamento da regra:

```text
S → aSb
```

Toda vez que ela é aplicada, adicionamos:

- um `a`;
- um `b`.

Isso significa que sempre teremos a mesma quantidade de `a` e `b`.

As palavras geradas possuem o formato:

```text
aⁿbⁿ, com n ≥ 0
```

Exemplos:

```text
ε
ab
aabb
aaabbb
aaaabbbb
...
```

A palavra:

```text
aabbb
```

possui:

```text
2 símbolos a
3 símbolos b
```

Como as quantidades são diferentes:

```text
aabbb ∉ L(G₂)
```

Portanto, **não é possível gerar `aabbb` com essa gramática**.

---

## Bloco 3 — Classificação da Gramática

Considere:

```text
S → aA
A → b
```

Devemos classificar a gramática como **Regular** ou **Livre de Contexto**.

As produções são:

```text
S → aA
A → b
```

Uma gramática regular à direita pode possuir regras do tipo:

```text
A → aB
```

ou:

```text
A → a
```

As duas regras apresentadas seguem exatamente esse formato:

```text
S → aA
A → b
```

Portanto, a gramática é:

```text
REGULAR
```

Como toda gramática regular também é uma gramática livre de contexto, ela poderia ser considerada livre de contexto em um sentido mais amplo. Porém, quando a questão pede a classificação mais específica, a resposta correta é:

> **Gramática Regular.**

A única palavra gerada por essa gramática é:

```text
S ⇒ aA ⇒ ab
```

Logo:

```text
L(G) = {ab}
```

---

## Resumo dos três blocos

| Bloco | Resultado |
|---|---|
| 1 | `S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab` |
| 1 — término | A derivação termina quando restam apenas terminais |
| 2 | `S ⇒ aSb ⇒ aaSbb ⇒ aaaSbbb ⇒ aaabbb` |
| 2 — `aabbb` | Não pode ser gerada |
| 2 — padrão | `L(G₂) = {aⁿbⁿ | n ≥ 0}` |
| 3 | Gramática **Regular** |
| 3 — palavra gerada | `ab` |

## Dica para memorizar

Quando você estiver analisando uma gramática, observe principalmente **onde o não terminal aparece**.

Por exemplo:

```text
S → aS
```

permite continuar acrescentando símbolos.

Já:

```text
S → b
```

elimina o não terminal e encerra a derivação.

Em uma regra como:

```text
S → aSb
```

o não terminal fica no meio da palavra. Esse tipo de estrutura permite criar dependências entre partes da palavra, como a mesma quantidade de `a` e `b`.

# Exercícios Práticos para Fixação

## Bloco 1 — Derivação

Considere a gramática:

```text
G₁:
S → aS | b
```

### A) Gere a palavra `aaab`

Queremos formar três símbolos `a` e terminar com `b`.

Começamos pelo símbolo inicial:

```text
S
```

Aplicamos a regra `S → aS` três vezes:

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aaaS
```

Agora usamos a regra `S → b`:

```text
aaaS ⇒ aaab
```

Portanto, a derivação completa é:

```text
S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab
```

Logo:

```text
aaab ∈ L(G₁)
```

### B) Como sabemos que a derivação terminou?

A derivação termina quando não existe mais nenhum símbolo **não terminal** na palavra.

Na expressão:

```text
aaaS
```

ainda existe o não terminal `S`, então a derivação não terminou.

Depois da aplicação:

```text
aaaS ⇒ aaab
```

restam somente os símbolos terminais `a` e `b`.

Por isso, a derivação terminou.

---

## Bloco 2 — Gramática Livre de Contexto

Considere:

```text
G₂:
S → aSb | ε
```

A regra `S → aSb` coloca um `a` no início e um `b` no final.

A regra `S → ε` encerra a derivação.

### A) Gere a palavra `aaabbb`

Aplicamos `S → aSb` três vezes:

```text
S
⇒ aSb
⇒ aaSbb
⇒ aaaSbbb
```

Agora encerramos com:

```text
S → ε
```

Assim:

```text
aaaSbbb ⇒ aaaεbbb
```

Como `ε` representa a palavra vazia:

```text
aaaεbbb = aaabbb
```

Portanto:

```text
S ⇒ aSb ⇒ aaSbb ⇒ aaaSbbb ⇒ aaabbb
```

Logo:

```text
aaabbb ∈ L(G₂)
```

### B) É possível gerar `aabbb`?

**Não.**

Observe o comportamento da regra:

```text
S → aSb
```

Toda vez que ela é aplicada, adicionamos:

- um `a`;
- um `b`.

Isso significa que sempre teremos a mesma quantidade de `a` e `b`.

As palavras geradas possuem o formato:

```text
aⁿbⁿ, com n ≥ 0
```

Exemplos:

```text
ε
ab
aabb
aaabbb
aaaabbbb
...
```

A palavra:

```text
aabbb
```

possui:

```text
2 símbolos a
3 símbolos b
```

Como as quantidades são diferentes:

```text
aabbb ∉ L(G₂)
```

Portanto, **não é possível gerar `aabbb` com essa gramática**.

---

## Bloco 3 — Classificação da Gramática

Considere:

```text
S → aA
A → b
```

Devemos classificar a gramática como **Regular** ou **Livre de Contexto**.

As produções são:

```text
S → aA
A → b
```

Uma gramática regular à direita pode possuir regras do tipo:

```text
A → aB
```

ou:

```text
A → a
```

As duas regras apresentadas seguem exatamente esse formato:

```text
S → aA
A → b
```

Portanto, a gramática é:

```text
REGULAR
```

Como toda gramática regular também é uma gramática livre de contexto, ela poderia ser considerada livre de contexto em um sentido mais amplo. Porém, quando a questão pede a classificação mais específica, a resposta correta é:

> **Gramática Regular.**

A única palavra gerada por essa gramática é:

```text
S ⇒ aA ⇒ ab
```

Logo:

```text
L(G) = {ab}
```

---

## Resumo dos três blocos

| Bloco | Resultado |
|---|---|
| 1 | `S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab` |
| 1 — término | A derivação termina quando restam apenas terminais |
| 2 | `S ⇒ aSb ⇒ aaSbb ⇒ aaaSbbb ⇒ aaabbb` |
| 2 — `aabbb` | Não pode ser gerada |
| 2 — padrão | `L(G₂) = {aⁿbⁿ | n ≥ 0}` |
| 3 | Gramática **Regular** |
| 3 — palavra gerada | `ab` |

## Dica para memorizar

Quando você estiver analisando uma gramática, observe principalmente **onde o não terminal aparece**.

Por exemplo:

```text
S → aS
```

permite continuar acrescentando símbolos.

Já:

```text
S → b
```

elimina o não terminal e encerra a derivação.

Em uma regra como:

```text
S → aSb
```

o não terminal fica no meio da palavra. Esse tipo de estrutura permite criar dependências entre partes da palavra, como a mesma quantidade de `a` e `b`. 
# Exercícios Práticos para Fixação

**Disciplina:** Linguagens Formais e Autômatos  
**Curso:** Inteligência Artificial

---

## Bloco 1 — Derivação

Dada a gramática:

```text
G₁: S → aS | b
```

### A) Gere a palavra `aaab`

Começamos pelo símbolo inicial `S` e aplicamos as regras da gramática:

```text
S ⇒ aS
  ⇒ aaS
  ⇒ aaaS
  ⇒ aaab
```

Portanto, a palavra `aaab` pode ser gerada pela gramática.

### B) Como saber que a derivação terminou?

A derivação termina quando não existe mais nenhuma variável, ou símbolo não terminal, na palavra.

No caso:

```text
aaab
```

A palavra possui apenas símbolos terminais (`a` e `b`). Como não existe mais o símbolo `S`, nenhuma outra regra precisa ser aplicada.

---

## Bloco 2 — Gramática Livre de Contexto (GLC)

Dada a gramática:

```text
G₂: S → aSb | ε
```

Onde `ε` representa a palavra vazia.

### A) Gere a palavra `aaabbb`

Aplicando as regras:

```text
S ⇒ aSb
  ⇒ aaSbb
  ⇒ aaaSbbb
  ⇒ aaaεbbb
  ⇒ aaabbb
```

Portanto, a palavra `aaabbb` pode ser gerada pela gramática.

### B) É possível gerar `aabbb`? Justifique.

**Não.**

A regra:

```text
S → aSb
```

sempre adiciona um `a` no início e um `b` no final ao mesmo tempo.

Por isso, essa gramática gera palavras com a mesma quantidade de `a` e `b`, seguindo o padrão:

```text
ε
ab
aabb
aaabbb
aaaabbbb
...
```

De forma geral, a linguagem gerada é:

```text
L(G₂) = { aⁿbⁿ | n ≥ 0 }
```

A palavra `aabbb` possui:

- 2 símbolos `a`;
- 3 símbolos `b`.

Como as quantidades são diferentes, `aabbb` **não pertence à linguagem gerada pela gramática**.

---

## Bloco 3 — Classificação da Gramática

Considere a gramática:

```text
S → aA
A → b
```

### Classificação

Essa gramática é **Regular**.

### Justificativa

Uma gramática regular pode possuir regras no formato:

```text
A → aB
```

ou

```text
A → a
```

Na gramática apresentada:

```text
S → aA
A → b
```

as duas regras seguem esse formato.

A derivação possível é:

```text
S ⇒ aA ⇒ ab
```

Portanto, a linguagem gerada é:

```text
L = { ab }
```

Logo, a classificação mais adequada é **Gramática Regular**.

> Observação: toda gramática regular também pode ser vista como uma gramática livre de contexto, mas, quando existe uma classificação mais específica, classificamos esta gramática como **Regular**.

---

## Resumo das respostas

| Bloco | Resposta |
|---|---|
| 1A | `S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaab` |
| 1B | Termina quando restam apenas símbolos terminais. |
| 2A | `S ⇒ aSb ⇒ aaSbb ⇒ aaaSbbb ⇒ aaabbb` |
| 2B | Não. A gramática gera apenas palavras com a mesma quantidade de `a` e `b`. |
| 3 | A gramática é **Regular**. |
