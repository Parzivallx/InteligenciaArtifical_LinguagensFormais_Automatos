# Sistema Especialista para Orientação de Recrutas em Formação

> *Treino duro, combate fácil.*

**Integrantes:** ______________________ e ______________________
**Curso:** ______________________
**Disciplina:** Inteligência Artificial e LFA
**Professora:** Kadidja Valéria

## Por que escolhemos esse tema

Escolhemos a formação de recrutas porque é um terreno que conhecemos de perto: já pagamos flexão, já levamos bronca de sargento e já erramos o pé na ordem unida. Sabemos, na prática, que o instrutor tem uma tropa grande, pouco tempo e precisa decidir rápido quem precisa de reforço e quem já pode ajudar os colegas.

A ideia foi pegar essa decisão do dia a dia da caserna e transformar num sistema que junta duas coisas: um modelo que aprende com exemplos e um conjunto de regras escritas a partir da nossa própria experiência.

## Arquivos do repositório

| Arquivo | Conteúdo |
|---|---|
| `sistema_especialista_recrutas_militar_BRASIL_2027.ipynb` | Notebook comentado com o desenvolvimento completo, as respostas à leitura e a análise dos resultados |
| `dataset_recrutas_simulado.csv` | Dataset rotulado usado no treino e no teste (40 exemplos) |
| `README.md` | Este arquivo |

## Como funciona

O sistema trabalha em duas etapas, como uma cadeia de comando:

1. **A árvore de decisão reconhece o perfil do recruta.** Ela olha o desempenho no TAF e o aproveitamento nas avaliações de instrução e classifica o recruta como `acompanhamento` (ainda precisa do instrutor por perto) ou `autonomia` (já se vira sozinho).
2. **O sistema especialista emite a recomendação.** Ele pega o perfil previsto pela árvore, junta com uma informação que vem do instrutor (se o recruta tem ou não dificuldade em ordem unida) e aplica a regra correspondente. Na saída aparecem a atividade recomendada, a regra usada e o porquê.

A palavra final é sempre do instrutor. O sistema só assessora: computador não tem divisa.

## As regras

Escrevemos quatro regras com base no que vivemos na formação. Elas não foram aprendidas dos dados, e essa é justamente a diferença entre a parte especialista e a parte de aprendizado de máquina.

- **R1:** perfil de acompanhamento com dificuldade em ordem unida → reforço com o instrutor, repetindo até sair em forma.
- **R2:** perfil de acompanhamento sem dificuldade em ordem unida → instrução supervisionada e revisão dos fundamentos, porque o problema tende a ser a base geral.
- **R3:** perfil de autonomia com dificuldade em ordem unida → treino específico de ordem unida, sem precisar de acompanhamento constante.
- **R4:** perfil de autonomia sem dificuldade → auxiliar de instrução ou chefe de grupo, para apoiar os demais.

## Os dados

Montamos um dataset **simulado** com 40 recrutas fictícios (21 de autonomia e 19 de acompanhamento). Nenhum recruta real foi usado.

O critério de rotulagem foi simples: quem tem 60% ou mais no TAF **e** na instrução é `autonomia`, e o resto é `acompanhamento`. Em 3 casos de fronteira decidimos o rótulo no olho, como um instrutor faria, para simular a subjetividade que existe em uma rotulagem de verdade. Esses casos estão marcados na coluna `rotulo_ajustado`.

O arquivo `dataset_recrutas_simulado.csv` tem as colunas `id`, `taf_percentual`, `instrucao_percentual`, `perfil` e `rotulo_ajustado`.

## O que conseguimos

Separamos 30 exemplos para treino e 10 para teste. A árvore (com profundidade máxima 2) acertou **93,3% no treino** e **100% no teste**.

Parece ótimo, mas encaramos com desconfiança, porque bom soldado desconfia de vitória fácil. São só 10 casos de teste, os dados são simulados e os rótulos seguem uma regra que nós mesmos criamos. Na prática, a árvore redescobriu o nosso critério. Os dois erros no treino foram justamente dois dos casos de fronteira que rotulamos no olho.

## Limitações

- O dataset é pequeno e simulado, então os resultados não valem para uma formação real.
- O modelo só enxerga dois números. A realidade de um recruta envolve saúde, adaptação ao quartel, motivação e muito mais.
- A dificuldade em ordem unida depende da observação de uma pessoa e pode carregar viés.
- Desempenho de pessoas é dado sensível. Num uso real, seria preciso anonimizar, coletar só o necessário e respeitar a LGPD.

Tudo isso está discutido com mais calma no notebook.

## Como rodar

O jeito mais fácil é abrir o notebook no [Google Colab](https://colab.research.google.com/) e ir em **Ambiente de execução → Executar tudo**. Os dados já estão dentro do notebook, então não precisa carregar o CSV.

Se preferir rodar na sua máquina:

```bash
pip install pandas matplotlib scikit-learn jupyter
jupyter notebook sistema_especialista_recrutas_militar_BRASIL_2027.ipynb
```

## Tecnologias

Python, pandas, scikit-learn, matplotlib e Google Colab.

## Referências

- IBM. Guia de Aprendizado de Máquina: https://www.ibm.com/br-pt/think/machine-learning
- IBM. Aprendizado supervisionado: https://www.ibm.com/br-pt/think/topics/supervised-learning
- scikit-learn. DecisionTreeClassifier: https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html
- scikit-learn. train_test_split: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html
