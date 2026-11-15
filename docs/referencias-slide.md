# Referências para o slide: ASTRIX Mission Studio

Material de apoio para montar o slide de referências do pitch final ([`pitch-final.md`](pitch-final.md))
e os campos "NASA Data" e "Space Agency Partner Data and Other References" da página do projeto
([`entrega.md`](entrega.md)). Foi levantado em 15/11/2026, a partir do código do jogo em `astrix/`:

- `astrix/CREDITS.md`: créditos, imagens, bibliotecas e reuso do Void Protocol;
- `astrix/packages/core/src/catalog.ts:105-125`, constante `SOURCES`: registro de fontes que o jogo mostra no painel de fontes;
- `astrix/packages/data/sources-extra.json`: fontes extras do mesmo registro;
- `astrix/docs/RESOURCES.md`: como cada dado entra no jogo e o que não se pode concluir dele;
- `astrix/docs/research/verified-facts.md`: valores conferidos na fonte em 14/11/2026.

Os títulos das fontes ficam no original, em inglês. As datas de acesso vêm do registro do jogo: lá,
`retrieved` é uma data de referência escrita à mão, salvo nos snapshots da RadLab e do DONKI, que
guardam o horário real da coleta (`astrix/docs/RESOURCES.md`, "UI evidence path"). As seções 1 a 9 vêm
dos arquivos acima; a seção 10 é uma sugestão de texto.

## 1. Desafio

| Fonte | Publicador | Link | Uso no jogo |
|---|---|---|---|
| Space Mission Design Game (desafio 13) | NASA Space Apps Challenge 2026 | <https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/> | requisitos do desafio |

## 2. Recursos da aba oficial do desafio

O registro do jogo marca oito fontes com `listedByChallenge: true` (`catalog.ts:108-116`).

| Fonte | Publicador | Link | Uso no jogo |
|---|---|---|---|
| CubeSat 101: Basic Concepts and Processes for First-Time CubeSat Developers | NASA CSLI | <https://www.nasa.gov/wp-content/uploads/2017/03/nasa_csli_cubesat_101_508.pdf> | formato e limites de massa de CubeSat (1U = cubo de 10 cm; 3U < 4,00 kg) |
| Design and Develop Science Missions | NASA | <https://www.nasa.gov/wp-content/uploads/2025/04/250323-design-and-develop-science-mission.pdf> | fases da missão, segmentos (lançamento, espaço, solo, usuário) e disciplinas de sistema |
| Concept Maturity Levels | NASA/JPL | <https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=hdl:2014/44299> | vocabulário das etapas de projeto |
| Mission Design Lab | NASA Goddard | <https://etd.gsfc.nasa.gov/capabilities/mission-design-lab/> | papéis das disciplinas no trabalho em equipe |
| GMAT (General Mission Analysis Tool) | NASA | <https://software.nasa.gov/software/GSC-19468-1> | rodada orbital de referência, independente, para comparar com o modelo do jogo (`astrix/docs/research/gmat-validation.md`). O GMAT roda fora do jogo e não vem embutido nele |
| NASA Mission Viz | NASA | <https://nasa.github.io/mission-viz/> | referência de visualização de órbita; nenhum arquivo copiado |
| A Learning Game About Telescopes (Webb, "Build It Yourself") | NASA | <https://science.nasa.gov/mission/webb/game-build-it-yourself/> | precedente de jogo de projeto e revisão |
| Digital Games and Activities | Agência Espacial Canadense (CSA) | <https://www.asc-csa.gc.ca/eng/youth-educators/digital-games-and-activities.asp> | precedente de jogo educativo |

## 3. Dados da NASA que entram no jogo

Os três primeiros são instantâneos (snapshots) versionados no código, com URL, data de coleta e hash
SHA-256. O jogo não consulta nenhuma API da NASA nem do USGS enquanto roda (`astrix/docs/RESOURCES.md`,
"Acquisition → provenance → runtime → evidence").

