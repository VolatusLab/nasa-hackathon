# Problemática do desafio 13: Space Mission Design Game

Base para as decisões do grupo sobre escopo, stack e solução. **Não propõe solução**: a ideia de
como resolver o desafio é do grupo ([ADR 0004](adr/0004-desafio-13-jogo-de-projeto-de-missao.md),
[`../CLAUDE.md`](../CLAUDE.md) §1). Onde o texto analisa uma implicação, ela aparece como
**critério ou pergunta**.

- **Status:** rascunho para o grupo validar. Reescrito em 14/11/2026 com foco em prática e avaliação.
- **Fontes lidas em 14/11/2026.** Cada afirmação factual leva `[S#]`; a lista de fontes está no
  fim, com o grau de evidência de cada uma.
- **Lacunas explícitas** aparecem como `[VERIFICAR]`. Não há número sem fonte.
- **Uso de IA:** texto redigido com Claude Code, a partir das fontes listadas. Registrado em
  [`entrega.md`](entrega.md).

## 1. Problemática em uma frase

Estudantes de ensino médio e de graduação em engenharia praticam pouco a decisão integrada de uma
missão espacial, e quase nunca com medida de aprendizado: as experiências disponíveis são
fragmentadas por idade, escopo ou formato, e nenhuma das lidas publica evidência de que ensine as
decisões acopladas que promete ensinar [S6, S7, S8, S10, S11].

## 2. Problemática em um parágrafo

O enunciado reconhece duas faltas. A primeira é de **prática**: estudantes e aspirantes a
engenheiros raramente têm um ambiente para experimentar uma missão inteira, do conceito à operação,
e as ferramentas existentes costumam tratar temas isolados [S8]. Nas ferramentas lidas, a prática
existe, mas com recorte: jogos de cartas para crianças e adolescentes, um workshop presencial para
graduação, ou software profissional [quadro na seção 5]. A segunda é de **avaliação**: o enunciado
pede que o jogo ensine "por que uma decisão específica afeta o desempenho" [S8], e nenhuma das
ferramentas lidas publica resultado de aprendizado. O Marsbound tem um instrumento de pré e pós-teste
sem resultados publicados [S7]; o KSP tem um estudo preliminar, em curso de engenharia, de amostra
pequena e sem grupo de controle [S10]; os demais não reportam avaliação [S6, S11]. Assim, o professor
não sabe se a prática ensina o que promete, e quem desenvolve não tem como provar um efeito. A falta
de ferramenta, tese inicial do grupo, não foi confirmada: ferramentas existem. Ela continua como
hipótese a testar (H2, pergunta Q7).

## 3. O que a prática precisa cobrir: o conteúdo de engenharia

### 3.1 Decisões acopladas

O enunciado lista as decisões e as restrições que a missão precisa fechar em conjunto [S8]. A
tabela registra apenas as ligações citadas pelo enunciado ou pelas fontes oficiais.

| Decisão | O que ela afeta, segundo a fonte | Fonte |
|---|---|---|
| Instrumento mais capaz | sobe o valor científico; sobe massa, consumo de energia, volume de dados e custo | [S8] (Background) |
| Órbita escolhida | cobertura, oportunidades de observação, comunicações e tempo de vida | [S8] (Orbit and launch) |
| Veículo lançador | capacidade de carga, custo e alcance orbital; deve ser compatível com a massa e a órbita | [S8] (Orbit and launch) |
| Componentes da nave | estrutura, energia, baterias, comunicações, computador de bordo e controle de atitude | [S8] (Spacecraft and payload) |
| Margem de projeto | reserva em orçamento, cronograma e parâmetros técnicos, consumida ao longo do ciclo de vida | [S2] (glossário, "Margin") |
| Dimensionamento de subsistemas | tamanhos de sistemas e subsistemas são muitas vezes determinados durante os estudos de compensação (*trade studies*) | [S2] (estudos de trade) `[VERIFICAR]` página |

O Handbook da NASA define o processo de análise de decisão como um apoio a órgãos decisórios para
avaliar "technical, cost, and schedule issues, alternatives, and their uncertainties" [S2]
(seção 6.8). O trecho lido não traz o texto completo da seção; ela precisa ser conferida antes de
ser citada em material de entrega.

### 3.2 Maturidade e etapas

Os recursos indicados para o desafio mostram como a maturidade e as etapas de projeto organizam as
decisões:

- **CML (Concept Maturity Levels), do JPL:** o artigo se concentra "mainly on CML 1–4, where the
  greatest design decisions are made" [S9].
