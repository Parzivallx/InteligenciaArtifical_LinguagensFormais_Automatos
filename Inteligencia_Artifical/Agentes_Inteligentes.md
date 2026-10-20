# 📘 Atividade — Agentes Inteligentes

> **Disciplina:** Inteligência Artificial, Linguagens Formais e Autômatos  
> **Instituição:** UDF  
> **Aula:** 19/10/2026  
> **Professora:** Kadidja Valéria  
> **Estudante:** Emmanuel Ferreira Gomes  
> **Turma:** 2267209

## 🎯 Objetivo

Resolver os exercícios 2.3, 2.4 e 2.5 do capítulo 2, sobre agentes inteligentes, apresentando justificativas, exemplos e a classificação dos ambientes.

---

## 📝 Exercício 2.3 — Verdadeiro ou falso

### a) Falso
Um agente pode agir de forma racional mesmo sem ter acesso a todas as informações do ambiente. Ele precisa tomar a melhor decisão possível com os dados disponíveis.

**Exemplo:** um aplicativo de navegação escolhe uma rota usando as informações de trânsito que consegue obter.

### b) Verdadeiro
Um agente puramente reativo não utiliza informações de situações anteriores para decidir suas ações.

**Exemplo:** um robô que lembra quais corredores já percorreu consegue evitar caminhos repetidos.

### c) Verdadeiro
Se todas as ações possíveis geram o mesmo resultado, não faz diferença qual delas o agente escolhe.

**Exemplo:** um sistema em que todos os botões disponíveis geram a mesma pontuação.

### d) Falso
A função do agente considera o histórico de percepções, enquanto o programa é a implementação dessa função e pode utilizar memória interna.

**Exemplo:** um robô pode guardar a informação de que já tentou abrir uma porta.

### e) Falso
Nem toda função de agente pode ser implementada por um programa, pois existem funções que não podem ser computadas.

**Exemplo:** o problema da parada mostra que não existe um algoritmo geral capaz de determinar se qualquer programa vai terminar.

### f) Verdadeiro
Escolher uma ação aleatoriamente pode ser racional quando todas as opções apresentam o mesmo resultado esperado.

**Exemplo:** escolher entre duas rotas com o mesmo custo e tempo estimado.

### g) Verdadeiro
Uma mesma função de agente pode ser racional em ambientes diferentes, dependendo das condições e dos resultados esperados.

**Exemplo:** um organizador de arquivos pode funcionar bem em computadores diferentes.

### h) Falso
Mesmo quando o ambiente não pode ser totalmente observado, algumas ações ainda podem ser melhores que outras.

**Exemplo:** ligar um aquecedor sem verificar a temperatura pode ser desnecessário ou perigoso.

### i) Falso
Um agente racional pode perder mesmo tomando uma boa decisão, porque o resultado também depende de fatores desconhecidos.

**Exemplo:** no pôquer, um jogador pode fazer uma aposta matematicamente vantajosa e ainda perder a rodada.

---

## 🤖 Exercício 2.4 — Ambientes e agentes

### 1. ⚽ Jogador de futebol

**Agente:** jogador de futebol.

**PEAS:**
- **Desempenho:** vencer a partida, marcar gols e realizar bons passes.
- **Ambiente:** campo, bola, companheiros, adversários e árbitro.
- **Atuadores:** pernas, pés, cabeça e movimentos do corpo.
- **Sensores:** visão, audição, tato e percepção corporal.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Multiagente |
| Determinismo | Estocástico e estratégico |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo e discreto |
| Conhecimento | Parcialmente conhecido |

### 2. 🌊 Exploração dos oceanos subterrâneos de Titã

**Agente:** submarino autônomo hipotético.

**PEAS:**
- **Desempenho:** mapear o ambiente, coletar amostras e economizar energia.
- **Ambiente:** oceano subterrâneo, gelo, rochas e correntes.
- **Atuadores:** propulsores, braços mecânicos e coletor de amostras.
- **Sensores:** sonar, câmeras, sensores de pressão e temperatura.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Um agente |
| Determinismo | Estocástico |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo e discreto |
| Conhecimento | Desconhecido |

### 3. 📚 Compra de livros usados de IA pela internet

**Agente:** sistema de compra automatizada.

**PEAS:**
- **Desempenho:** encontrar livros adequados pelo menor custo possível.
- **Ambiente:** sites, anúncios, vendedores, compradores e transportadoras.
- **Atuadores:** pesquisar, filtrar, comparar e realizar compras autorizadas.
- **Sensores:** preços, fotos, descrições, avaliações e disponibilidade.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Multiagente |
| Determinismo | Estocástico e estratégico |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo e discreto |
| Conhecimento | Parcialmente conhecido |

### 4. 🎾 Jogador de tênis contra outra pessoa

**Agente:** jogador de tênis.

**PEAS:**
- **Desempenho:** ganhar pontos, games e partidas.
- **Ambiente:** quadra, bola, rede, raquete e adversário.
- **Atuadores:** braços, pernas e raquete.
- **Sensores:** visão, audição, tato e percepção corporal.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Multiagente competitivo |
| Determinismo | Estocástico e estratégico |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo e discreto |
| Conhecimento | Parcialmente conhecido |

### 5. 🎾 Jogador de tênis contra uma parede

**Agente:** jogador treinando sozinho.

**PEAS:**
- **Desempenho:** manter a sequência de rebatidas e melhorar a precisão.
- **Ambiente:** quadra, parede, bola e raquete.
- **Atuadores:** braços, pernas e raquete.
- **Sensores:** visão, audição, tato e percepção corporal.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável na prática |
| Número de agentes | Um agente |
| Determinismo | Aproximadamente determinístico em condições ideais |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Predominantemente contínuo |
| Conhecimento | Aproximadamente conhecido |

