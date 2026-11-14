# 08 — Harmonization of MODIS and VIIRS Hot Spots

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/modis-and-viirs-hot-spots/>
  (lida em 14/11/2026)
- **Nível:** intermediário, avançado
- **Temas:** ciências da Terra, software

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Construir uma aplicação web que harmoniza os registros de focos de calor dos sensores MODIS e
VIIRS em um calendário de atividade de queima para uma área escolhida pelo usuário.

## Contexto

**Regimes de fogo.** Alguns ecossistemas precisam de fogo periódico. Mas mudanças na
intensidade, extensão e frequência prejudicam clima, sociedade e biodiversidade, além de causar
mortes, perdas materiais e risco para quem combate. A atividade de queima inclui incêndios em
vegetação natural e queimas de origem humana (agricultura, limpeza de terreno, lixo, indústria).

**Detecção por satélite.** Sensores no infravermelho médio e termal detectam pontos quentes na
superfície. MODIS e VIIRS fornecem detecção de anomalia termal em tempo real. Um ponto quente
nem sempre é incêndio em vegetação: pode vir de fogo urbano, erupção vulcânica ou processo
industrial, como a queima de gás em campos de petróleo.

**O problema.** Os sensores MODIS (satélites Terra e Aqua) têm mais de duas décadas de
observações, mas estão no fim da vida operacional e vêm sendo substituídos pelo VIIRS. Os dois
registros **não são diretamente comparáveis**: têm resolução espacial, sensibilidade e horários
de observação diferentes. Sem harmonização, o gestor não tem um retrato consistente de quando e
onde houve queima.

**Calendário de queima.** Junta histórico e dado recente para mostrar de relance padrões
sazonais, anomalias e tendências: quais meses e anos tiveram mais fogo, e como o mês atual se
compara com a mediana histórica da área.

## O que é pedido

Um **calendário harmonizado de atividade de queima**, baseado em focos ativos, dentro de uma
aplicação web. O enunciado propõe duas partes:

1. **Harmonização** dos focos MODIS e VIIRS, de modo que, ao fim, o sensor de origem deixe de
   importar e o foco passe a ser o padrão, a tendência e a anomalia.
2. **Aplicação web** que recebe os focos harmonizados. O usuário escolhe uma região e um
   intervalo de datas e baixa análises e visualizações.

O calendário mostraria o número de focos detectados do início dos anos 2000 até hoje: quais
épocas do ano têm mais fogo, quais anos queimaram mais e como um incêndio atual se compara com
os anteriores.

Complementos citados: rampas de cor para mostrar semelhanças e diferenças entre meses, e um
arquivo CSV para download com os focos da busca.

O enunciado sugere como base os focos do FIRMS (NASA Earthdata).

## O que o enunciado sugere considerar

- **Público:** equipes de alerta e resposta a emergências, cientistas, gestores de terras e
  bombeiros.
- Interatividade: mapa em que o usuário desenha a área de interesse, ou campo para latitude e
  longitude.
- Rampas de cor acessíveis.
- Poucos índices e números-chave, bem visualizados: comparações históricas, anomalias em relação
  a médias de vários anos, número de incêndios detectados e registrados.

## Dados e recursos indicados

| Recurso | O que oferece |
|---|---|
| [FIRMS (NASA Earthdata)](https://www.earthdata.nasa.gov/data/tools/firms) | imagens de satélite quase em tempo real, focos ativos e produtos relacionados, com cobertura global; dados e serviços geoespaciais para a comunidade de manejo do fogo |

É o único recurso listado. A página não lista recursos de agências parceiras, mas a imagem do
desafio é creditada à agência espacial argentina (CONAE).

## Para a escolha do grupo

- **Público declarado:** resposta a emergências, cientistas, gestores e bombeiros.
- **Entrega esperada:** aplicação web com mapa, calendário e download.
- **Dado obrigatório:** focos MODIS e VIIRS. O FIRMS é a fonte que o enunciado sugere.
- **Natureza dos dados:** pontos com data, posição e atributos, em tabela; cobertura global, o
  que inclui o Brasil.
- **Onde está a dificuldade** (leitura de quem resumiu): a parte web é direta; o núcleo
  científico é o **método de harmonização**, que o enunciado não define. O grupo precisa
  propor um método, justificá-lo e mostrar que ele funciona. É aí que entram os critérios
  "Validade" e "Criatividade".
- **Escopo bem delimitado:** o enunciado diz com clareza o que a aplicação recebe, mostra e
  exporta.
- **Perguntas para o grupo responder antes de escolher:**
  - Como comparar dois sensores com resolução, sensibilidade e horários de observação diferentes?
  - Conseguimos baixar focos históricos do FIRMS para uma área ainda hoje? Precisa de chave?
  - Que volume de dados a aplicação aguenta para o período de 2000 até hoje?