- **MDL (Mission Design Lab):** os níveis de estudo são *Office Hours*, *Concept Development*,
  *Trade Studies* e *Point Design*, do levantamento rápido ao projeto detalhado com modelos CAD e
  estimativas de custo [S9].
- **Segmentos de uma missão:** lançamento, espacial, solo e usuário [S9].

### 3.3 Falhas reais: acoplamento e verificação

- **Mars Climate Orbiter (1999).** A página oficial da NASA descreve a causa como erro de
  navegação, causado pela falha em converter unidades inglesas para métricas, com software de
  solo em unidades inglesas e software de bordo em métricas [S5]. A redação exata do relatório da
  comissão de investigação não foi lida: `[VERIFICAR]` antes de citar a causa-raiz em material de
  entrega.
- **Mars Polar Lander (1999).** A investigação da NASA concluiu que "the premature shutdown of the
  Lander's descent engines was the most probable cause for the loss of the spacecraft" [S3].
- **Lições que não chegam ao projeto seguinte.** O GAO registrou preocupação de que as lições
  "were not being applied to current programs and projects" [S3]. Gestores relataram "the lack of
  time available for lessons learned" e "reluctance to share negative lessons" [S4].
- **Integração e teste.** Wright (NASA Goddard, 2018) escreve que "It has been said that I&T is the
  last defense against any flight system problems prior to launch" [S1]. Ele também afirma que
  "History is replete with mishaps that could have been avoided, had the participants been aware of
  and heeded previous lessons learned" [S1]. O próprio autor diz que as recomendações "are not
  considered formal requirements" [S1]: é argumento técnico, não norma.

**Leitura do grupo (inferência a validar, não fato de fonte):** o acoplamento aparece na decisão de
projeto e também na interface e na verificação. Uma prática que treine só *trade-offs* de massa,
energia e custo deixaria de fora uma fonte documentada de falha.

### 3.4 Não existe solução única

O enunciado diz que "there is rarely a single perfect solution" e que combinações diferentes de
nave, instrumentos, órbitas e lançadores podem atingir o mesmo objetivo [S8]. Isso importa para a
avaliação: sem um critério de decisão explícito, não há como dizer se uma escolha foi boa.

## 4. Prática e avaliação: o que existe e o que falta

### 4.1 O que o enunciado afirma

- Estudantes e aspirantes a engenheiros "rarely have access to an environment where they can
  experiment with an entire mission from concept to operation" [S8].
- "these trade-offs often remain abstract" [S8].
- Ferramentas existentes "often focus on individual topics" [S8].
- O jogo deve ensinar o porquê: "Consider teaching participants why a particular decision affects
  mission performance, rather than simply indicating whether the decision is correct or incorrect"
  [S8].

Essas afirmações são do enunciado. O grupo as trata como premissas a verificar, não como fatos
independentes.

### 4.2 Avaliação de aprendizagem nas ferramentas lidas

| Ferramenta | O que existe de avaliação | Resultado publicado | Fonte |
|---|---|---|---|
| NASA Space Voyagers | nenhuma: a página não relata avaliação | não | [S6] |
| Marsbound! | etapa *Evaluate* e questionários pré e pós | não encontrado | [S7] |
| Kerbal Space Program (curso de engenharia) | estudo com pré e pós-teste, de caráter preliminar | sim, preliminar; amostra pequena, sem grupo de controle `[VERIFICAR]` com o artigo | [S10] |
| ESA Academy, Concurrent Engineering | nenhuma avaliação de aprendizagem reportada | não | [S11] |

- **Lacuna de evidência:** nas buscas de 14/11/2026, não se encontrou estudo revisado por pares que
  meça ganho de aprendizagem em jogos ou práticas de projeto de missão.
- **Evidência geral sobre jogos sérios e aprendizagem:** um resumo de busca indica efeito positivo
  de jogos sérios sobre aprendizagem (Wouters et al., 2013), e outro indica benefício de falhar antes
  de aprender a regra (*productive failure*, Sinha e Kapur, 2021). Nenhum dos dois foi lido
  na íntegra, e os números não foram confirmados `[VERIFICAR]`. Eles não são jogos de projeto de
  missão, então só sustentam a hipótese de que o formato pode ajudar.

### 4.3 Público e nível

| Recurso | Público indicado | Fonte |
|---|---|---|
| Marsbound! | 3º a 5º ano (grades 3–5) | [S7] |
| NASA Space Voyagers | 6º a 12º ano (grades 6–12) | [S6] |
| Workshops da ESA Academy | graduação (20 estudantes em 2018; 116 em 2025) | [S11] |
| Desafio 13 | iniciante/jovem e intermediário; público declarado: estudantes e aspirantes a engenheiros | [S8] |

