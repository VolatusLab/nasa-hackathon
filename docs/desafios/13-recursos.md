# 13 — Os nove recursos da aba oficial, um por um

O que foi possível ler de cada link da aba Recursos do desafio 13, e o que não foi. Serve para o
grupo saber o que existe em cada recurso antes de decidir o que usar. Em cinco dos nove, o conteúdo
principal não foi lido: o artigo do recurso 3, os jogos dos recursos 6 e 9, a página do recurso 8
e a maior parte do guia do recurso 7. **Não recomenda uso nem
propõe solução**: a escolha é do grupo, e a da primeira versão está no
[ADR 0005](../adr/0005-recursos-nasa-primeira-versao.md).

- **Lista oficial:** aba Recursos da página do desafio, lida em 14/11/2026. Texto em
  `assets/desafio-13-recursos.txt`, impressão em `assets/Resources.pdf`, tradução em
  [`13-enunciado-completo.md`](13-enunciado-completo.md).
- **Como foi lido:** cada link foi baixado em 14/11/2026 para `data/raw/` (fora do Git). O
  `data/raw/MANIFEST.tsv` guarda a URL, o hash e a data de cada arquivo. O link 8 não pôde ser
  aberto.
- **Aviso da aba:** "NASA does not endorse any non-U.S. Government entity and is not responsible
  for information contained on non-U.S. Government websites. For non-U.S. Government websites,
  participants must comply with any data use parameters of that specific website." Vale para o
  link 9 (CSA) e para destinos fora do governo dos Estados Unidos a que os recursos levam: o
  SourceForge, onde fica o download do GMAT, e o GitHub, onde fica o Mission Viz.
- **Regra do projeto:** recurso que passar a ser usado entra no registro de fontes de
  [`../entrega.md`](../entrega.md), com link, licença e data, no mesmo pull request.
- **Uso de IA:** texto redigido com Claude Code a partir dos arquivos baixados. Registrado em
  [`../entrega.md`](../entrega.md).

## Resumo

| # | Recurso | O que é | Traz números de missão? | Termos de reuso lidos | Na primeira versão (ADR 0005) |
|---|---|---|---|---|---|
| 1 | Design and Develop Science Missions | apresentação de webinar, 25 páginas | não | não indicados no arquivo | não citado no ADR |
| 2 | GMAT | software de trajetória, código aberto | não na página do catálogo | "Open Source"; a página não nomeia a licença | fora |
| 3 | Concept Maturity Levels | artigo de conferência de 2013 | não lido (PDF não baixado) | CC0 1.0 na página do repositório | não citado no ADR |
| 4 | Mission Design Lab | serviço de estudo de conceito do Goddard | não; descreve prazos e produtos dos estudos | não indicados | fora |
| 5 | NASA Mission Viz | repositório de visualizações 3D na web | arquivos de trajetória de exemplo | sem licença na raiz; partes de terceiros com termos próprios | só link |
| 6 | A Learning Game About Telescopes | jogo educativo no site do Webb | não verificado (jogo não aberto) | não indicados | só link |
| 7 | CubeSat 101 | guia de 2017 para quem faz o primeiro CubeSat | sim: massa de 1U, prazos por fase | "For Public Release" | não citado no ADR |
| 8 | Visualize a Space Mission Using VR | desafio do Space Apps de 2023 | não lido | não lido | não citado no ADR |
| 9 | Digital Games and Activities (CSA) | página com jogos e atividades da agência canadense | não | em página separada, não lida | não citado no ADR |

"Não citado no ADR" quer dizer que o grupo ainda não decidiu sobre o recurso, e não que ele foi
recusado.

## 1. Design and Develop Science Missions

- **Link:** <https://www.nasa.gov/wp-content/uploads/2025/04/250323-design-and-develop-science-mission.pdf?emrc=a454cf>
- **Arquivo local:** `data/raw/nasa-recursos/design-and-develop-science-missions.pdf`
- **O que é:** apresentação de 25 páginas (24 slides numerados e um de encerramento), datada de
  26/03/2025, da série de webinars de engenharia
  de sistemas "Access to Space for All", da NASA, de autoria de J. Levri. A capa traz o endereço
  `nasa.gov/smallsat-institute`.
