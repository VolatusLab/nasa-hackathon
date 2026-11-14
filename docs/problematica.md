# Problemática do desafio 13: Space Mission Design Game

Base para as decisões do grupo sobre escopo, stack e solução. **Não propõe solução**: a ideia de
como resolver o desafio é do grupo ([ADR 0004](adr/0004-desafio-13-jogo-de-projeto-de-missao.md),
[`../CLAUDE.md`](../CLAUDE.md) §1). Onde o texto analisa uma implicação, ela aparece como
**critério ou pergunta**.

- **Status:** rascunho para o grupo validar. Pode mudar antes da decisão de escopo.
- **Fontes lidas em 14/11/2026.** Cada afirmação factual leva `[S#]`; a lista de fontes está no
  fim, com o grau de evidência de cada uma.
- **Lacunas explícitas** aparecem como `[VERIFICAR]`. Não há número sem fonte.
- **Uso de IA:** texto redigido com Claude Code, a partir das fontes listadas. Registrado em
  [`entrega.md`](entrega.md).

## 1. Problemática em uma frase

Missões espaciais só funcionam quando decisões acopladas de engenharia (instrumentos, nave,
órbita, lançador, massa, energia, orçamento, comunicações, dados e tempo de vida) são tomadas e
reavaliadas em conjunto, e quem aprende esse processo costuma ver cada parte isolada, sem
experimentar a missão inteira nem entender por que uma escolha altera o resultado [S8].

## 2. Problemática em um parágrafo

O desafio parte de uma tensão já reconhecida no próprio enunciado: uma decisão que melhora um
aspecto da missão cria limitações em outro. Um instrumento mais capaz aumenta o valor científico e
também a massa, o consumo de energia, o volume de dados e o custo [S8]. Essas ligações são difíceis
de ensinar porque o ensino costuma tratar cada tema isoladamente, como mecânica orbital, projeto
de nave ou lançamento, sem mostrar como eles interagem [S8]. A falha de uma missão real também
pode vir de uma interface mal verificada, e não de uma escolha de projeto: a perda da Mars Climate
Orbiter é atribuída pela NASA a um erro de navegação causado pela falha em converter unidades
inglesas para métricas [S5] `[VERIFICAR]` com o relatório oficial. Assim, o problema tem duas
partes: decidir sob acoplamento e verificar as ligações entre as partes. Os dois aspectos precisam
ser considerados, e o desafio pede um jogo que permita experimentar a missão inteira, com
restrições e retorno sobre o porquê de cada resultado [S8]. Quais desses aspectos entram no jogo é
decisão do grupo (Q1 e Q2).

## 3. Camada 1: o problema de engenharia

### 3.1 Decisões acopladas

O enunciado lista as decisões e as restrições que a missão precisa fechar em conjunto [S8]. A
tabela abaixo registra apenas as ligações que o próprio enunciado ou as fontes oficiais citam.

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

O aparato de maturidade e de projeto está nos recursos indicados para o desafio, e é a base
para pensar a ordem das decisões:

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

**Leitura do grupo (inferência a validar, não fato de fonte):** os casos mostram que o acoplamento
entre partes aparece tanto na decisão de projeto quanto na interface e na verificação. Um jogo que
modele só *trade-offs* de massa, energia e custo deixaria de fora uma fonte documentada de falha.

### 3.4 Não existe solução única

O enunciado diz que "there is rarely a single perfect solution" e que combinações diferentes de
nave, instrumentos, órbitas e lançadores podem atingir o mesmo objetivo [S8]. Isso é uma
propriedade do problema, não uma opinião: o critério de decisão precisa ser explicitado, senão a
avaliação não se sustenta.

## 4. Camada 2: por que é difícil aprender

### 4.1 O que o enunciado afirma

- Estudantes e aspirantes a engenheiros "rarely have access to an environment where they can
  experiment with an entire mission from concept to operation" [S8].
- "these trade-offs often remain abstract" [S8].
- Ferramentas existentes "often focus on individual topics" [S8].

Essas afirmações são do enunciado, e o grupo as trata como premissa a verificar, não como fato
independente.

### 4.2 O que a evidência educativa mostra (e o que não mostra)

- **Marsbound! (NASA/JPL Education).** O guia traz uma etapa "Evaluate change in ability to solve
  engineering problems" com questionário pré e pós [S7]. É instrumento de avaliação embutido no
  material, mas **nenhum resultado publicado** foi encontrado [S7].