A diferença de público muda o tipo de prática e de avaliação. Ela é uma decisão do grupo (pergunta Q4).

## 5. Ferramentas: meio de entrega, não a lacuna comprovada

Levantamento a partir de descrições oficiais e de leituras de páginas e materiais, sem testar as
ferramentas. O conjunto é o levantado em 14/11/2026, e não o universo de ferramentas.

| Ferramenta | Formato | Missão | Decisões acopladas | Explica o porquê | Avaliação publicada | Público indicado |
|---|---|---|---|---|---|---|
| NASA Space Voyagers [S6] | cartas, em grupo ou sozinho | construir uma nave e explorar destinos | recursos de financiamento e de pesquisa; dano "permanent and cumulative" | não pede explicação escrita; aponta vídeo de tutorial | não | 6º a 12º ano |
| Marsbound! [S7] | cartas, em equipes | projeto de missão a Marte (operações não confirmadas) | orçamento, massa e potência como restrições | sim, etapa *Explain*: alunos explicam e questionam soluções | instrumento sem resultados | 3º a 5º ano |
| Kerbal Space Program [S10] | jogo comercial, com estudos em sala | foguetes e órbitas; sem orçamento nem operações | parcial | não avaliado no material lido | preliminar | público geral; estudo em curso de engenharia |
| ESA Academy, Concurrent Engineering [S11] | oficina presencial | projeto de missão em subsistemas (energia, térmica, propulsão, custo) | sim | não reportado | não | graduação |
| Jogo do telescópio, NASA Webb [S9] | jogo educativo | só o telescópio | objetivos científicos determinam comprimentos de onda, instrumentos e óptica | sim: "scientific objectives determine the engineering characteristics" | não indicado | não indicado |
| NASA Mission Viz [S9] | visualização 3D | não decide; mostra trajetórias | não | apoio visual | não | não indicado |
| Mission Design Lab [S9] | ambiente profissional | estudos de conceito de missão | análise de disciplinas | não é ferramenta de ensino | não | engenheiros |

**Leitura:** nenhuma das ferramentas lidas reúne missão inteira, decisões acopladas, colaboração,
explicação do porquê e avaliação publicada, para o mesmo público. A Marsbound reúne três das quatro
dimensões de projeto para o público de 3º a 5º ano. Esse é um achado da busca, não prova de que a
combinação não exista. A afirmação precisa de busca sistemática, com protocolo declarado, antes de
ser feita `[VERIFICAR]`.

## 6. Quem é afetado

- **Público declarado pelo enunciado:** estudantes e aspirantes a engenheiros, em níveis
  iniciante/jovem e intermediário [S8].
- **Hipóteses a validar, sem fonte levantada:** professores que escolhem a prática em sala e
  precisam de evidência para justificar o uso; estudantes de engenharia com pouco contato com projeto
  de missão. Essas hipóteses precisam de validação antes de entrar no pitch.

## 7. Contexto brasileiro e local

**Lacuna:** nenhuma fonte brasileira foi lida e verificada nesta rodada, então nenhum dado de
contexto local entra como fato. `[VERIFICAR]`.

Fontes candidatas para uma próxima leitura, todas ainda não lidas:
- Escola Virtual da Agência Espacial Brasileira (cursos gratuitos de engenharia espacial);
- Relatório de gestão da AEB de 2024;
- Catálogo da indústria espacial brasileira (AEB).

## 8. Lentes do evento

### 8.1 Critérios de julgamento

Os cinco critérios são Impacto, Criatividade, Validade, Relevância e Apresentação [S8, e
`entrega.md`]. A problemática os toca assim:

- **Validade:** a base científica depende de as ligações da tabela 3.1 serem fiéis às fontes
  (Handbook, [S2]), e de a prática ter alguma forma de avaliação (4.2).
- **Relevância:** o critério pede que o dado da NASA seja parte central, não enfeite. O uso de
  recursos da NASA já foi decidido pelo grupo (ADR 0004); a pergunta é qual recurso muda uma
  decisão da prática (Q5).
- **Impacto:** depende do público e da escala de uso (Q4).
- **Criatividade:** a problemática não impõe forma; o grupo escolhe.
- **Apresentação:** o pitch não pode afirmar aprendizado sem medida. Se a demo não medir, precisa
  dizer isso (Q6).

### 8.2 Regras do evento

