📚 Exercícios Práticos para Fixação

Material de revisão sobre Gramáticas Formais, Derivação, Gramáticas Livres de Contexto (GLC) e Gramáticas Regulares.

📑 Sumário
🔹 Bloco 1 — Derivação
A) Gerando aaab
B) Identificando o fim da derivação
🔹 Bloco 2 — GLC
A) Gerando aaabbb
B) É possível gerar aabbb?
🔹 Bloco 3 — Classificação
📌 Resumo das respostas
🔹 Bloco 1 — Derivação

Considere a seguinte gramática:

G1: S -> aS | b

A) Gerando aaab

Queremos descobrir se a palavra aaab pode ser gerada pela gramática.

Começamos pelo símbolo inicial S:

S
→ aS
→ aaS
→ aaaS
→ aaab

✅ Resultado

A palavra aaab pode ser gerada pela gramática G1.

B) Identificando o fim da derivação

A derivação termina quando não existem mais símbolos não terminais na palavra.

No início temos:

S


O símbolo S é um não terminal.

Aplicamos algumas vezes a produção:

S → aS


Até chegar ao momento em que utilizamos:

S → b


Obtendo:

aaab


Agora temos somente símbolos terminais:

a a a b

💡 Regra importante

Uma derivação terminou quando a sentença resultante contém somente símbolos terminais.

🔹 Bloco 2 — GLC

Considere a gramática:

G2: S -> aSb | ε


Observação: ε representa a palavra vazia.

A) Gerando aaabbb

Começamos pelo símbolo inicial S:

S
→ aSb
→ aaSbb
→ aaaSbbb


Agora precisamos eliminar o último não terminal S.

Para isso, utilizamos:

S → ε


Portanto:

S
→ aSb
→ aaSbb
→ aaaSbbb
→ aaabbb

✅ Resultado

A palavra aaabbb pode ser gerada pela gramática G2.

B) É possível gerar aabbb?

Não.

A produção:

S → aSb


sempre adiciona:

um a no início;
um b no final.

Ou seja, os símbolos são adicionados em pares.

Por exemplo:

S
→ aSb
→ aaSbb
→ aaaSbbb


Isso permite gerar palavras como:

ab
aabb
aaabbb
aaaabbbb
...


Observe o padrão:

Palavra	Quantidade de a	Quantidade de b
ab	1	1
aabb	2	2
aaabbb	3	3
aaaabbbb	4	4

Já a palavra:

aabbb


possui:

2 a
3 b

As quantidades são diferentes.

❌ Resultado
aabbb ∉ L(G2)


Portanto, aabbb não pertence à linguagem gerada por G2.

💡 Regra importante

A gramática G2 gera palavras no formato:

aⁿbⁿ


onde n ≥ 0.

Exemplos:

ε
ab
aabb
aaabbb
aaaabbbb
...

🔹 Bloco 3 — Classificação

Considere a gramática:

S -> aA
A -> b


A pergunta é:

Essa gramática é REGULAR ou LIVRE DE CONTEXTO?

🔎 Analisando as produções

Primeira produção:

S → aA


Temos:

a → terminal;
A → não terminal.

Segunda produção:

A → b


Temos somente um terminal.

Essas produções estão de acordo com o formato de uma gramática regular.

🔄 Derivação

Podemos verificar isso gerando a palavra:

S
→ aA
→ ab


Logo, a gramática gera:

ab

✅ Resultado

A gramática é:

🟢 REGULAR
📌 Resumo das Respostas
Bloco	Questão	Resposta
1	A	✅ aaab pode ser gerada
1	B	✅ A derivação termina quando não há não terminais
2	A	✅ aaabbb pode ser gerada
2	B	❌ aabbb não pode ser gerada
3	Classificação	🟢 Gramática REGULAR
🧠 Conceitos-chave
🔸 Terminal

É um símbolo que aparece na palavra final e não precisa mais ser substituído.

Exemplos:

a
b

🔸 Não terminal

É um símbolo utilizado durante a derivação e que pode ser substituído por uma produção.

Exemplo:

S
A

🔸 Derivação

É o processo de aplicar as produções da gramática até chegar a uma palavra formada somente por terminais.

Exemplo:

S
→ aS
→ aaS
→ aaaS
→ aaab

🔸 Palavra vazia

Representada por:

ε


Significa uma palavra que possui zero símbolos.

🔸 Gramática Regular

Uma gramática cujas produções seguem um formato regular, como:

A → aB
A → a

🎯 Para memorizar

Derivação termina → só existem terminais.

S → aSb → adiciona um a e um b juntos.

Gramática regular → produções seguem o formato regular.

📝 Checklist de revisão
 Sei diferenciar terminal e não terminal.
 Sei fazer uma derivação passo a passo.
 Sei identificar quando uma derivação termina.
 Sei interpretar ε como palavra vazia.
 Sei verificar se uma palavra pertence à linguagem.
 Sei identificar uma gramática regular.
 Sei explicar por que uma palavra não pode ser gerada.

📚 Fim dos exercícios

💡 Dica: tente refazer cada derivação sem olhar a resposta. Depois, compare seu resultado com as soluções acima.
