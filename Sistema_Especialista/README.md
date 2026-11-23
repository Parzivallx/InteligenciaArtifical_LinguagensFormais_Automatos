# Sistema Especialista com Aprendizado Supervisionado: Orientação de Recrutas em Formação

> *Treino duro, combate fácil.*

Trabalho da disciplina **Inteligência Artificial e LFA**, com a Profa. Kadidja Valéria.

**Integrantes:** Emmanuel Ferreira Gomes e João Pedro Reis Rios

## Sobre o projeto

O sistema une duas formas de conhecimento para recomendar a atividade de instrução mais adequada para cada recruta em formação:

1. **Aprendizado supervisionado:** uma árvore de decisão aprende, a partir de exemplos rotulados, a reconhecer o perfil do recruta (`acompanhamento` ou `autonomia`).
2. **Sistema especialista:** um conjunto de regras escritas por nós (o "regulamento") combina o perfil previsto pela árvore com um fato informado pelo instrutor e emite a recomendação, junto com a regra aplicada e a justificativa.

> ⚠️ **Todos os dados são simulados.** Nenhum recruta real foi usado. O trabalho é apenas didático e não serve para avaliar pessoas reais.

## Arquivos do repositório

| Arquivo | Conteúdo |
|---|---|
| `sistema_especialista_recrutas_militar_BRASIL_2027.ipynb` | Notebook comentado com o desenvolvimento completo, as respostas à leitura e a análise dos resultados |
| `dataset_recrutas_simulado.csv` | Dataset rotulado usado no treino e no teste (40 exemplos) |
| `README.md` | Este arquivo |

## Entradas, rótulo e saída

- **Atributos (X):** `taf_percentual` (desempenho no TAF, de 0 a 100) e `instrucao_percentual` (aproveitamento nas avaliações de instrução, de 0 a 100)
- **Rótulo (y):** `perfil`, com as classes `acompanhamento` e `autonomia`
- **Fato informado pelo instrutor:** `dificuldade_ordem_unida` (`True` ou `False`)
- **Saída:** a atividade recomendada, a regra aplicada e a justificativa

## Dataset

- **Tamanho:** 40 exemplos (21 de `autonomia` e 19 de `acompanhamento`)
- **Origem:** dados simulados, criados pelo grupo
- **Critério de rotulagem:** `autonomia` quando o recruta tem 60% ou mais no TAF **e** na instrução. Caso contrário, `acompanhamento`.
- **Ajuste manual:** 3 casos de fronteira (`rotulo_ajustado = sim`) foram rotulados por julgamento, para simular a subjetividade da rotulagem real

| Coluna | Tipo | Descrição |
|---|---|---|
| `id` | texto | Identificador do recruta simulado (R01 a R40) |
| `taf_percentual` | inteiro | Desempenho no TAF (0 a 100) |
| `instrucao_percentual` | inteiro | Aproveitamento nas avaliações de instrução (0 a 100) |
| `perfil` | texto | Rótulo: `acompanhamento` ou `autonomia` |
| `rotulo_ajustado` | texto | `sim` se o rótulo foi decidido por julgamento, `nao` se seguiu a regra dos 60% |

## Regras do sistema especialista

| Regra | Se (perfil previsto + fato) | Então (recomendação) |
|---|---|---|
| R1 | acompanhamento + dificuldade em ordem unida | Reforço de ordem unida com o instrutor |
| R2 | acompanhamento + sem dificuldade | Instrução supervisionada e revisão dos fundamentos |
| R3 | autonomia + dificuldade em ordem unida | Treino específico de ordem unida |
| R4 | autonomia + sem dificuldade | Função de auxiliar de instrução ou chefe de grupo |

As regras vêm da experiência do grupo com a formação de recrutas. Elas não foram aprendidas dos dados. A justificativa de cada uma está no notebook.

## Resultados

- **Modelo:** `DecisionTreeClassifier` com `max_depth=2`
- **Divisão:** 30 exemplos de treino e 10 de teste (`test_size=0.25`, `stratify=y`, `random_state=42`)
- **Acurácia no treino:** 93,3% (os 2 erros são casos de fronteira com rótulo ajustado manualmente)
- **Acurácia no teste:** 100% (10 de 10)

O 100% no teste **não** prova que o modelo funcionaria com dados reais: o teste tem só 10 casos, os dados são simulados e os rótulos seguem uma regra simples definida por nós. A análise completa, as limitações e os cuidados com dados pessoais (LGPD) estão nas seções 5.2 e 10 do notebook.

## Como executar

**No Google Colab (recomendado):**
1. Abra o notebook no [Google Colab](https://colab.research.google.com/) (Arquivo → Fazer upload de notebook, ou abrir direto do GitHub)
2. Vá em **Ambiente de execução → Executar tudo**

**Localmente:**
```bash
pip install pandas matplotlib scikit-learn jupyter
jupyter notebook sistema_especialista_recrutas_militar_BRASIL_2027.ipynb
```

Os dados já estão dentro do notebook, então o CSV não é necessário para rodar. Ele foi incluído como entrega separada do dataset.

## Tecnologias

Python, pandas, scikit-learn, matplotlib e Google Colab.

## Referências

- IBM. Guia de Aprendizado de Máquina: https://www.ibm.com/br-pt/think/machine-learning
- IBM. Aprendizado supervisionado: https://www.ibm.com/br-pt/think/topics/supervised-learning
- scikit-learn. DecisionTreeClassifier: https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html
- scikit-learn. train_test_split: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html