- **O que traz:**
  - a definição de missão científica da NASA e os quatro segmentos (lançamento, espacial, solo e
    usuário);
  - o processo em seis etapas: "Identify Need & Goals", "Define Concept", "Define Requirements",
    "Design", "Build & Verify", "Implement";
  - um exemplo completo, o experimento BioNutrients-2 na Estação Espacial Internacional, percorrido
    etapa por etapa e segmento por segmento;
  - a ideia de começar pelo fim ("Begin with the End in Mind"), partindo do segmento de usuário;
  - a ligação entre requisito e verificação: "When identifying requirements, also plan how you will
    verify that design satisfies requirements (prior to implementation)";
  - uma lista de referências, com o Systems Engineering Handbook e as normas NPR 7123.1 e 7120.5.
  - seis exemplos de missão no último slide de conteúdo, cada um com link: PUNCH, PILOT, Dawn, um
    estudo de coleta de amostras das luas de Marte, o foguete SLS e o programa Artemis (este com
    link para a Wikipédia).
- **O que não traz:** números de massa, potência, custo ou dados de nave. Os valores que aparecem
  são os requisitos do experimento do exemplo, entre eles: 12 amostras em réplica, 30 mL por
  amostra, 3 µg de betacaroteno por mL, recipiente de amostra com menos de 250 g e volume total
  ocupado abaixo de 300 mL.
- **Termos:** documento da NASA; termos de reuso não indicados no arquivo `[VERIFICAR]`.

## 2. General Mission Analysis Tool (GMAT)

- **Link:** <https://software.nasa.gov/software/GSC-19468-1>
- **Arquivo local:** `data/raw/nasa-recursos/gmat-catalogo-software.html` (só a página do catálogo;
  o programa não foi baixado nem executado)
- **O que é:** página do catálogo de software da NASA para o GMAT, versão R2025a, referência
  GSC-19468-1.
- **O que traz:**
  - a descrição: "enterprise, multi-mission, open source software system for space mission design,
    optimization, and navigation", de órbita baixa a missões lunares, de ponto de libração e de
    espaço profundo;
  - os usos declarados: "real-world mission support, engineering studies, as a tool for education,
    and public engagement";
  - categoria "Design and Integration Tools", tipo de liberação "Open Source", sistemas Windows,
    Linux e Mac OS;
  - o botão de download, que aponta para <https://sourceforge.net/projects/gmat/>.
- **O que não traz:** o nome da licença, a documentação e qualquer número de missão. O que o
  programa calcula está descrito na aba Recursos, não nesta página.
- **Termos:** "Open Source", sem nome de licença na página `[VERIFICAR]` no SourceForge.
- **Situação:** fora da primeira versão, pelo custo de integração (ADR 0005).

## 3. Concept Maturity Levels (CMLs)

- **Link:** <https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=hdl:2014/44299>
- **Arquivo local:** `data/raw/nasa-recursos/cml-dataverse-pagina.html` (só a página do
  repositório; o PDF do artigo, `13-3547_A1b.pdf`, de 1,4 MB, **não foi baixado**)
- **O que é:** registro, no repositório aberto do JPL, do artigo "Space mission concept development
  using concept maturity levels", de Wessen, Borden, Ziemer e Kwok, apresentado na AIAA SPACE 2013
  (San Diego, 10 a 12/09/2013).
