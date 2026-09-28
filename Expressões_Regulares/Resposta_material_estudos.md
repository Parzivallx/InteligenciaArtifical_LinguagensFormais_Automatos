# 📚 8. Exercício Guiado

Antes de escrever a expressão:

1. Defina o alfabeto.
2. Separe a palavra em blocos.
3. Identifique escolhas e repetições.
4. Crie exemplos válidos e inválidos.
5. Escreva a expressão.

---

## 🔹 Exercício 1 — Sufixo `00`

Sobre **Σ = {0, 1}**, construa uma ER para todas as palavras que terminam em `00`.

### ✏️ Expressão

```regex
^[01]*00$

💡 Explicação
[01]* → qualquer quantidade de 0 e 1.

00 → garante que a palavra termina em 00.

^ e $ → garantem que toda a cadeia seja analisada.

🔹 Exercício 2 — Exatamente dois a
Sobre Σ = {a, b}, construa uma ER para palavras que possuem exatamente dois símbolos a e qualquer quantidade de b.

✏️ Expressão
^b*ab*ab*$

💡 Explicação
A estrutura é:

b* a b* a b*

Assim, existem exatamente dois a e qualquer quantidade de b.

🔹 Exercício 3 — Identificador Acadêmico
O identificador deve:

começar com duas letras maiúsculas;

possuir três algarismos;

terminar opcionalmente com uma letra minúscula;

não possuir caracteres extras.

✏️ Expressão
^[A-Z]{2}[0-9]{3}[a-z]?$

💡 Exemplos
Exemplo	Resultado
AB123	✅
XY456a	✅
A123	❌
ABC123	❌
AB12	❌
ab123	❌

🏆 9. Desafio Final — Código de Matrícula
📋 Formato
CURSO-ANO-NÚMERO-TURNO

📌 Regras
CURSO: CCO, ESW ou SIS;

ANO: de 2024 a 2029;

NÚMERO: exatamente quatro algarismos;

TURNO: M, T ou N;

os blocos são separados por -;

não são permitidos caracteres extras.

🔎 Regex
^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$

🧩 Estrutura
(CCO|ESW|SIS) - 202[4-9] - [0-9]{4} - (M|T|N)
      ↓             ↓           ↓          ↓
    Curso          Ano       Número      Turno

🔤 Conjuntos
C = {CCO, ESW, SIS}
A = {2024, 2025, 2026, 2027, 2028, 2029}
D = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
T = {M, T, N}

A linguagem é:

L = {c-a-d₁d₂d₃d₄-t | c ∈ C, a ∈ A, dᵢ ∈ D, t ∈ T}

🧩 Explicação da Regex
1️⃣ Curso
(CCO|ESW|SIS)

Permite somente CCO, ESW ou SIS.

2️⃣ Ano
202[4-9]

Permite 2024 até 2029.

3️⃣ Número
[0-9]{4}

Exige exatamente quatro algarismos.

{4} é diferente de +: {4} exige quatro, enquanto + permite um ou mais.

4️⃣ Turno
(M|T|N)

Permite M, T ou N.

5️⃣ Âncoras
^
$

Garantem que não existam caracteres extras antes ou depois da matrícula.

✅ Exemplos Válidos
Código	Resultado
CCO-2024-0001-M	✅
ESW-2026-1042-N	✅
SIS-2029-9999-T	✅
CCO-2027-0100-N	✅
ESW-2025-4321-M	✅
SIS-2028-5678-M	✅
CCO-2025-0042-T	✅

❌ Exemplos Inválidos
Código	Motivo
ADS-2026-0001-N	Curso inexistente
CCO-2030-0001-M	Ano fora do intervalo
SIS-2027-123-N	Número com três algarismos
esw-2026-1042-N	Curso em minúsculas
CCO/2026/0001/M	Separador incorreto
CCO-2026-0001-X	Turno inexistente
CCO-2026-0001-M-EXTRA	Caracteres extras

❓ Perguntas
1. Qual parte representa a escolha entre os cursos?
(CCO|ESW|SIS)

O operador | representa alternativas.

2. Como o ano foi limitado?
202[4-9]

Assim, somente 2024 a 2029 são aceitos.

3. Por que usar {4}?
[0-9]{4}

Porque o número precisa ter exatamente quatro algarismos.

4. Qual é a função de ^ e $?
Eles garantem que a Regex valide a cadeia inteira.

5. A Regex permite uma matrícula fora das regras?
Não. Ela limita o curso, ano, número, turno, separadores e tamanho da cadeia.

🤖 Desafio Extra — DFA Equivalente
O DFA lê a matrícula da esquerda para a direita.

🔄 Estados
Estado	Função
q0	início
q1	curso
q2	hífen após o curso
q3	ano
q4	hífen após o ano
q5	quatro algarismos do número
q6	hífen após o número
q7	turno
q8	aceitação
qd	estado sumidouro

🌐 Fluxo Simplificado
→ q0
   ↓ curso
  q1
   ↓ -
  q2
   ↓ ano
  q3
   ↓ -
  q4
   ↓ [0-9]{4}
  q5
   ↓ -
  q6
   ↓ M | T | N
  q7
   ↓
  q8 ★

Qualquer símbolo inválido leva para:

qd

E o estado qd permanece nele mesmo:

qd → qd

🧠 Como o DFA funciona?
📌 Curso
Aceita somente:

CCO
ESW
SIS

📅 Ano
Aceita somente:

2024
2025
2026
2027
2028
2029

🔢 Número
Exige exatamente:

[0-9][0-9][0-9][0-9]

🌙 Turno
Aceita:

M | T | N

⭐ Aceitação
q8 é o único estado de aceitação.

Se houver qualquer caractere extra ou inválido, a cadeia vai para qd.

✅ Conclusão
A expressão final é:

^(CCO|ESW|SIS)-202[4-9]-[0-9]{4}-(M|T|N)$

Ela representa:

CURSO - ANO - NÚMERO - TURNO

e garante que todos os requisitos da matrícula sejam respeitados.