- **NASA Space Voyagers (JPL).** A página lista alinhamento com padrões de ensino, mas não relata
  nenhuma avaliação de resultados de aprendizagem [S6] (leitura da página, sem citação literal).
- **Lacuna de evidência:** a busca de 14/11/2026 não encontrou estudo revisado por pares que meça
  ganho de aprendizagem em jogos de projeto de missão. Essa lacuna precisa ser declarada em
  qualquer argumento educativo do pitch e da demo.

### 4.3 Público e nível

| Recurso | Público indicado | Fonte |
|---|---|---|
| Marsbound! | 3º a 5º ano (grades 3–5) | [S7] |
| NASA Space Voyagers | 6º a 12º ano (grades 6–12) | [S6] |
| Desafio 13 | iniciante/jovem e intermediário; público declarado: estudantes e aspirantes a engenheiros | [S8] |

A diferença de público muda o nível de simplificação. Ela é uma decisão do grupo (pergunta Q6).

## 5. Camada 3: o que as ferramentas levantadas cobrem

Levantamento feito a partir das descrições oficiais, sem testar as ferramentas. O escopo é o
conjunto levantado em 14/11/2026, e não o universo de ferramentas.

| Ferramenta | Missão inteira | Decisões acopladas | Papéis e colaboração | Explica o porquê | Público indicado |
|---|---|---|---|---|---|
| NASA Space Voyagers [S6] | sim, com cartas: construir uma nave e explorar destinos | escolha entre recursos de financiamento e de pesquisa, com dano cumulativo | até quatro jogadores, em colaboração | não pede explicação escrita; aponta um vídeo de tutorial | 6º a 12º ano |
| Marsbound! [S7] | sim, com cartas: missão a Marte | orçamento, massa e potência como restrições | equipes | a descrição não cita explicação do resultado | 3º a 5º ano |
| Jogo do telescópio, da NASA Webb [S9] | não: só o telescópio | objetivos científicos determinam comprimentos de onda, instrumentos e óptica | individual | sim: "scientific objectives determine the engineering characteristics" | não indicado |
| NASA Mission Viz [S9] | não: visualização de trajetórias | não decide; mostra | não | sim, como apoio visual | não indicado |
| Mission Design Lab [S9] | sim, mas é ambiente profissional de avaliação de conceitos | análise de disciplinas (energia, propulsão, térmica etc.) | equipes de engenheiros | não é ferramenta de ensino | profissionais |

**O que a tabela não mostra:** nenhuma ferramenta levantada reúne, ao mesmo tempo, missão inteira,
decisões acopladas, colaboração de até quatro pessoas e explicação do porquê do resultado. Isso é
um achado desta busca, não uma afirmação de que nada existe. A conclusão precisa de busca ampliada
(`[VERIFICAR]`).

## 6. Quem é afetado

- **Público declarado pelo enunciado:** estudantes e aspirantes a engenheiros, em níveis
  iniciante/jovem e intermediário [S8].
- **Hipóteses a validar, sem fonte levantada:** professores que usariam o jogo em sala; estudantes
  de cursos de engenharia com pouco contato com projeto de missão. Essas hipóteses precisam de
  validação antes de entrar no pitch.

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

- **Relevância:** o critério pede que o dado da NASA seja parte central, não enfeite. O uso de
  recursos da NASA já foi decidido pelo grupo (ADR 0004); a pergunta é qual recurso muda uma
  decisão do jogo (Q3).
- **Validade:** a base científica depende de as ligações da tabela 3.1 serem fiéis às fontes
  (Handbook, [S2]).
- **Impacto:** depende do público e da escala de uso (Q6).
- **Criatividade:** a problemática não impõe forma; o grupo escolhe.
- **Apresentação:** a lacuna de evidência educativa (4.2) precisa aparecer com honestidade.

### 8.2 Regras do evento

- Entrega em inglês; apenas o vídeo pode ser falado em português, com legenda em inglês [`entrega.md`].
- Nenhum nome, voz, imagem ou outra representação reconhecível de menor de 18 anos.
- Todo recurso externo usado entra no registro de fontes de `entrega.md`, com link, licença e
  data de acesso.