| Fonte | Publicador | Link | Uso no jogo | Limite que o slide precisa respeitar |
|---|---|---|---|---|
| RadLab: ISS DosTel1 (módulo Columbus), de 10/05/2024 00:00 a 12/05/2024 00:00 UTC | NASA OSDR | <https://visualization.osdr.nasa.gov/radlab/gui/data-api/> | repetição de 48 h de dose medida na missão Storm Watch | 1.886 leituras de um único instrumento. Não é mapa de radiação de qualquer órbita |
| DONKI: CME `2024-05-20T05:36:00-CME-001` e tempestades geomagnéticas de maio de 2024 | NASA GSFC/CCMC | <https://ccmc.gsfc.nasa.gov/DONKI/view/CME/31034/-1> | contexto do evento e narrativa | o jogo não calcula dose nem falha a partir do DONKI |
| Catálogo USGS Astrogeology (exportação local `astrix/nasa.json`) | USGS | <https://astrogeology.usgs.gov/search> | contagem de produtos por missão e links de produtos no relatório da missão Red Relay | 1.000 registros de um total de 1.643; a associação de produto a missão é heurística, pelo título |
| Fichas técnicas da Terra, da Lua, de Marte e do Sol | NASA NSSDCA | <https://nssdc.gsfc.nasa.gov/planetary/factsheet/earthfact.html>, `moonfact.html`, `marsfact.html`, `sunfact.html` | constantes físicas do modelo simplificado (GM, raio, órbita, irradiância solar) | — |
| What are SmallSats and CubeSats? | NASA S3VI | <https://www.nasa.gov/smallsat-institute/what-are-smallsats-and-cubesats/> | definição da classe SmallSat (menos de 180 kg) | definição de classe, não qualificação de voo |
| NASA Watches Mars Light Up During Epic Solar Storm (10/06/2024) | NASA/JPL | <https://www.nasa.gov/solar-system/planets/mars/nasa-watches-mars-light-up-during-epic-solar-storm/> | contexto de dose na superfície de Marte (Curiosity, instrumento RAD) | medida na superfície, não em órbita |
| State of the Art of Small Spacecraft Technology: Thermal Control, Power, Guidance, Navigation and Control, Communications e Avionics (este, capítulo arquivado) | NASA | <https://www.nasa.gov/smallsat-institute/sst-soa/> (um capítulo por subsistema, em `catalog.ts:119-123`) | referência para os subsistemas da espaçonave | as especificações dos componentes do jogo são hipóteses didáticas, não cotações reais |
| NASA Inspiration4 Mission Datasets | NASA OSDR | <https://www.nasa.gov/osdr-latest-news-i4-mission-datasets/> | tópico de explicação "crew-return" (`astrix/packages/data/src/science.ts:70`): precedente de missão com quatro tripulantes e três dias em órbita baixa | contexto, não especificação da cápsula do jogo (`astrix/docs/MISSION_FLOW_REFINEMENT_SPEC.md:478`) |

## 4. Normas e documentos técnicos

| Fonte | Publicador | Link | Uso no jogo |
|---|---|---|---|
| Life Support Baseline Values and Assumptions Document (BVAD), Rev. 2 (2022), tabela 3-31 | NASA | <https://ntrs.nasa.gov/api/citations/20210024855/downloads/BVAD_2.15.22-final.pdf> | consumo diário por tripulante na Crew Pathfinder: 0,895 kg de O₂, 1,085 kg de CO₂, 3,217 kg de água e 0,800 kg de comida seca |
| NASA-STD-3001 Volume 2, Rev. F: Human Factors, Habitability, and Environmental Health | NASA | <https://www.nasa.gov/wp-content/uploads/2025/05/nasa-std-3001-vol-2.pdf> | suporte à tripulação |
| Environmental Control and Life Support: LiOH chemistry (2018) | NASA | <https://ntrs.nasa.gov/api/citations/20180002051/downloads/20180002051.pdf> | filtro de CO₂ (hidróxido de lítio) |
| CubeSat Design Specification Rev. 14.1 | Cal Poly | <https://www.nasa.gov/wp-content/uploads/2018/01/cubesatdesignspecificationrev14_12022-02-09.pdf> | especificação de CubeSat |
| CCSDS Orbit Data Messages 502.0-B-3 | CCSDS | <https://ccsds.org/Pubs/502x0b3e1.pdf> | formato do estado orbital |
| GMAT Reference: Spacecraft Orbit State | espelho da documentação do GMAT | <https://documentation.help/GMAT/SpacecraftOrbitState.html> | definição do estado orbital |
| CODATA: velocidade da luz no vácuo e aceleração padrão da gravidade | NIST | <https://physics.nist.gov/cgi-bin/cuu/Value?c>, <https://physics.nist.gov/cgi-bin/cuu/Value?gn> | constantes (atraso de sinal; equação do foguete) |
| NASA Images and Media Usage Guidelines | NASA | <https://www.nasa.gov/nasa-brand-center/images-and-media/> | regras de uso das imagens da NASA |

