# 06 — Field Shift: Adapting Farms with NASA Data

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/adapting-farms-with-nasa-data/>
  (lida em 14/11/2026)
- **Nível:** intermediário, avançado
- **Temas:** artes e multimídia, ciências da Terra, software

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Criar uma ferramenta de apoio à decisão que combina observações da Terra feitas pela NASA com
informação local de solo, culturas e prioridades do produtor, para explorar estratégias de
rotação de culturas.

## Contexto

Produtores rurais lidam com temperatura em mudança, chuva menos previsível, falta de água,
erosão, perda de nutrientes, eventos extremos e solo em declínio. Escolher uma cultura nova
para a rotação é difícil: a que melhora o solo em um lugar pode, em outro, consumir água demais,
trazer doença, não ter mercado ou cair fora da estação de cultivo.

O desafio se inspira na experiência de famílias de agricultores de várias gerações. Os acervos
de longo prazo da NASA ajudam a entender as condições locais, e técnicas de IA ajudam a
traduzi-los em informação prática.

## O que é pedido

Um app, modelo, mapa interativo ou outra ferramenta que ajude o produtor a **explorar opções
de rotação** capazes de melhorar a saúde do solo e a resiliência a mudanças de clima e de água.

Conjuntos de dados que o enunciado nomeia: SMAP, ECOSTRESS, GPM, Landsat, MODIS, NASA POWER,
GRACE e GRACE-FO, e SRTM ou outros produtos de elevação. GRACE e GRACE-FO (água de longo prazo)
são citados no enunciado, mas a página de recursos não traz link para eles.

O enunciado descreve, sempre como possibilidade ("you may"):

- analisar padrões de temperatura, estresse por calor, chuva, umidade do solo, evaporação,
  risco de geada, chuva extrema, estresse da vegetação e tendências de água de longo prazo;
- considerar solo local, características das culturas e prioridades do produtor (uso de água,
  valor forrageiro, fixação de nitrogênio, redução de erosão, matéria orgânica, mercado);
- apontar períodos em que o campo fica descoberto, estações em que a cultura atual fica mais
  vulnerável e oportunidades de rotação;
- **comparar ao menos três estratégias de rotação, incluindo a atual**, e para cada uma
  explicar: por que foi sugerida, que evidência a sustenta, quais benefícios traz, onde falta
  informação e quais riscos pedem revisão local.

O resultado é uma ferramenta **de apoio**: aponta padrões e possibilidades, sem substituir o
julgamento do produtor nem o conhecimento agronômico local.

## O que o enunciado sugere considerar

- **Condições e dados:** relacionar clima e solo à vulnerabilidade da cultura; explicar termos
  como evapotranspiração, anomalia de umidade do solo, índices de vegetação (NDVI), risco de
  geada; deixar claro como a observação por satélite difere da medição em solo.
- **IA, modelagem e fusão de dados:** comparar abordagens; explicar como o modelo trata a
  incerteza e onde o conhecimento local precisa validar; harmonizar conjuntos com resoluções
  espaciais e temporais diferentes em uma grade comum.
- **Rotação:** comparar cenários por ciclagem de nutrientes, erosão, matéria orgânica, quebra
  de ciclo de pragas, uso de água, forragem e mercado; explicar o papel de culturas fixadoras de
  nitrogênio, de cobertura, de raiz profunda e tolerantes à seca.
- **Mapas e visualização:** tendências no tempo, vulnerabilidades por talhão, linhas do tempo,
  sobreposições e controles de cenário.
- **Desenho centrado no produtor:** fácil de interpretar para quem tem pouca experiência
  técnica; permitir que o produtor informe prioridades e restrições; lembrar que a ferramenta
  apoia, não substitui.

## Dados e recursos indicados

### NASA (missões e produtos)