- Conteúdo gerado com IA é identificado.
- Prazo: 15/11/2026, 23h59.

## 9. Tensões que a solução vai ter de resolver

Descrevem o campo de decisão. **Nenhuma escolhe um lado.**

- **Realismo × acessibilidade:** o enunciado pede restrições realistas e acesso a pessoas com
  pouco conhecimento [S8].
- **Profundidade × prazo:** o escopo do desafio é amplo, e o prazo termina em 15/11/2026, 23h59.
- **Multijogador × complexidade:** o grupo decidiu incluir multijogador desde a primeira versão
  (ADR 0004); o enunciado cita colaboração entre papéis diferentes [S8].
- **Dado real × modelo simplificado:** o enunciado aceita modelos realistas ou simplificados [S8]; o
  critério de Relevância pede dado da NASA central.
- **Explicar o porquê × mostrar o resultado:** o enunciado pede que o jogo ensine por que uma
  decisão afeta o desempenho, e não só se está certa ou errada [S8].
- **Um resultado único × vários caminhos:** o enunciado afirma que não há solução perfeita única
  [S8]; o critério de avaliação precisa dizer o que é "bom".

## 10. Perguntas de decisão para o grupo

Cada pergunta indica a pendência que ela informa (`pendencias.md`) e a seção que a sustenta.

- **Q1 (pendência 6):** qual é o núcleo mínimo de decisões acopladas que a primeira versão precisa
  representar? Base: 3.1.
- **Q2 (pendência 6):** o jogo vai modelar unidades e verificação de interfaces, ou só decisões de
  projeto? Base: 3.3 (Mars Climate Orbiter e Wright).
- **Q3 (pendência 7):** qual recurso da NASA muda uma decisão do jogo, e como? Base: 3.2 e 8.1.
- **Q4 (pendência 6):** quais papéis existem no modo multijogador (planejamento, nave, ciência,
  comunicações, recursos), e como a equipe negocia prioridades? Base: enunciado, seção
  "Collaboration" [S8].
- **Q5 (pendência 10):** como a demo mostra o porquê de um fracasso, e não só a nota final? Base: 4.2.
- **Q6 (pendência 6):** para qual público o jogo é feito primeiro: crianças e adolescentes, ou
  estudantes de engenharia? Base: 4.3.
- **Q7 (pendência 8):** a stack depende de Q1 a Q4. Base: 9.
- **Q8 (pendência 6):** o grupo quer medir aprendizagem na demo? Se sim, com qual instrumento?
  Base: 4.2 (lacuna de evidência).

## 11. Lacunas de evidência e hipóteses

- **L1:** nenhum estudo revisado por pares sobre ganho de aprendizagem em jogos de projeto de
  missão foi encontrado (4.2).
- **L2:** percentuais de margem de massa e de energia por fase não foram confirmados. Uma
  apresentação do Goddard (2014), encontrada em busca, cita números, mas não foi lida e atribui os
  valores a outra referência. O trecho lido do Handbook menciona margens de massa e de energia
  como medidas exigidas, sem percentuais `[VERIFICAR]`.
- **L3:** redação exata da causa-raiz no relatório oficial do Mars Climate Orbiter não lida (3.3).
- **L4:** o trecho do Handbook lido não traz o texto completo da seção 6.8 (3.1).
- **L5:** contexto brasileiro sem fonte verificada (7).
- **L6:** as citações do GAO foram extraídas por leitura de texto integral de cada relatório, e
  devem ser conferidas antes de publicação. Os relatórios têm mais de 20 anos, e a prática
  atual pode ter mudado.
- **H1 (hipótese a validar):** entender por que uma decisão afeta o resultado melhora a
  decisão futura. O enunciado afirma isso [S8]; nenhuma fonte levantada mede o efeito.

## 12. Fontes

Todas lidas em 14/11/2026. Grau de evidência: **primária** (documento oficial ou relatório da
agência), **secundária oficial** (página da agência que resume outro documento), **material
educativo** (sem avaliação de resultado publicada).

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

Fontes encontradas em busca e **não usadas** por não terem sido lidas: apresentação do Goddard
(2014) sobre margens; artigo de Baker e Whalen sobre estudos de trade; relatório de Orion sobre
equilíbrio entre desempenho e massa; SEBoK (*System Analysis*); e as fontes sobre o contexto
brasileiro (seção 7).