### 6. 🏃 Salto em altura

**Agente:** atleta.

**PEAS:**
- **Desempenho:** ultrapassar a barra sem derrubá-la.
- **Ambiente:** pista, barra, colchão e condições climáticas.
- **Atuadores:** pernas, braços e movimentos do corpo.
- **Sensores:** visão, equilíbrio, tato e percepção corporal.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Um agente durante a execução do salto |
| Determinismo | Estocástico na prática |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo |
| Conhecimento | Aproximadamente conhecido |

### 7. 💰 Participação em um leilão

**Agente:** sistema automatizado de compra.

**PEAS:**
- **Desempenho:** conseguir o item por um preço adequado.
- **Ambiente:** plataforma, item, vendedor, concorrentes e prazo.
- **Atuadores:** enviar lances, consultar informações e encerrar a participação.
- **Sensores:** preço atual, histórico público, notificações e tempo restante.

| Propriedade | Classificação |
|---|---|
| Observabilidade | Parcialmente observável |
| Número de agentes | Multiagente competitivo |
| Determinismo | Estratégico e incerto |
| Episódico ou sequencial | Sequencial |
| Dinâmica | Dinâmico |
| Discreto ou contínuo | Contínuo e discreto |
| Conhecimento | Parcialmente conhecido |

### Comparação dos ambientes

- **Tênis contra uma pessoa e contra uma parede:** contra uma pessoa, o agente precisa considerar as estratégias do adversário. Contra a parede, a resposta depende principalmente da trajetória da bola e das condições físicas.
- **Compra de livros usados:** o agente pode não conhecer o estado real do livro, a confiabilidade do vendedor ou possíveis mudanças no preço e no estoque.
- **Futebol e leilão:** as decisões de outros agentes influenciam diretamente o resultado. No futebol, isso acontece pelas ações dos jogadores; no leilão, pelos lances dos concorrentes.

---

## 📖 Exercício 2.5 — Conceitos de agentes inteligentes

### 1. Agente
É algo que percebe o ambiente e realiza ações para alcançar algum resultado.

**Exemplo:** um robô que identifica obstáculos e desvia deles.

### 2. Função do agente
Relaciona as percepções recebidas pelo agente às ações que ele deve realizar.

**Exemplo:** ao detectar um obstáculo, o robô decide mudar de direção.

### 3. Programa do agente
É a implementação que permite ao agente escolher suas ações com base nas percepções e, quando necessário, na memória.

**Exemplo:** um programa que controla os movimentos de um robô.

### 4. Racionalidade
É escolher a ação mais adequada considerando as informações disponíveis e o resultado esperado.

**Exemplo:** um GPS que escolhe a rota com menor tempo estimado.

### 5. Autonomia
É a capacidade de agir com base nas próprias percepções e experiências, sem depender totalmente de instruções externas.

**Exemplo:** um aspirador robô que limpa a casa sozinho.

### 6. Agente reativo
Escolhe ações com base na percepção atual, sem precisar considerar um histórico de situações anteriores.

**Exemplo:** uma luz que acende quando detecta movimento.

### 7. Agente baseado em modelo
Mantém uma representação interna do ambiente para ajudar nas decisões.

**Exemplo:** um robô que registra os locais onde já encontrou obstáculos.

### 8. Agente baseado em objetivos
Escolhe ações pensando em alcançar um objetivo definido.

**Exemplo:** um GPS que calcula um caminho até o destino.

### 9. Agente baseado em utilidade
Compara as alternativas e escolhe aquela que oferece o resultado mais vantajoso segundo seus critérios.

**Exemplo:** um aplicativo que considera tempo, distância e custo para recomendar uma rota.

### 10. Agente de aprendizagem
Melhora seu comportamento com base nas experiências e nos resultados anteriores.

**Exemplo:** um sistema de recomendações que aprende com as preferências do usuário.

---

## 🔄 Síntese de autômato — Compra de livros usados

**Cenário:** um agente automatizado procura e compra livros usados de Inteligência Artificial.

### Estados internos
- **E1 — Busca:** procura anúncios disponíveis.
- **E2 — Avaliação:** compara preço e condições do livro.
- **E3 — Finalizado:** registra a compra concluída.

### Percepções
- **P1:** anúncio encontrado.
- **P2:** oferta dentro do orçamento e adequada aos critérios.
- **P3:** pagamento confirmado.

### Ações
- **A1:** pesquisar anúncios.
- **A2:** avaliar a oferta e realizar a compra autorizada quando aprovada.
- **A3:** registrar a compra e encerrar o processo.

### Regras de transição

1. `E1 + P1 → E2 / A2`: ao encontrar um anúncio, o agente passa para a avaliação da oferta.
2. `E2 + P3 → E3 / A3`: após a confirmação do pagamento, o agente registra a compra e encerra o processo.

O estado interno permite que o agente saiba em qual etapa está e utilize informações obtidas anteriormente. Uma limitação desse modelo é que ele não representa todas as situações possíveis, como cancelamentos, problemas na entrega ou devoluções.

---

## 📚 Referências

- RUSSELL, Stuart; NORVIG, Peter. *Inteligência Artificial: uma abordagem moderna*. Capítulo 2 — Agentes inteligentes.
- VALÉRIA, Kadidja. *Agentes Inteligentes*. Material de aula de 19 de outubro de 2026, UDF.