- Entrega em inglês; apenas o vídeo pode ser falado em português, com legenda em inglês [`entrega.md`].
- Nenhum nome, voz, imagem ou outra representação reconhecível de menor de 18 anos.
- Todo recurso externo usado entra no registro de fontes de `entrega.md`, com link, licença e
  data de acesso.
- Conteúdo gerado com IA é identificado.
- Prazo: 15/11/2026, 23h59.

## 9. Tensões que a solução vai ter de resolver

Descrevem o campo de decisão. **Nenhuma escolhe um lado.**

- **Prática aberta × avaliação comparável:** quanto mais livre a prática, mais difícil medir o mesmo
  resultado em todos os alunos.
- **Realismo × acessibilidade:** o enunciado pede restrições realistas e acesso a pessoas com
  pouco conhecimento [S8].
- **Profundidade × prazo:** o escopo é amplo, e o prazo termina em 15/11/2026, 23h59.
- **Multijogador × avaliação individual:** o grupo decidiu adiar o multijogador para depois da primeira
  versão (ADR 0006); o enunciado cita colaboração entre papéis diferentes [S8]. Medir o aprendizado
  de cada um em equipe é um problema próprio.
- **Dado real × modelo simplificado:** o enunciado aceita modelos realistas ou simplificados [S8]; o
  critério de Relevância pede dado da NASA central.
- **Explicar o porquê × pontuar:** o enunciado pede que o jogo ensine por que uma decisão afeta o
  desempenho [S8]; uma pontuação sozinha não faz isso.

## 10. Perguntas de decisão para o grupo

Cada pergunta indica a pendência que ela informa (`pendencias.md`) e a seção que a sustenta.

- **Q1 (pendência 6):** que decisões acopladas a prática precisa exercitar na primeira versão? Base: 3.1.
- **Q2 (pendência 6):** como o grupo sabe se a prática ensinou algo? Que itens de pré e pós-teste
  usaria, e quem os aplicaria? Base: 4.2.
- **Q3 (pendência 6):** como o retorno explica o porquê de um resultado, e não só o resultado?
  Base: 4.1 (citação do enunciado).
- **Q4 (pendência 6):** qual público vem primeiro: 3º a 5º ano, 6º a 12º ano ou graduação? Base: 4.3.
- **Q5 (pendência 7):** qual recurso da NASA entra como parte central de uma decisão, e como? Base:
  3.2 e 8.1.
- **Q6 (pendência 10):** como a demo mostra a prática e a evidência, sem afirmar aprendizado que não
  foi medido? Base: 8.1.
- **Q7 (pendência 6):** o público-alvo já tem acesso a algum simulador (por exemplo GMAT ou KSP)? Se
  sim, por que não usa? A resposta testa a hipótese H2. Base: 5.
- **Q8 (pendência 8):** a stack depende de Q1 a Q3 e de Q7. Base: 9.

## 11. Lacunas de evidência e hipóteses

- **L1:** nenhum estudo revisado por pares sobre ganho de aprendizagem em jogos ou práticas de
  projeto de missão foi encontrado nas buscas (4.2).
- **L2:** percentuais de margem de massa e de energia por fase não foram confirmados. Uma
  apresentação do Goddard (2014), encontrada em busca, cita números, mas não foi lida. O trecho lido
  do Handbook menciona margens de massa e de energia como medidas exigidas, sem percentuais
  `[VERIFICAR]`.
- **L3:** redação exata da causa-raiz no relatório oficial do Mars Climate Orbiter não lida (3.3).
- **L4:** o trecho do Handbook lido não traz o texto completo da seção 6.8 (3.1).
- **L5:** contexto brasileiro sem fonte verificada (7).
- **L6:** as citações do GAO foram extraídas por leitura de texto integral de cada relatório, e
  devem ser conferidas antes de publicação. Os relatórios têm mais de 20 anos, e a prática
  atual pode ter mudado.
- **L7:** itens só vistos em resumo de busca, sem leitura integral: Wouters et al. (2013); Sinha e
  Kapur (2021); UCL Systemisers; Purdue AeroQuest; KerbalEDU. O link da ESA de 2018 não foi
  registrado `[VERIFICAR]`.
- **L8:** o estudo do KSP (S10) foi lido por extração de texto de um PDF, e a amostra de 58
  participantes citada na leitura de auditoria precisa ser confirmada `[VERIFICAR]`.
- **H1 (hipótese a validar):** prática com retorno explicativo melhora a decisão posterior em
  missões com decisões acopladas. O enunciado afirma o objetivo [S8]; nenhuma fonte levantada mede
  esse efeito.
