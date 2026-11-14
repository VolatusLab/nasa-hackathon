# 05 — Dancing with the SARs

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/dancing-with-the-sars/>
  (lida em 14/11/2026)
- **Nível:** intermediário, avançado
- **Temas:** ciências da Terra

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Construir uma aplicação interativa que usa dados de radar da missão NISAR (NASA e ISRO) para
acompanhar e visualizar um ou mais tipos de mudança na superfície da Terra.

## Contexto

A maioria dos sensores em órbita usa a luz do Sol refletida (sensoriamento passivo). O radar é
**ativo**: emite a própria energia, na faixa de micro-ondas, e mede o retorno. O radar de
abertura sintética (SAR) combina várias aquisições de uma antena curta para simular uma antena
longa e ganhar resolução.

Por que importa:

- funciona de dia, de noite e com nuvens, o que serve a desastres (derramamento de óleo,
  incêndio, furacão);
- é sensível à **rugosidade** e à **constante dielétrica**, o que revela estrutura, geometria
  e material da superfície;
- destaca água, áreas alagadas e umidade do solo;
- mede movimento fino do terreno, em centímetros (terremotos, subsidência).

## O que é pedido

Três passos descritos no enunciado:

1. **Escolher uma área de estudo:** a própria cidade, uma área úmida tropical, um manto de
   gelo, um incêndio florestal, um bairro alagado, uma erupção vulcânica.
2. **Baixar dados NISAR** gratuitos pelas fontes indicadas, e dados complementares se quiser
   (imagem óptica, camadas de GIS) para dar contexto.
3. **Apresentar os achados** em meio digital interativo e **levantar hipóteses** sobre o que
   causa o que se vê (ou não se vê) nos dados. Perguntas do enunciado: quais polarizações
   destacam essas mudanças em terra e no gelo? Que aplicações futuras do NISAR são possíveis?

O resultado desejado é uma solução **de código aberto**, fácil de usar, que traduza observações
de radar em informação acionável para cientistas, gestores, educadores e público. Exemplos
citados: mapas interativos de detecção de mudança, animações de série temporal, painéis.

Tipos de mudança mencionados: áreas úmidas e várzeas, desmatamento e incêndios, lavouras,
umidade do solo, geleiras e gelo marinho, deformação por terremoto e subsidência costeira.

## O que o enunciado sugere considerar

- Analisar polarizações diferentes do NISAR e frequências de outros sensores.
- Baixar datas diferentes para montar série temporal, e dados auxiliares (população, tipo de
  vegetação) para contexto.
- Mostrar como a ação humana (agricultura, indústria) afeta os recursos naturais.
- Narrativa forte por meio das visualizações. O resumo pode ser relatório, vídeo, slides ou
  mapa narrativo.
- Se o grupo conhece a área (é a própria cidade), trazer contexto e histórias locais.
- Tornar o resumo interativo: controle deslizante de imagens, mapas web.

## Dados e recursos indicados

### NASA

| Recurso | O que oferece |
|---|---|
| [Earthdata Search](https://search.earthdata.nasa.gov/search) | busca, comparação, visualização e acesso ao acervo de ciências da Terra |
| [ASF Data Search Vertex](https://search.asf.alaska.edu/) | acervo de dados SAR da NASA, operado pela Alaska Satellite Facility |
| [Guia do usuário de dados NISAR](https://nisar-docs.asf.alaska.edu/) | tudo sobre acesso e uso dos dados NISAR |
| [Introdução a sensoriamento remoto](https://www.earthdata.nasa.gov/learn/earth-observation-data-basics/remote-sensing) | conceitos básicos |
| [Introdução a SAR](https://www.earthdata.nasa.gov/learn/earth-observation-data-basics/sar) | frequência, comprimento de onda, polarização, espalhamento |
| [Treinamentos ARSET](https://appliedsciences.nasa.gov/get-involved/training) | cursos online, com material de SAR e NISAR em inglês e espanhol |
| [NISAR StoryMaps](https://nisar.jpl.nasa.gov/applications/arcgis-storymaps/) | aplicações de SAR em cheias, incêndios, subsidência, manchas de óleo e geleiras |
| [White papers de aplicações do NISAR](https://nisar.jpl.nasa.gov/applications/societal-benefit/) | resumos de duas páginas por aplicação |
| [UAVSAR Postcards](https://uavsar.jpl.nasa.gov/education/postcards.html) | composições em falsa cor de dados SAR aerotransportados |

### Agências parceiras

| Recurso | O que oferece |
|---|---|
| [RADARSAT Constellation Mission (CSA)](https://donnees-data.asc-csa.gc.ca/en/dataset/rcm) | três satélites de radar canadenses |
| [Tutorial de SAR em Python (CSA)](https://github.com/asc-csa/Synthetic_Aperture_Radar_Tutorial) | passo a passo com Python e QGIS |
| [RADARSAT-1 (CSA)](https://donnees-data.asc-csa.gc.ca/en/dataset/radarsat1) | acervo histórico sob licença aberta |
| [Catálogo SAOCOM (CONAE, Argentina)](https://catalogos.conae.gov.ar/catalogo/catalogoSatSaocomInfo.html) | missão SAR argentina, com tutoriais; exige cadastro |
| [Cadastro no catálogo SAOCOM](https://www.argentina.gob.ar/noticias/la-informacion-saocom-cada-vez-mas-accesible) | protocolo de registro |

## Para a escolha do grupo

- **Público declarado:** cientistas, gestores de recursos, educadores, tomadores de decisão e
  público geral.
- **Entrega esperada:** aplicação interativa de código aberto.
- **Dado obrigatório:** NISAR. É um dos desafios que amarram a entrega a uma missão
  específica.
- **Natureza dos dados:** produtos de radar, em formato e volume especializados; pedem
  ferramentas próprias de geoprocessamento.
- **Onde está a dificuldade** (leitura de quem resumiu): a curva de aprendizado de SAR. Baixar,
  abrir e interpretar um produto NISAR é o primeiro obstáculo, antes de qualquer interface.
  Pede também hipótese física sobre o que causa a mudança observada.
- **Ponto a favor citado no enunciado:** a área pode ser a região do próprio grupo, com
  contexto e histórias locais.
- **Perguntas para o grupo responder antes de escolher:**
  - Existe cobertura NISAR da área que queremos, nas datas que queremos?
  - Conseguimos baixar e abrir um produto ainda hoje?
  - Alguém já trabalhou com imagem de satélite ou GIS?
  - O "código aberto" pedido combina com a decisão sobre licença e repositório público?
