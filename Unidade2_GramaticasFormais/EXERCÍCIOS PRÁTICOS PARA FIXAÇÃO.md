📚 Exercícios Práticos para Fixação

Material de revisão sobre Gramáticas Formais, Derivação, Gramáticas Livres de Contexto (GLC) e Gramáticas Regulares.

📑 Sumário
Bloco 1 — Derivação
A) Gere a palavra aaab
B) Quando a derivação termina?
Bloco 2 — GLC
A) Gere a palavra aaabbb
B) É possível gerar aabbb?
Bloco 3 — Classificação
Resumo das respostas
Conceitos-chave
🔹 BLOCO 1 — DERIVAÇÃO

Dada a gramática:

G1: S -> aS | b

A) Gere a palavra aaab

Resposta:

Começamos pelo símbolo inicial S.

S
→ aS
→ aaS
→ aaaS
→ aaab


Portanto, a palavra aaab pode ser gerada pela gramática.

B) Quando a derivação termina?

Resposta:

A derivação termina quando não aparece mais nenhum símbolo não terminal.

No começo temos:

S


O símbolo S é um não terminal.

Aplicamos a regra:

S -> aS


algumas vezes e, no final, utilizamos:

S -> b


Chegamos então a:

aaab


Nesse ponto existem somente símbolos terminais:

a a a b


Por isso, a derivação terminou.

Regra: uma derivação termina quando a sentença contém somente símbolos terminais.

🔹 BLOCO 2 — GLC

Dada a gramática:

G2: S -> aSb | ε


ε representa a palavra vazia.

A) Gere a palavra aaabbb

Resposta:

Começamos com S.

S
→ aSb
→ aaSbb
→ aaaSbbb


Agora utilizamos a produção:

S -> ε


Portanto, a derivação completa é:

S
→ aSb
→ aaSbb
→ aaaSbbb
→ aaabbb


Portanto, a palavra aaabbb pode ser gerada.

B) É possível gerar aabbb?

Resposta: não.

A regra:

S -> aSb


sempre adiciona:

um a no início;
um b no final.

Logo, a quantidade de a e b será sempre igual.

Por exemplo:

S
→ aSb
→ aaSbb
→ aaaSbbb


Podemos gerar:

ab
aabb
aaabbb
aaaabbbb
...


Porém:

aabbb


possui:

2 letras a;
3 letras b.

Como as quantidades são diferentes, essa palavra não pode ser gerada.

❌ Resultado
aabbb ∉ L(G2)


Portanto:

aabbb não pertence à linguagem gerada por G2.

A linguagem gerada possui o formato:

L(G2) = { aⁿbⁿ | n ≥ 0 }


Exemplos:

ε
ab
aabb
aaabbb
aaaabbbb
...

🔹 BLOCO 3 — CLASSIFICAÇÃO

Classifique a gramática como REGULAR ou LIVRE DE CONTEXTO:

S -> aA
A -> b

Resposta

A gramática é REGULAR.

Isso acontece porque as produções seguem o formato de uma gramática regular.

Temos:

S -> aA


e:

A -> b


Na primeira produção temos:

a → terminal;
A → não terminal.

Na segunda produção temos apenas o terminal b.

🔄 Derivação

A palavra gerada pode ser obtida através de:

S
→ aA
→ ab


Logo:

ab


é uma palavra gerada pela gramática.

✅ Resultado

A gramática é REGULAR.

📌 RESUMO DAS RESPOSTAS
Bloco	Questão	Resposta
1	A	✅ aaab pode ser gerada
1	B	✅ A derivação termina quando não há não terminais

|
