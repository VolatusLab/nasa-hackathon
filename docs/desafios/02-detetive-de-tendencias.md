# 02 — Be An Earth System Trend Detective!

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/earth-system-trend-detective/>
  (lida em 14/11/2026)
- **Nível:** avançado
- **Temas:** ciências da Terra, software

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Criar uma ferramenta que escolhe variáveis de ciências da Terra, mostra como elas mudam ao longo
do tempo em uma região e diz se a tendência encontrada é estatisticamente significativa.

## Contexto

Instrumentos em satélites e modelos globais medem muitos aspectos do sistema terrestre: terra,
atmosfera e oceanos. Uma mudança que segue em uma direção ao longo do tempo (uma tendência)
revela os processos que a causam. Há dois complicadores: a quantidade enorme de variáveis
disponíveis, e o fato de a mesma variável poder subir em uma região e cair em outra, mesmo sob
o mesmo processo.

Fontes citadas no enunciado: os instrumentos MODIS, OMI, AIRS e GPM, e os modelos MERRA-2 e
GLDAS.

## O que é pedido

Uma resposta completa reúne quatro elementos:

1. **Identificar variáveis** de interesse que possam ter tendência.
2. **Obter os dados para uma região**, porque a maioria das tendências não é global.
3. **Gerar e visualizar uma série temporal** longa o bastante para análise estatística.
4. **Fazer uma análise estatística básica:** taxa de mudança no tempo e teste de significância,
   com métodos como teste t, teste de Mann-Kendall ou intervalos de confiança.

O enunciado nota que já existem ferramentas que geram séries temporais e pacotes que fazem o
teste de significância; cumprir o escopo é fazer **as duas coisas**, visualização e análise.

## O que o enunciado sugere considerar

- **Público:** estudantes de ensino médio e superior e pessoas com alguma base científica.
  Definições simples das variáveis ajudam muito.
- **Abordagem:** o usuário poderia responder a poucas perguntas sobre o que ou onde quer
  investigar, e a ferramenta buscaria as variáveis relacionadas. Exemplos de demonstração
  ajudam a entender o uso.
- **IA (opcional):** poderia ajudar a apontar dados com potencial de tendência em certa área.
- **Dados:** existem em resolução horária, de 3 horas, diária e mensal; **diária e mensal são
  as mais fáceis** de processar.
- Uma tendência é interessante mesmo sem atingir significância.
- Vale procurar ferramentas públicas de gráficos de dados hidrológicos de organizações externas,
  como o CUAHSI (o enunciado cita o nome, sem link).
- Tendências não lineares e remoção de ciclos sazonais estão **fora do escopo** imaginado;
  detectar e analisar tendências lineares já é um bom começo.

## Dados e recursos indicados

### NASA e outros órgãos dos EUA

| Recurso | O que oferece |
|---|---|
| [Giovanni](https://giovanni.gsfc.nasa.gov/) | menus com muitas variáveis; gera séries temporais e permite baixar os dados |
| [Hydrology Time Series](https://disc.gsfc.nasa.gov/information/tools?title=Hydrology%20Time%20Series) | séries temporais com dados hidrológicos |
| [AppEEARS](https://appeears.earthdatacloud.nasa.gov/) | acesso e transformação de dados geoespaciais de vários acervos federais, com séries temporais |
| [Climate Data Online (NOAA)](https://www.ncei.noaa.gov/cdo-web/) | acervo histórico global de tempo e clima, com ferramenta de mapa |
| [Artigo: séries temporais de clorofila SeaWiFS](https://ntrs.nasa.gov/api/citations/20090042747/downloads/20090042747.pdf) | exemplo de criação de série temporal e teste de significância |

### Agências parceiras e outros

| Recurso | O que oferece |
|---|---|
| [KNMI Climate Explorer](https://climexp.knmi.nl/) | ferramenta web para explorar, analisar e visualizar dados climáticos |
| [Artigo: testes estatísticos de tendência](https://medium.com/@snp.kriss/statistical-test-methods-to-detect-trends-in-time-series-data-b361a0ec530b) | métodos para testar tendência em série temporal |
| [Guia de significância estatística](https://www.statsig.com/perspectives/a-comprehensive-guide-to-statistical-significance) | introdução a testes de significância |
| [RADARSAT Constellation Mission (CSA)](https://donnees-data.asc-csa.gc.ca/en/dataset/rcm) | dados de radar canadenses para vigilância marítima, desastres e ecossistemas |
| [Geo.ca](http://geo.ca/) | informação geoespacial aberta do Canadá |
| [Missão SWOT (CSA)](https://www.asc-csa.gc.ca/eng/satellites/swot/) | informação sobre a missão que mede a elevação da água de lagos, rios e oceanos |
| [Monitoramento de ecossistemas do espaço (CSA)](https://www.asc-csa.gc.ca/eng/satellites/everyday-lives/monitoring-and-protecting-our-ecosystems-from-space.asp) | como dados de satélite ajudam a acompanhar mudanças |
| [Tutorial de SAR em Python (CSA)](https://github.com/asc-csa/Synthetic_Aperture_Radar_Tutorial) | passo a passo com Python e QGIS |

## Para a escolha do grupo

- **Público declarado:** estudantes e público com base científica.
- **Entrega esperada:** ferramenta de software com visualização e estatística.
- **Natureza dos dados:** séries temporais de satélite e de modelo; há ferramentas da NASA que
  já entregam a série pronta para download.
- **Onde está a dificuldade** (leitura de quem resumiu): só este e o
  [12](12-planeta-x-e-spherex.md) são marcados apenas como avançados. Exige estatística (regressão, teste de significância) aplicada
  corretamente; o critério "Validade" pesa sobre isso.
- **Perguntas para o grupo responder antes de escolher:**
  - Alguém do grupo domina teste de tendência e significância a ponto de explicar o resultado?
  - Conseguimos baixar uma série temporal de uma dessas fontes ainda hoje?
  - Quantas variáveis e regiões cabem no prazo?