| Recurso | O que oferece |
|---|---|
| [SMAP](https://www.earthdata.nasa.gov/data/platforms/space-based-platforms/smap) | umidade superficial do solo e estado de congelamento, a cada 2 a 3 dias, global |
| [GPM e IMERG](https://gpm.nasa.gov/data) | taxa e acumulado de precipitação, global |
| [Landsat](https://earthexplorer.usgs.gov/), [MODIS](https://lpdaac.usgs.gov/products/), [VIIRS](https://search.earthdata.nasa.gov/search?q=VIIRS) | refletância, NDVI e índices de vegetação (30 m no Landsat; 250 a 1000 m nos outros) |
| [NASA POWER](https://power.larc.nasa.gov/) | dados solares, meteorológicos e climatológicos de uso agrícola |
| [SRTM](https://www.earthdata.nasa.gov/data/instruments/srtm) | elevação global: declividade, escoamento, risco de erosão |
| [ECOSTRESS](https://ecostress.jpl.nasa.gov/data) | temperatura da superfície e evapotranspiração em alta resolução |
| [NLDAS/GLDAS](https://www.earthdata.nasa.gov/) | séries contínuas de temperatura, chuva, umidade do solo e radiação (buscar por "NLDAS" ou "GLDAS" no Earthdata Search) |
| [GEDI](https://gedi.umd.edu/data) | estrutura da vegetação por laser: altura de dossel, biomassa |

### Dados agrícolas e de solo dos EUA

Estes cobrem **os Estados Unidos ou parte deles** (o CoCoRaHS, a América do Norte).

| Recurso | O que oferece |
|---|---|
| [USDA Ag Data Commons](https://www.nal.usda.gov/services/agdatacommons) | conjuntos abertos de solo, culturas, clima e manejo |
| [Web Soil Survey](https://websoilsurvey.nrcs.usda.gov/app/) | mapas e propriedades oficiais de solo |
| [Cropland Data Layer / CropScape](https://nassgeodata.gmu.edu/CropScape/) | classificação anual de culturas, 30 m |
| [PRISM](https://prism.oregonstate.edu/) | clima diário, mensal e normais de 30 anos |
| [SSURGO / STATSGO2](https://www.nrcs.usda.gov/resources/data-and-reports/soils) | atributos detalhados de solo |
| [NAIP](https://naip-usdaonline.hub.arcgis.com/) | imagens aéreas de cerca de 1 m |
| [NLCD](https://www.usgs.gov/centers/eros/science/national-land-cover-database) | cobertura e uso da terra, 30 m, várias décadas |
| [CoCoRaHS](https://www.cocorahs.org/Maps) | chuva diária medida por voluntários (América do Norte) |
| [USGS NWIS](https://waterdata.usgs.gov/nwis) | água subterrânea, vazão e qualidade da água |
| [USDA AMS Market News](https://www.ams.usda.gov/market-news) | preços e condições de mercado |
| [USDA NASS QuickStats](https://quickstats.nass.usda.gov/) | estatísticas agrícolas por condado e estado |
| [OpenET](https://openetdata.org/) | evapotranspiração por talhão (oeste dos EUA) |
| [LANDFIRE](https://www.landfire.gov/) | tipo e condição da vegetação |

### Globais e de agências parceiras

| Recurso | O que oferece |
|---|---|
| [FAO GAEZ](https://gaez.fao.org/) | aptidão agroclimática global para dezenas de culturas, restrições de solo, potencial de produtividade |
| [Copernicus Sentinel-2 (ESA)](https://dataspace.copernicus.eu/) | imagens multiespectrais de 10 a 20 m, com revisita frequente |
| [ERA5 (ECMWF)](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview) | reanálise global horária de clima |

## Para a escolha do grupo

- **Público declarado:** produtores rurais, inclusive com pouca experiência técnica.
- **Entrega esperada:** ferramenta de apoio à decisão (app, modelo ou mapa interativo).
- **Natureza dos dados:** é o desafio com mais fontes indicadas. Os dados da NASA são globais;
  os de solo, cultura e mercado são quase todos dos Estados Unidos. A exceção é o FAO GAEZ,
  global (aptidão de culturas e restrições de solo).
- **Onde está a dificuldade** (leitura de quem resumiu): juntar fontes de resolução diferente e
  sustentar cada sugestão de rotação com evidência. Para uma área fora dos EUA, há o GAEZ em
  escala global; dado local mais detalhado de solo e cultura teria de vir de outra fonte, que o
  grupo precisaria encontrar e citar.
- **Ponto de atenção:** recomendação agronômica sem fonte fere o critério "Validade". O
  enunciado sugere que a ferramenta explicite lacunas e riscos.
- **Perguntas para o grupo responder antes de escolher:**
  - Para qual região a ferramenta é feita, e de onde vem o dado local de solo e cultura?
  - Alguém do grupo conhece rotação de culturas ou tem acesso a quem conheça?
  - Quais das fontes da NASA dá para acessar e usar ainda hoje?