- **H2 (hipótese a testar, Q7):** a falta de acesso a ferramentas é o gargalo. Hoje a evidência
  não a confirma, porque as ferramentas existem.

## 12. Fontes

Todas consultadas em 14/11/2026. Grau de evidência: **primária** (documento oficial ou relatório da
agência), **secundária oficial** (página da agência que resume outro documento), **material
educativo** (sem avaliação de resultado publicada), **estudo** (pesquisa com avaliação).

| # | Fonte | Tipo e grau | Link | Licença e termos |
|---|---|---|---|---|
| S1 | Wright, M. R. (2018). *Flight Systems Integration & Test: Lessons Learned for Future Success*. NASA Goddard. NTRS 20180003229 | primária, relatório técnico NASA; não revisado por pares | https://ntrs.nasa.gov/api/citations/20180003229/downloads/20180003229.pdf | documento do governo dos EUA; termos específicos `[VERIFICAR]` |
| S2 | NASA. *NASA Systems Engineering Handbook*, NASA/SP-2016-6105 Rev2 | primária, normativa | https://www.nasa.gov/sites/default/files/atoms/files/nasa_systems_engineering_handbook_0.pdf | documento do governo dos EUA; termos específicos `[VERIFICAR]` |
| S3 | GAO. *NASA: Better Mechanisms Needed for Sharing Lessons Learned*, GAO-02-195 (2002) | primária, relatório de auditoria | https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-02-195/html/GAOREPORTS-GAO-02-195.htm | domínio público (GAO) `[VERIFICAR]` |
| S4 | GAO. *Survey of NASA's Lessons Learned Process*, GAO-01-1015R (2001) | primária, relatório de auditoria | https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-01-1015R/html/GAOREPORTS-GAO-01-1015R.htm | domínio público (GAO) `[VERIFICAR]` |
| S5 | NASA Science. *Mars Climate Orbiter* | secundária oficial (resumo; o relatório da comissão não foi lido) | https://science.nasa.gov/mission/mars-climate-orbiter/ | página oficial da NASA `[VERIFICAR]` |
| S6 | NASA JPL Education. *NASA Space Voyagers: The Game* | material educativo; sem avaliação de resultado | https://www.jpl.nasa.gov/edu/learn/project/nasa-space-voyagers-the-game/ | não indicada na página `[VERIFICAR]` |
| S7 | NASA JPL Education. *Marsbound! Mission to the Red Planet*, guia completo | material educativo; avaliação pré e pós sem resultados publicados | https://d2pn8kiwq2w21t.cloudfront.net/documents/marsbound-fullguide.pdf (redirecionamento de `jpl.nasa.gov/edu/pdfs/marsbound-fullguide.pdf`) | não indicada `[VERIFICAR]` |
| S8 | NASA Space Apps Challenge 2026. *Space Mission Design Game* (enunciado) | oficial, regra do desafio | https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/ (impressão em `assets/NASA Space Apps Challenge.pdf`) | uso de conteúdo do evento conforme os termos do evento `[VERIFICAR]` |
| S9 | NASA Space Apps Challenge 2026. *Aba Recursos* do desafio 13 | oficial, lista de recursos | https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/?tab=resources (impressão em `assets/Resources.pdf`) | igual a S8 `[VERIFICAR]` |
| S10 | Ranalli, J. (2013). Estudo sobre o uso do Kerbal Space Program em curso de engenharia de primeiro ano (*Frontiers in Education*) | estudo; preliminar, com pré e pós-teste | https://jranalli.github.io/preprints/Ranalli2013FIE.pdf (texto extraído por leitura de auditoria; conferir o link, pois outra leitura não conseguiu abrir o mesmo PDF) | não indicada `[VERIFICAR]` |
| S11 | ESA Academy. *Concurrent Engineering Challenge* (edições de 2018 e 2025) | material educativo; oficina presencial, sem avaliação reportada | https://esa.int/Education/ESA_Academy/116_students_tackle_real-world_space_mission_design_at_ESA_Academy_s_Concurrent_Engineering_Challenge_2025 (link da busca; página de 2025 lida em auditoria; 2018 sem link registrado) `[VERIFICAR]` |

Fontes encontradas em busca e **não usadas** por não terem sido lidas: apresentação do Goddard
(2014) sobre margens; artigo de Baker e Whalen sobre estudos de trade; relatório de Orion sobre
equilíbrio entre desempenho e massa; SEBoK (*System Analysis*); Wouters et al. (2013); Sinha e
Kapur (2021); UCL Systemisers; Purdue AeroQuest; KerbalEDU; e as fontes sobre o contexto brasileiro
(seção 7).
