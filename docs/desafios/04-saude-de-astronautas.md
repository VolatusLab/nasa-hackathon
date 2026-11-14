# 04 — Create Health Monitoring Software for Astronauts on Space Missions

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/health-monitoring-software/>
  (lida em 14/11/2026)
- **Nível:** intermediário
- **Temas:** exploração humana, software, exploração espacial

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Construir um software que reúne indicadores de saúde e ajuda o astronauta a avaliar o próprio
estado e a agir durante a missão.

## Contexto

Missões mais longas expõem os astronautas por mais tempo a um ambiente hostil. O programa de
pesquisa humana da NASA mapeou os **cinco perigos do voo espacial humano**: radiação espacial,
isolamento e confinamento, distância da Terra, campos de gravidade e ambientes fechados
hostis. Eles contribuem para alterações do sistema imune, perda de densidade óssea, eventos
cardiovasculares, nutrição inadequada e problemas de saúde comportamental.

Em missões longas, o próprio astronauta precisa perceber essas mudanças. Indicadores citados
como úteis: pressão arterial, frequência cardíaca, glicemia, temperatura corporal, horas de
sono e humor.

## O que é pedido

Uma **ferramenta visual** que ajude o astronauta a avaliar a própria saúde e oriente sobre
tratamentos e melhorias.

- A entrada de dados pode ser qualquer uma: texto, cliques, imagem de câmera.
- Qualquer dado serve, desde que represente um indicador de saúde (o enunciado cita glicemia em
  mg/dL e imagens de ultrassom).
- Perguntas que o enunciado propõe como guia: quais medições dá para fazer no espaço? Por que
  o exame é necessário? Como os perigos do voo afetam cada indicador? Quando um resultado pede
  atenção da tripulação ou dos médicos em solo? O que fazer para evitar uma condição crítica?
- O desenho da interface tem papel importante. Exemplo citado: uma figura humana em que cada
  parte do corpo é clicável e mostra função e estado de saúde.

## O que o enunciado sugere considerar

- Servir a ambientes diferentes: nave, estação, rover, base em outro planeta ou lua.
- Lembrar o astronauta de fazer medições ou tarefas como parte da rotina.
- Recursos possíveis: gamificação para engajar nas tarefas de saúde, gráficos dinâmicos da
  evolução dos indicadores, código de cores para leitura rápida.
- Não presumir que o astronauta sabe avaliar a própria saúde: dar instruções e explicações
  simples sobre medições, indicadores e riscos.

## Dados e recursos indicados

### NASA

| Recurso | O que oferece |
|---|---|
| [5 Hazards of Human Spaceflight](https://www.nasa.gov/hrp/hazards/) | informação básica sobre os cinco perigos, com links para artigos e relatórios |
| [Risks of Human Spaceflight](https://www.nasa.gov/hrp/risks/) | os principais riscos para humanos em missão, com links para relatórios |
| [Ongoing HRP Research in Space](https://www.nasa.gov/hrp/ongoing-hrp-research/) | artigos das pesquisas em andamento |

### Agências parceiras

| Recurso | O que oferece |
|---|---|
| [Monitoramento de radiação para a saúde de astronautas (CSA)](https://www.asc-csa.gc.ca/eng/news/articles/2026/2026-02-26-monitoring-radiation-astronaut-health.asp) | tecnologias e pesquisas canadenses para medir a exposição à radiação |
| [Por que fazer experimentos no espaço? (CSA)](https://www.asc-csa.gc.ca/eng/iss/science/why-do-we-conduct-science-experiments-in-space.asp) | como a pesquisa na estação espacial avança o conhecimento sobre saúde humana |

## Para a escolha do grupo

- **Público declarado:** astronautas em missão.
- **Entrega esperada:** software com interface visual.
- **Natureza dos dados:** os recursos indicados são **artigos e relatórios**, não conjuntos de
  dados numéricos prontos. Os valores de saúde vêm da entrada do usuário.
- **Onde está a dificuldade** (leitura de quem resumiu): a parte de software é acessível, mas
  toda faixa de referência, alerta e orientação precisa de fonte. Inventar limite clínico fere
  o critério "Validade" e a regra do repositório de não inventar número. Também é preciso
  mostrar onde o dado da NASA entra de forma central (critério "Relevância").
- **Perguntas para o grupo responder antes de escolher:**
  - De onde vêm as faixas de referência de cada indicador, e quem confere?
  - Quais dos cinco perigos a ferramenta cobre?
  - Como o uso de recurso da NASA aparece dentro do produto, e não só nos slides?
