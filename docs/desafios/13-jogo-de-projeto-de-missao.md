# 13 — Space Mission Design Game (Jogo de Projeto de Missões Espaciais)

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/>
  (lida em 14/11/2026)
- **Nível:** iniciante/jovem, intermediário
- **Temas:** jogos
- **Enunciado completo, em português:** [`13-enunciado-completo.md`](13-enunciado-completo.md).
  Esta ficha não repete o enunciado; ela reúne a identificação do desafio, os recursos e as
  perguntas para a escolha do grupo.

## Em uma frase

Criar um jogo interativo em que o participante projeta, gerencia e simula uma missão espacial
completa, tomando decisões de engenharia com recursos limitados e vendo como cada escolha afeta o
resultado.

## Dados e recursos indicados

Fonte principal: a aba Recursos da página oficial, lida em 14/11/2026 (impressão em PDF em
`assets/Resources.pdf`). Tradução integral em [`13-enunciado-completo.md`](13-enunciado-completo.md),
seção "Aba Recursos". A aba traz nove links, todos listados abaixo.

O PDF do evento (`assets/Recursos_Dados_NASA_Ceres_2026.pdf`, entregue pela organização local) traz
um subconjunto de quatro itens: Mission Viz, Mission Design Lab, Software NASA e Dataset JPL. Os dois
últimos são o GMAT e o dataset de maturidade de conceitos, pelos links idênticos da aba oficial. A
diferença entre os dois documentos foi verificada: a aba oficial é a lista completa.

### NASA

| Recurso | O que oferece | No PDF do evento? |
|---|---|---|
| [Design and Develop Science Missions](https://www.nasa.gov/wp-content/uploads/2025/04/250323-design-and-develop-science-mission.pdf?emrc=a454cf) | a abordagem de engenharia de sistemas e os quatro segmentos de uma missão: lançamento, espaço, solo e usuário | não |
| [GMAT](https://software.nasa.gov/software/GSC-19468-1) | software de código aberto para projeto, análise e otimização de trajetórias | sim, como "Software NASA" |
| [Concept Maturity Levels](https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=hdl:2014/44299) | escala do JPL para medir a maturidade de um conceito de missão | sim, como "Dataset JPL" |
| [Mission Design Lab](https://etd.gsfc.nasa.gov/capabilities/integrated-design-center/mission-design-lab/) | como a NASA desenvolve e avalia conceitos de missão, e as disciplinas que analisa | sim |
| [NASA Mission Viz](https://nasa.github.io/mission-viz/) | visualização 3D interativa de conceitos e trajetórias de missão | sim |
| [A Learning Game About Telescopes](https://science.nasa.gov/mission/webb/game-build-it-yourself/) (jogo "monte um telescópio espacial") | jogo educativo em três níveis: objetivos científicos determinam comprimentos de onda, instrumentos e óptica | não |
| [CubeSat 101](https://www3.nasa.gov/sites/default/files/atoms/files/nasa_csli_cubesat_101_508.pdf) | guia de conceitos e processos para quem desenvolve um CubeSat pela primeira vez | não |
| [Visualize a Space Mission Using Virtual Reality](https://www.spaceappschallenge.org/2023/challenges/visualize-a-space-mission-using-virtual-reality/) | desafio de 2023 do Space Apps sobre visualizar missões em realidade virtual; é referência, não dado | não |

### Agências parceiras

| Recurso | O que oferece | No PDF do evento? |
|---|---|---|
| [Digital Games and Activities (CSA)](https://www.asc-csa.gc.ca/eng/youth-educators/digital-games-and-activities.asp) | coleção de jogos digitais, e-books, vídeos e atividades práticas | não |

## Para a escolha do grupo

- **Público declarado:** estudantes e aspirantes a engenheiros.
- **Entrega esperada:** jogo ou simulação funcional.
- **Natureza dos dados:** os recursos são **documentos, ferramentas e exemplos**, não conjuntos
  de dados. O enunciado não indica de onde tirar os valores de massa, custo e consumo dos
  componentes, e aceita modelos de nave realistas ou simplificados
  ([enunciado completo](13-enunciado-completo.md), seção "Considerações potenciais").
- **Onde está a dificuldade** (leitura de quem resumiu): o escopo é o mais largo dos desafios
  de jogo. A lista de possibilidades é longa, e o multijogador para até quatro pessoas é uma
  parte técnica pesada. Escolher o que entra na primeira versão é a decisão principal.
- **Ponto de atenção:** o critério "Relevância" pede dado da NASA como parte central, e este
  desafio não indica um conjunto de dados. O grupo decidiu usar recursos da NASA (14/11/2026); falta
  escolher quais (pendência 7 em [`../pendencias.md`](../pendencias.md)).
- **Semelhança com outro desafio:** o [03](03-treinador-de-astronauta-junior.md) também pede
  jogo, com público de 7 a 12 anos e foco em operar uma base, não em projetar a missão.
- **Perguntas para o grupo responder antes de escolher:**
  - Multijogador: fica para depois da primeira versão ([ADR 0006](../adr/0006-multijogador-depois-da-primeira-versao.md)).
  - Quais recursos e quantos componentes entram?
  - De onde vêm os valores de massa, custo e energia de cada componente?
  - Como o jogo explica por que a missão falhou?