- **O que traz (resumo do artigo, na página):** o CML é "a classification system for characterizing
  the various levels of a concept's maturity", usado antes de o conceito entrar nas fases de
  formulação (A e B). As definições foram expandidas em uma matriz que indica a amplitude e a
  profundidade de análise necessárias para cada nível.
  O resumo cita as dimensões da matriz ("science objectives, mission design, technical risk,
  project organization, cost, export compliance") e explica por que o artigo para no nível 4: "The
  scope was limited due to the fact that CMLs 5 and 6 are already well defined".
- **O que não foi lido:** a definição de cada nível e a matriz. A descrição dos níveis 1 a 4 que
  aparece nos documentos do grupo, e a frase de que neles se tomam as maiores decisões de projeto,
  vêm da aba Recursos, não do artigo.
- **Termos:** a página indica "License/Data Use Agreement: CC0 1.0". O aviso de direitos dentro do
  PDF não foi conferido `[VERIFICAR]`.

## 4. Mission Design Lab (MDL)

- **Link:** <https://etd.gsfc.nasa.gov/capabilities/integrated-design-center/mission-design-lab/>
- **Arquivo local:** `data/raw/nasa-recursos/mission-design-lab.html`
- **O que é:** página do Goddard sobre um **serviço**: um ambiente em que engenheiros e parceiros
  de ciência fazem estudos de conceito de missão para clientes. Não é ferramenta que se baixe nem
  conjunto de dados.
- **O que traz:**
  - quatro tipos de estudo, com prazo e produtos:

    | Estudo | Prazo | Produtos citados |
    |---|---|---|
    | Office Hours | cerca de 1 h | sessão de ideias; identificar os "tall poles" e os estudos de compensação principais |
    | Concept Development | alguns meios períodos | viabilidade do conceito, avaliação de risco |
    | Tailored Trade Study | variável | conceito, ConOps, resumo de recursos, árvore de alternativas, custo aproximado |
    | Point Design Study | 6 dias | CAD, lista mestra de equipamentos (MEL), modelos de engenharia, custo |

  - as capacidades: projeto de órbita (baixa, geoestacionária, libração, lunar, espaço profundo),
    nave única ou constelação, sistema de solo, acomodação no lançador e fim de missão;
  - o que cada disciplina entrega em um estudo: requisitos, projeto de base, alternativas e estudos
    de compensação, interfaces, "detailed estimates of mass, power, and data rate", risco e custo;
  - dezesseis disciplinas: controle de atitude, custo, propulsão, aviônica, projeto mecânico,
    confiabilidade, dinâmica de voo, software de voo, sistemas mecânicos, detritos orbitais,
    ambiente de radiação, estruturas, comunicações, operações, energia e térmica.
  - a ligação com o recurso 3: os estudos são dimensionados pelo nível de maturidade do conceito
    (CML 1 a 4), e o estudo de projeto pontual tem como critério de entrada passar em uma lista de
    verificação de CML.
- **O que não traz:** resultado de nenhum estudo, nem números de missão.
- **Aviso na página:** "Due to the lapse in federal government funding, NASA is not updating this
  website." O rodapé diz que a página foi atualizada em 23/07/2026.
- **Termos:** não indicados `[VERIFICAR]`.
- **Situação:** fora da primeira versão (ADR 0005).

## 5. NASA Mission Viz

- **Link:** <https://nasa.github.io/mission-viz/>
- **Arquivo local:** `data/raw/nasa-recursos/mission-viz-repo.zip` (cópia do repositório
  `github.com/nasa/mission-viz`; os arquivos têm data de 16/05/2022)
- **O que é:** repositório com exemplos e tutoriais de visualização de missão na web. O `README`
  lista quatro aplicações (um planetário em ThreeJS, um em R, um com asteroides potencialmente
  perigosos e uma visualização de missão Terra–Lua) e cinco tutoriais.
- **O que traz:**
  - `OntologyDrivenOrrery/`: planetário em ThreeJS movido por ontologias de órbita (`.owl`,
    `.jsonld`) e um propagador de órbita em JavaScript;
  - `RMarkdown/`: as versões em R, um tutorial de projeto de órbita elíptica e dois arquivos de
    elementos orbitais (`SolarSystem_OrbitalElements.xlsx` e `PlanetaryOrbits.json`);
  - `X3Dom/`: arquivos de trajetória de exemplo (`MolniyaOrbit.json`, `LunarOrbit.js`,
    `LunarTransferTrajectory.js`, `missionfile.js`), um modelo de satélite (`TrianaSatellite.x3d`)
    e três tutoriais em PDF sobre como exibir na web uma trajetória gerada no GMAT.
- **Termos:** não há arquivo de licença na raiz. Partes do repositório são de terceiros e têm
  termos próprios:
  - `X3Dom/LICENSE`: biblioteca X3DOM, licença dupla MIT e GPL;
  - three.js e jQuery: MIT; CanvasMatrix: termos da Apple;
  - `OntologyDrivenOrrery/SSAO_Rovetto.owl`: "© 2011-2020, Robert John Rovetto. Not authorized for
    commercial use unless explicitly negotiated with the copyright holder, creator or author.
    Attribution is required." A restrição vale para essa ontologia.
- **Situação:** só por link, sem copiar código, até a licença ser confirmada com a NASA (ADR 0005,
  pendência 7).

## 6. A Learning Game About Telescopes

- **Link:** <https://science.nasa.gov/mission/webb/game-build-it-yourself/>
- **Arquivo local:** `data/raw/nasa-recursos/webb-build-it-yourself.html` (só a página; **o jogo
  não foi aberto**, e o texto extraído traz "Unable to render the provided source" no lugar dele)
- **O que é:** página do jogo "Build It Yourself: Satellite!", na área do telescópio Webb do site
  de ciência da NASA.
- **O que a página diz:**
  - "This game teaches the player that science requirements drive telescope mission design and
    engineering";
  - o jogador escolhe a ciência, depois comprimentos de onda, instrumentos e óptica; o número de
    opções é limitado, e algumas ficam indisponíveis por não serem viáveis;
  - há três níveis, e dá para mudar as escolhas até o lançamento;
  - depois do lançamento, o jogo mostra o satélite e a missão real com dados parecidos;
  - o jogo foi aprovado na revisão de produtos de educação da NASA em 2013;
  - tela mínima de 1024 por 768, "generally not mobile phone compatible"; não tem acessibilidade
    embutida, mas tem transcrição completa.
- **O que não foi lido:** a transcrição do jogo, a lista de opções de satélite, os resultados
  científicos dos três níveis e a seção de informação para educadores, que a página oferece em
  seções recolhidas. A última pode dizer para que público o jogo foi feito.
- **O que não traz:** números de massa, potência ou custo, pelo que a página descreve.
- **Termos:** não indicados na página `[VERIFICAR]`.
- **Situação:** só por link, como referência de design (ADR 0005).

## 7. CubeSat 101

- **Link:** <https://www3.nasa.gov/sites/default/files/atoms/files/nasa_csli_cubesat_101_508.pdf>
- **Arquivo local:** `data/raw/nasa-recursos/cubesat-101.pdf`
- **O que é:** guia "CubeSat 101: Basic Concepts and Processes for First-Time CubeSat Developers",
  da CubeSat Launch Initiative (CSLI) da NASA, revisão de outubro de 2017, produzido sob contrato
  pela California Polytechnic State University.
- **O que traz:**
  - o processo de desenvolvimento em 16 etapas, cada uma com duração típica no título, do conceito
    ("Concept Development (1-6 months)") ao lançamento (1 dia) e à operação ("variable, up to
    20 years");
  - modelos de missão conforme o tipo de lançamento, inclusive a liberação pela Estação Espacial;
  - de onde vêm os requisitos de lançamento, o licenciamento de rádio e de sensoriamento remoto, e
    a documentação de certificação de voo (massa, bateria, ensaios de vibração e de vácuo térmico);
  - números de referência: "A 1U CubeSat is a 10 cm cube with a mass of approximately 1 to
    1.33 kg"; um CubeSat "can be designed, built, tested, and delivered in as little as 9 months,
    but typically takes 18 to 24 months".
- **Limite da leitura:** o sumário e os trechos acima foram lidos; o guia inteiro, não.
- **Termos:** a capa diz "For Public Release". Não é licença nomeada `[VERIFICAR]`.

## 8. Visualize a Space Mission Using Virtual Reality

- **Link:** <https://www.spaceappschallenge.org/2023/challenges/visualize-a-space-mission-using-virtual-reality/>
- **Arquivo local:** nenhum. O site do Space Apps falha por erro de certificado na máquina de
  quem baixou, e a página **não foi lida** `[VERIFICAR]`.
- **O que se sabe, pela descrição da aba Recursos:** foi um desafio do Space Apps de 2023, sobre
  visualizar em realidade virtual uma missão inteira: conceito, trajetórias orbitais, cronograma e
  visualização tridimensional. Pela descrição da aba, é outro desafio, e não um conjunto de dados;
  como a página não foi lida, isso é leitura de quem redigiu.

## 9. Digital Games and Activities (CSA)

- **Link:** <https://www.asc-csa.gc.ca/eng/youth-educators/digital-games-and-activities.asp>
- **Arquivo local:** `data/raw/nasa-recursos/csa-jogos-atividades.html` (só a página de índice;
  nenhum dos jogos foi aberto)
- **O que é:** índice de jogos, livros digitais e atividades da Agência Espacial Canadense, com
  data de modificação de 26/11/2025.
- **O que a página lista:** onze itens. Quatro são jogos: "Game – OSIRIS-REx" (escolher o melhor
  local do asteroide Bennu para coletar uma amostra), "Game – RADARSAT Constellation Mission" (usar
  imagens de radar para ajudar um agricultor, um capitão e um socorrista), "Game – Mission:
  Astronaut" (minijogos sobre treinamento e vida no espaço) e "Tomatosphere Adventure" (jogo em
  Minecraft Education sobre fotossíntese e cultivo de tomates em Marte). Os demais são atividades,
  livros digitais, modelos para impressão 3D, quebra-cabeça, quizzes e listas de música.
- **O que não traz:** números de missão.
- **Termos:** o rodapé aponta "Notices and copyright" e "Terms and conditions", em páginas
  separadas que não foram lidas `[VERIFICAR]`. É site de governo que não é o dos Estados Unidos:
  vale o aviso da aba sobre cumprir os parâmetros de uso do próprio site.

## Fora da aba: os kits de imprensa do ADR 0005

Os números de NISAR e de Europa Clipper que o grupo aprovou como referência **não estão na aba
Recursos**. Vêm das páginas de fatos rápidos dos kits de imprensa do JPL, que é laboratório da
NASA. Se isso basta para o critério "Relevância" e para a condição de prêmio global, o guia não
foi conferido nesse ponto `[VERIFICAR]`. Os valores lidos e os limites de cada página estão no
registro de fontes de [`../entrega.md`](../entrega.md).

## Outros arquivos baixados e não usados

O `data/raw/MANIFEST.tsv` lista três arquivos que não vêm da aba e que nenhum documento do grupo
usa. Foram baixados em 14/11/2026, durante a análise dos recursos.

| Arquivo | O que é | O que traz |
|---|---|---|
| `documentos-apoio/maven-fact-sheet-rev11.pdf` | ficha da missão MAVEN, da NASA (2013) | comprimento de 11,4 m; massa seca máxima de 903 kg; massa máxima com combustível no lançamento de 2.550 kg; potência de 1.135 W "when Mars is furthest from the Sun" |
| `documentos-apoio/lsp-vehicles-performance.html` | página inicial do site de desempenho de lançadores do Launch Services Program | só a apresentação do site; nenhum número de capacidade |
| `documentos-apoio/lsp-req-317-01a.pdf` | documento de requisitos LSP-REQ-317.01, Revisão B, do Launch Services Program | não foi lido além da capa |

Os termos de reuso desses três arquivos não foram conferidos `[VERIFICAR]`.
