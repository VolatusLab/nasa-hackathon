# 14 — The Earth Information Jukebox

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/the-earth-information-jukebox/>
  (lida em 14/11/2026)
- **Nível:** iniciante/jovem, intermediário
- **Temas:** artes e multimídia, ciências da Terra, software

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Construir uma "jukebox da Terra": interface, script ou aplicação que associa as visualizações do
Earth Information Center (EIC) da NASA a sons gerados dinamicamente a partir delas.

## Contexto

O EIC produz visualizações de como o planeta muda, da temperatura global às correntes oceânicas.
Essa informação é quase toda **visual**, o que limita o acesso de pessoas cegas ou com baixa
visão e restringe a forma como o público interage com a ciência da Terra.

**Sonificação** é a tradução de dados em som (áudio que não é fala). Ela abre uma experiência
multissensorial, pode revelar padrões sutis que o olho não percebe e cria uma ligação emocional
com o tema.

## O que é pedido

Uma experiência em que a pessoa escolhe ou acompanha uma visualização do EIC junto com a
paisagem sonora correspondente. Dois caminhos são aceitos:

- uma **ferramenta interativa** que traduz o dado visual em som; ou
- uma **coleção curada de áudios originais gerados**, que conte a história sonora dos dados,
  acompanhada da explicação do processo criativo.

A abertura do enunciado fala em sonificação gerada em tempo real; os objetivos aceitam também a
coleção de áudios gerados.

Formas de entrega citadas: jukebox web interativa, aplicativo de desktop, endpoint de API, ou
playlist de áudios gerados com a explicação.

O método de tradução é livre. O enunciado cita, como exemplos, visão computacional para mapear
espectro de cor em acordes, algoritmos que traduzem densidade de pixels em ritmo e conjuntos de
regras artísticas que controlam um sintetizador. Pede equilíbrio entre interpretação dos dados e
um resultado musicalmente agradável.

## O que o enunciado sugere considerar

**Conceitos**

- Muitas visualizações do EIC são sequências animadas; dá para extrair quadros individuais como
  base da geração de áudio.

**A experiência**

- Se for ferramenta interativa: o quão intuitivo é escolher uma visualização e iniciar o áudio.
- **Acessibilidade é tema central:** compatibilidade com leitor de tela, resposta tátil, texto
  descritivo rico acompanhando o áudio.

**Tradução dos dados**

- Mapear elementos visuais (cor, brilho, formas, densidade de pixels) em parâmetros de áudio
  (altura, ritmo, andamento, volume, instrumentação).
- Tradução direta de pixel para som pode virar ruído caótico; escalas, harmonias e regras
  artísticas ajudam.
- Disciplinas possíveis: visão computacional, aprendizado de máquina, sintetizadores, estações
  de áudio digital.

**Contar a história**

- Documentar o processo: o porquê das escolhas artísticas e os algoritmos usados.
- Pensar no impacto emocional dos dados.

## Dados e recursos indicados

Todos da NASA, do Scientific Visualization Studio (SVS). A página não lista recursos de agências
parceiras para este desafio.

| Recurso | O que oferece |
|---|---|
| [Banco de conteúdo do EIC](https://svs.gsfc.nasa.gov/gallery/earth-information-center/) | vídeos e imagens usados nos painéis do EIC, que podem servir de dado para gerar o áudio |
| [Sonificação de dados: Caldwell 73](https://svs.gsfc.nasa.gov/13786/) | exemplo de como a NASA converte imagem em som (brilho e posição em volume e altura) |
| [Mudança nas luzes noturnas, 2012 a 2023](https://svs.gsfc.nasa.gov/5313/) | iluminação urbana no globo; alto contraste |
| [Correntes e temperatura da superfície do mar](https://svs.gsfc.nasa.gov/3912/#media_group_349716) | movimento fluido e gradientes de temperatura |
| [Aerossóis GEOS](https://svs.gsfc.nasa.gov/5669/) | fumaça, poeira e partículas por tipo, em camadas |
| [Rodadas de modelo de qualidade do ar](https://svs.gsfc.nasa.gov/5533/) | quadros de alta resolução para download |
| [Perpetual Ocean 2: correntes de contorno oeste](https://svs.gsfc.nasa.gov/5425/) | mapas de alto contraste das grandes correntes |
| [Dióxido de carbono global (DYAMOND)](https://svs.gsfc.nasa.gov/5196/) | concentração de CO2 mudando no tempo |
| [Relâmpagos detectados da ISS, 2017 a 2023](https://svs.gsfc.nasa.gov/5011/) | eventos pontuais e rápidos |
| [Rio atmosférico em 3D](https://svs.gsfc.nasa.gov/4960/) | trajetória e densidade de umidade |
| [Altura de florestas (GEDI)](https://svs.gsfc.nasa.gov/4950/) | mapas globais de altura de dossel |

## Para a escolha do grupo

- **Público declarado:** público geral, com atenção a pessoas cegas e com baixa visão.
- **Entrega esperada:** ferramenta interativa **ou** coleção de áudios com explicação.
- **Dado obrigatório:** visualizações do EIC.
- **Natureza dos dados:** vídeos e imagens prontos, com download direto. Não há acervo
  científico bruto para processar.
- **Onde está a dificuldade** (leitura de quem resumiu): fazer o som ser ao mesmo tempo fiel ao
  dado e agradável de ouvir, e sustentar a acessibilidade de verdade (uma interface de
  sonificação que não funciona com leitor de tela contradiz o tema). Pede algum conhecimento de
  áudio ou música.
- **Ponto a favor:** os dados já estão prontos para uso, e o enunciado aceita uma entrega sem
  aplicação interativa.
- **Atenção à regra do evento:** áudio gerado por IA precisa de aviso no texto descritivo e nos
  metadados.
- **Perguntas para o grupo responder antes de escolher:**
  - Alguém do grupo tem noção de música ou de síntese de áudio?
  - Ferramenta interativa ou coleção curada?
  - Como testar a experiência com leitor de tela antes do prazo?
  - Quais visualizações do EIC entram, e por quê?