## 5. Imagens embutidas no jogo

Todas são composições históricas, não imagens ao vivo (`astrix/CREDITS.md`, "Surface map assets").

| Arquivo | Fonte e crédito | Link |
|---|---|---|
| `earth-blue-marble-1024.png` | NASA Goddard Space Flight Center Scientific Visualization Studio; Blue Marble Next Generation, cortesia de Reto Stöckli (NASA/GSFC) e NASA Earth Observatory | <https://svs.gsfc.nasa.gov/2915/> |
| `earth-blue-black-marble-4096.webp` | Blue Marble Next Generation (janeiro de 2004): NASA Earth Observatory e NASA Goddard, Reto Stöckli. Black Marble 2016: NASA Earth Observatory, NASA Goddard e NASA-NOAA Suomi NPP VIIRS | <https://science.nasa.gov/earth/earth-observatory/blue-marble-next-generation/base-map/>, <https://science.nasa.gov/earth/earth-observatory/earth-at-night/maps/> |
| `mars-viking-1024.jpg` | USGS Astrogeology Science Center e NASA Viking (imagens de 1976 a 1980); o USGS indica domínio público | <https://astrogeology.usgs.gov/search/map/mars_viking_global_color_mosaic_925m> |
| `starmap-2020-{4096,1024}.jpg` | NASA Goddard SVS, Deep Star Maps 2020; Gaia DR2: ESA/Gaia/DPAC | <https://svs.gsfc.nasa.gov/4851/> |

## 6. Software de terceiros

Licenças completas em `astrix/THIRD_PARTY_NOTICES.txt`. As versões abaixo são as de
`astrix/CREDITS.md`; a versão que vale é a do `bun.lock`.

| Biblioteca | Versão | Licença |
|---|---|---|
| React e React DOM | 19.3.1 | MIT |
| Zustand | 5.1.0 | MIT |
| three.js | 0.183.2 | MIT |
| @react-three/fiber | 9.8.2 | MIT |
| @react-three/drei | 10.7.9 | MIT |
| lucide-react e lucide-static | 1.73.0 | ISC |
| i18next, react-i18next e i18next-browser-languagedetector | 25.10.10, 16.6.6 e 8.3.0 | MIT |
| Fontes Rajdhani e JetBrains Mono (@fontsource) | 5.3.0 | OFL-1.1 |
| qrcode-generator (Kazuhiko Arase) | 2.0.4 | MIT |

Ferramentas de desenvolvimento, que não vão no jogo publicado: Bun, TypeScript, Vite e Tailwind CSS.

## 7. Trabalho anterior reutilizado

- **Void Protocol**, commit `218625d`: componentes selecionados, adaptados com autorização do dono
  e distribuídos sob Apache-2.0 dentro do ASTRIX. O repositório Void Protocol inteiro **não** muda
  de licença. A lista arquivo a arquivo está em `astrix/CREDITS.md`, "Void Protocol adaptation
  record".
- O guia do evento pede que todo recurso usado entre na lista de referências, inclusive trabalho
  anterior do próprio time (`astrix/docs/research/verified-facts.md`, que cita a discussão
  [nasa/spaceapps #1924](https://github.com/nasa/spaceapps/discussions/1924), de 11/11/2026).

## 8. Uso de IA

Texto de `astrix/CREDITS.md`, "AI assistance", e do README do `astrix`: houve assistência de IA na
pesquisa, no planejamento, na adaptação de código, na implementação, na tradução e na verificação.
O jogo não embute imagem, vídeo ou áudio gerado por IA: a geometria da espaçonave, os diagramas e
os sons são gerados pelo código. A divulgação na submissão é feita à parte (registro de
[`entrega.md`](entrega.md)).

## 9. Licença do projeto

ASTRIX Mission Studio: Apache-2.0 (`astrix/LICENSE`). Links para NASA, USGS e CSA são referências,
não endosso. O jogo não traz logotipo nem insígnia da NASA.

## 10. Sugestão de texto para o slide

Versão curta, em português, como pede a decisão do pitch. Ajustem à vontade.

> **Referências e fontes**
>
> **Desafio:** NASA Space Apps 2026, Space Mission Design Game.
>
> **Recursos do desafio:** CubeSat 101 (NASA CSLI) · Design and Develop Science Missions (NASA) ·
> Concept Maturity Levels (NASA/JPL) · Mission Design Lab (NASA Goddard) · GMAT (NASA) · Mission
> Viz (NASA) · Webb telescope game (NASA) · Digital Games and Activities (CSA).
>
> **Dados da NASA no jogo:** dose de radiação na ISS, 10 e 11/05/2024 (RadLab, NASA OSDR) · CME de
> 20/05/2024 (DONKI, NASA CCMC) · fichas técnicas da Terra, da Lua, de Marte e do Sol (NASA NSSDCA) ·
> catálogo USGS Astrogeology.
>
> **Normas:** BVAD Rev. 2 e NASA-STD-3001 Vol. 2 (NASA) · CubeSat Design Specification 14.1 (Cal
> Poly) · CCSDS 502.0-B-3 · CODATA (NIST).
>
> **Imagens:** Blue Marble e Black Marble (NASA Earth Observatory / Goddard SVS) · mosaico Viking
> (USGS/NASA) · Deep Star Maps 2020 (NASA SVS; ESA/Gaia/DPAC).
>
> **Software:** React, three.js, Zustand, i18next, Lucide (MIT/ISC); fontes Rajdhani e JetBrains
> Mono (OFL). Componentes do Void Protocol reutilizados com autorização.
>
> **IA:** assistência de IA no código, no texto e na tradução; nenhuma imagem gerada por IA.
>
> Valores do jogo: dados históricos e hipóteses didáticas declaradas, não telemetria ao vivo.
> Links para NASA, USGS e CSA não significam endosso.

Cuidados de redação (tabela da seção 9 de [`pitch-final.md`](pitch-final.md)): não escrevam
"dados reais da NASA em tempo real" nem "simulação realista". Escrevam "medições históricas da
NASA" para a RadLab e "valores de referência" para as fichas técnicas.

## 11. Divergências encontradas: resolver antes de publicar

1. **O registro de fontes de [`entrega.md`](entrega.md) não traz as fontes que o jogo usa.**
   Faltam RadLab, DONKI, USGS, as fichas técnicas da NSSDCA, BVAD, NASA-STD-3001, LiOH, CubeSat
   Design Specification, CCSDS, CODATA, os capítulos de SmallSat e as quatro imagens. O
   `CLAUDE.md` pede que todo dado usado entre nesse registro, com licença e data de acesso.
2. **O jogo não usa os recursos que o [ADR 0005](adr/0005-recursos-nasa-primeira-versao.md)
   escolheu.** O ADR prevê números dos kits de imprensa do NISAR e do Europa Clipper, mas nenhum
   arquivo do `astrix/` os cita (busca de 15/11/2026). O jogo usa RadLab, DONKI e as fichas
   técnicas. Decisão do grupo: atualizar o ADR, com um ADR novo que substitui o 0005, ou o jogo
   `[VERIFICAR]`.
3. **Os links divergem dentro do `astrix`.** Para o CubeSat 101, `CREDITS.md` aponta
   `www3.nasa.gov/sites/default/files/atoms/files/...` e `catalog.ts:108` aponta
   `www.nasa.gov/wp-content/uploads/2017/03/...`. Para o Mission Design Lab, `CREDITS.md` aponta
   `.../integrated-design-center/mission-design-lab/` (o mesmo link de [`entrega.md`](entrega.md))
   e `catalog.ts:111` aponta `.../capabilities/mission-design-lab/`. `[VERIFICAR]` qual link abre
   e usar um só no slide.
4. **Licenças sem confirmação.** As licenças das fontes da NASA seguem `[VERIFICAR]` no registro
   de [`entrega.md`](entrega.md). Para o Mission Viz, o ADR 0005 permite só link; o jogo também só
   cita o link, o que bate.
