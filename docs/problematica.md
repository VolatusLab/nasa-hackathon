# Problemática do desafio 13: Space Mission Design Game

Base para as decisões do grupo sobre escopo, stack e solução. **Não propõe solução**: a ideia de
como resolver o desafio é do grupo ([`entrega.md`](entrega.md), seção "Uso de IA";
[`../CLAUDE.md`](../CLAUDE.md) §1). Onde o texto analisa uma implicação, ela aparece como
**critério ou pergunta**.

- **Status:** texto consolidado em 14/11/2026, depois de revisão geral e de três rodadas de revisão
  por pares contra as fontes. Está pronto para subsidiar o escopo e o pitch (seção 12). A validação
  pelo grupo e as respostas às perguntas Q1 a Q8 seguem na pendência 17 de
  [`pendencias.md`](pendencias.md).
- **Fontes lidas em 14/11/2026.** Cada afirmação factual leva `[S#]`; a lista de fontes está no
  fim, com o grau de evidência de cada uma. Na revisão do mesmo dia, as citações e os números de S1 a
  S12 foram conferidos contra os arquivos baixados em `data/raw/` (fora do Git) e contra o texto
  oficial em `assets/`.
- **Lacunas explícitas** aparecem como `[VERIFICAR]`. Não há número sem fonte.
- **Uso de IA:** texto redigido com Claude Code, a partir das fontes listadas. Registrado em
  [`entrega.md`](entrega.md). Por isso, onde o texto interpreta as fontes, o rótulo é "leitura de
  quem redigiu": só vira leitura do grupo depois que o grupo validar.

## 1. Problemática em uma frase

Estudantes e aspirantes a engenheiros aprendem conceitos espaciais isolados e raramente têm onde
praticar a decisão integrada de uma missão inteira, do conceito à operação: é o que o enunciado
declara [S8].

Essa é a parte do problema que vem do enunciado, e é o núcleo. Duas leituras de quem redigiu a
acompanham, sem fazer parte da frase: as descrições das ferramentas lidas são coerentes com essa
premissa (seção 5), e nelas não foi encontrada medida publicada de aprendizado (4.2). A segunda
leitura não muda o que o desafio pede; ela limita o que o pitch pode afirmar (12.2).

O público é o que o enunciado descreve. O recorte dentro dele (faixa escolar ou universitários) não
está decidido: é a pergunta Q4. A frase que resume o que o desafio pede está em
[`desafio.md`](desafio.md).

## 2. Problemática em um parágrafo

O enunciado reconhece uma falta, a de **prática**: estudantes e aspirantes a engenheiros raramente
têm um ambiente para fazer experimentos com uma missão inteira, do conceito à operação, e as
ferramentas existentes costumam tratar temas isolados [S8]. Nas ferramentas lidas, a prática
existe, mas com recorte: dois jogos de cartas para faixas escolares diferentes, um jogo comercial
de foguetes usado em um curso de engenharia, uma oficina para universitários e um serviço
profissional [quadros na seção 5].

A segunda falta, de **avaliação**, é **leitura de quem redigiu** a partir das ferramentas lidas, e não
afirmação do enunciado. O enunciado sugere ensinar por que uma decisão afeta o desempenho da
missão [S8], o que trata do retorno ao jogador, não de medir aprendizado. Em nenhuma das
ferramentas lidas foi encontrado resultado publicado de aprendizado. O Marsbound tem fichas de
ideias antes e depois da atividade e rubricas, sem resultados no guia [S7]. O estudo com o KSP
mediu autoeficácia e atitude por questionário, não aprendizado; teve 58 alunos e resultado misto,
e os próprios autores o chamam de preliminar [S10]. A página do Space Voyagers e a notícia da ESA
não relatam avaliação [S6, S11].

**Leitura de quem redigiu (inferência a validar pelo grupo):** sem medida publicada, quem escolhe
a prática não tem como saber se ela ensina o que se propõe, e quem a desenvolve não tem como
demonstrar efeito.

A tese inicial do grupo, informada em 14/11/2026, era: "O principal problema identificado é a falta
de ferramentas práticas e interativas para ensinar o planejamento e o gerenciamento de missões
espaciais completas".

**Leitura de quem redigiu (a validar pelo grupo):** a tese pode ser lida de dois jeitos, e as
fontes respondem de modo diferente a cada um.

- Lida como "faltam ferramentas práticas e interativas", ela não se sustenta: há dois jogos de
  cartas ligados ao JPL, um jogo comercial usado em sala, uma oficina da ESA e um jogo no site do
  telescópio Webb (seção 5).
- Lida com o peso em "missões espaciais **completas**", ela repete a premissa do enunciado:
  "Existing tools often focus on individual topics [...] without demonstrating how these elements
  interact as a complete system" [S8]. O quadro 5.2 é coerente com essa premissa por um critério
  declarado: nas descrições lidas, nenhuma das experiências educativas reúne os seis recursos que o
  enunciado lista (massa, energia, orçamento, dados, comunicações e tempo).

O que o pitch pode dizer sobre isso, e com que palavras, está em uma única linha da tabela 12.2.
A primeira leitura continua como hipótese a testar (H2, pergunta Q7).

## 3. O conteúdo de engenharia que o enunciado e as fontes descrevem

### 3.1 Decisões acopladas

O enunciado lista decisões e restrições que interagem em uma missão [S8]. A tabela registra apenas
as ligações citadas pelo enunciado ou pelas fontes oficiais. As linhas com [S8] vêm, em parte, da
lista de considerações opcionais do enunciado.

| Decisão | O que ela afeta, segundo a fonte | Fonte |
|---|---|---|
| Instrumento mais capaz | pode subir o valor científico e, ao mesmo tempo, a massa, o consumo de energia, o volume de dados e o custo ("may increase") | [S8] (Background) |
| Órbita escolhida | cobertura, oportunidades de observação, comunicações e tempo de vida | [S8] (Orbit and launch) |
| Veículo lançador | capacidade de carga útil, custo e alcance orbital; o enunciado sugere verificar se a massa da nave e a órbita escolhida são compatíveis com o lançador | [S8] (Orbit and launch) |
| Componentes da nave | o enunciado lista como componentes possíveis: estrutura, sistemas de energia, baterias, comunicações, computadores de bordo, controle de atitude e instrumentos científicos. Não diz o que cada um afeta | [S8] (Spacecraft and payload) |
| Margem de projeto | reserva em orçamento, cronograma e parâmetros técnicos, consumida ao longo do ciclo de vida | [S2] (glossário, "Margin") |
| Dimensionamento de subsistemas | "System and subsystem sizes are often determined during the trade studies" | [S2] (seção 4.4, p. 70) |

O Handbook da NASA descreve o processo de análise de decisão como apoio a órgãos decisórios para
avaliar "technical, cost, and schedule issues, alternatives, and their uncertainties" [S2]
(seção 6.8, p. 164). A frase foi conferida no PDF; o restante da seção não foi lido.

### 3.2 Maturidade e etapas

Os recursos indicados para o desafio mostram como a maturidade e as etapas de projeto organizam as
decisões:

- **CML (Concept Maturity Levels), do JPL:** a aba Recursos diz que o artigo se concentra "mainly
  on CML 1–4, where the greatest design decisions are made" [S9]. A frase é da aba; o artigo não
  foi lido.
- **MDL (Mission Design Lab):** os níveis de estudo são *Office Hours*, *Concept Development*,
  *Trade Studies* e *Point Design*, do levantamento rápido ao projeto detalhado com modelos CAD e
  estimativas de custo [S9].
- **Segmentos de uma missão:** lançamento, espacial, solo e usuário [S9].
- **Processo de projeto:** o primeiro recurso da aba descreve seis etapas: "Identify Need & Goals",
  "Define Concept", "Define Requirements", "Design", "Build & Verify" e "Implement". Ele liga
  requisito a verificação: "When identifying requirements, also plan how you will verify that
  design satisfies requirements (prior to implementation)" [S12].

O que cada um dos nove recursos da aba traz de fato, inclusive o que não foi lido, está em
[`desafios/13-recursos.md`](desafios/13-recursos.md).

### 3.3 Falhas reais: acoplamento e verificação

- **Mars Climate Orbiter (1999).** A página oficial da NASA descreve a causa como erro de
  navegação, causado pela falha em converter unidades inglesas para métricas, com software de
  solo em unidades inglesas e software de bordo em métricas [S5]. O GAO resume assim a conclusão da
  equipe de investigação da NASA: "the loss was due to the mistaken use of English rather than
  metric units in the navigation software" [S3]. O relatório da própria comissão não foi lido:
  `[VERIFICAR]` antes de citar a redação literal da causa-raiz em material de entrega.
- **Mars Polar Lander (1999).** A investigação da NASA concluiu que "the premature shutdown of the
  Lander's descent engines was the most probable cause for the loss of the spacecraft" [S3].
- **Lições que não chegam ao projeto seguinte.** Segundo o GAO, as investigações da NASA sobre
  essas falhas levantaram a preocupação de que as lições "were not being applied to current
  programs and projects" [S3]. Gestores relataram "the lack of
  time available for lessons learned" e "reluctance to share negative lessons" [S4].
- **Integração e teste.** Wright (NASA Goddard, 2018) escreve que "It has been said that I&T is the
  last defense against any flight system problems prior to launch" [S1]. Ele também afirma que
  "History is replete with mishaps that could have been avoided, had the participants been aware of
  and heeded previous lessons learned" [S1]. O próprio autor diz que as recomendações "are not
  considered formal requirements" [S1]: é argumento técnico, não norma.

**Leitura de quem redigiu (inferência a validar pelo grupo, não fato de fonte):** nas falhas
acima, o acoplamento aparece na interface e na verificação, e não só na decisão de projeto. Se
isso entra ou não na primeira versão é escolha do grupo (Q1).

### 3.4 Não existe solução única

O enunciado sugere mostrar que "there is rarely a single perfect solution" e que combinações
diferentes de nave, instrumentos, órbitas e lançadores podem atingir o mesmo objetivo [S8].

**Leitura de quem redigiu (inferência a validar pelo grupo):** se há mais de uma solução boa,
dizer que uma escolha foi boa depende de um critério declarado. Qual critério, e se ele existe na
primeira versão, é escolha do grupo.

## 4. Prática e avaliação: o que existe e o que falta

### 4.1 O que o enunciado afirma

- Estudantes e aspirantes a engenheiros "rarely have access to an environment where they can
  experiment with an entire mission from concept to operation" [S8].
- "these trade-offs often remain abstract" [S8].
- Ferramentas existentes "often focus on individual topics" [S8].
- O enunciado sugere ensinar o porquê: "Consider teaching participants why a particular decision
  affects mission performance, rather than simply indicating whether the decision is correct or
  incorrect" [S8]. O item está na lista de considerações, que o enunciado abre com "You may (but
  are not required to) consider".

Essas afirmações são do enunciado. O grupo as trata como premissas a verificar, não como fatos
independentes.

### 4.2 Avaliação de aprendizagem nas ferramentas lidas

| Ferramenta | O que existe de avaliação | Resultado publicado | Fonte |
|---|---|---|---|
| NASA Space Voyagers | nenhuma na página lida; ela aponta um plano de aula, que não foi lido `[VERIFICAR]` | não encontrado | [S6] |
| Marsbound! | etapa *Evaluate* ("Evaluate change in ability to solve engineering problems"), com fichas de ideias antes e depois da atividade (*Pre-Ideas* e *Post-Ideas*) e três rubricas | não encontrado no guia | [S7] |
| Kerbal Space Program (curso de engenharia de primeiro ano) | questionário antes e depois da atividade, sobre autoeficácia e atitude. O artigo cita nota por rubrica sobre os objetivos de aprendizagem, mas não publica as notas | sim, preliminar e misto: 58 alunos, comparados com 909 de turmas anteriores que não usaram o jogo; três subescalas com mudança significativa, duas em alta e uma em queda. Os autores apontam amostra pequena, professor diferente, médias iniciais mais baixas e uma turma com mais alunos de segundo ano | [S10] |
| ESA Academy, Concurrent Engineering | nenhuma avaliação de aprendizagem na notícia lida | não encontrado | [S11] |

- **Lacuna de evidência:** nas buscas de 14/11/2026, não se encontrou estudo revisado por pares que
  meça ganho de aprendizagem em jogos ou práticas de projeto de missão.
- **Evidência geral sobre jogos e aprendizagem:** não lida. Dois trabalhos apareceram só em resumo
  de busca (L7) e, por isso, não sustentam nenhuma afirmação deste documento `[VERIFICAR]`.

### 4.3 Público e nível

| Recurso | Público indicado | Fonte |
|---|---|---|
| Marsbound! | *grades* 3 a 5 | [S7] |
| NASA Space Voyagers | *grades* 6 a 12 | [S6] |
| ESA Academy, Concurrent Engineering Challenge 2025 | universitários (116 estudantes) | [S11] |
| Desafio 13 | o enunciado descreve quem carece da prática: estudantes e aspirantes a engenheiros. "Iniciante/jovem" e "intermediário" são a dificuldade do desafio no evento, não o público do jogo | [S8] |

*Grades* são os anos escolares dos Estados Unidos. A equivalência com as séries brasileiras é
aproximada e não foi conferida em fonte `[VERIFICAR]`.

Qual público vem primeiro é decisão do grupo (pergunta Q4).

## 5. Ferramentas: meio de entrega, não a lacuna comprovada

### 5.1 O que cada descrição diz

Levantamento a partir de descrições oficiais e de leituras de páginas e materiais, sem testar as
ferramentas. O conjunto é o levantado em 14/11/2026, e não o universo de ferramentas. "Não
indicado" quer dizer que a fonte lida não trata do assunto, e não que a ferramenta não tenha a
característica.

| Ferramenta | Formato | Missão | Decisões acopladas | Explica o porquê | Avaliação publicada | Público indicado |
|---|---|---|---|---|---|---|
| NASA Space Voyagers [S6] | cartas, sozinho ou com até três outros jogadores, em colaboração | comprar naves e instrumentos e explorar um destino | recursos de financiamento e de pesquisa; dano "permanent and cumulative" | não pede explicação escrita; aponta vídeo de tutorial | não encontrada na página; plano de aula não lido | *grades* 6 a 12 |
| Marsbound! [S7] | cartas, em equipes | projeto de missão a Marte até o dia do lançamento, decidido em dado; sem fase de operação | orçamento, massa e potência como restrições | sim, etapa *Explain*: alunos explicam e questionam soluções | fichas antes e depois e rubricas, sem resultados no guia | *grades* 3 a 5 |
| Kerbal Space Program [S10] | jogo comercial, usado em projeto de equipe em sala | no estudo: projetar um foguete que vá à lua do planeta de origem e volte | no estudo: tipo de motor, quantidade de combustível e arranjo de estágios, com efeito em empuxo/peso, controle e estabilidade (descrito, não medido) | o estudo relata que os alunos tiveram dificuldade de ligar o jogo ao processo de projeto sem intervenção do professor | preliminar, sobre autoeficácia | no estudo: curso de engenharia de primeiro ano |
| ESA Academy, Concurrent Engineering [S11] | oficina em três universidades e em centro da ESA | conceito de missão por equipes de subsistema (propulsão, energia, térmica, controle de atitude e órbita, carga útil), com modelo CAD preliminar e estimativa de custo | sim: a notícia fala em "mission objectives, design constraints, and system-level trade-offs" | não indicado | não encontrada na notícia | universitários |
| Jogo do telescópio (*A Learning Game About Telescopes*) [S9] | jogo educativo | só o telescópio | objetivos científicos determinam comprimentos de onda, instrumentos e óptica | intenção declarada: "demonstrate how scientific objectives determine the engineering characteristics"; não testado | não indicado | não indicado |
| NASA Mission Viz [S9] | visualização 3D | mostra conceitos e trajetórias de missão | não indicado | apoio visual (leitura de quem redigiu) | não indicado | não indicado |
| Mission Design Lab [S9] | ambiente colaborativo profissional | estudos de conceito de missão, com comparação de arquiteturas (*Trade Studies*) | analisa disciplinas da nave, custo e risco | não indicado | não indicado | engenheiros e cientistas |

### 5.2 Recursos do enunciado em cada descrição

O enunciado lista seis recursos importantes: massa, energia, orçamento, dados, comunicações e
tempo [S8]. O quadro diz se a fonte lida menciona cada um como algo que o participante administra.
"Não" quer dizer que a fonte lida não menciona, e não que a ferramenta não tenha.

| Ferramenta | Massa | Energia | Orçamento | Dados | Comunicações | Tempo | Trecho da missão descrito |
|---|---|---|---|---|---|---|---|
| NASA Space Voyagers [S6] | não | não | sim (cartas de financiamento) | não | não | não | compra de naves e instrumentos, exploração do destino e dano a cada rodada, até explorar o destino ou acabarem as cartas |
| Marsbound! [S7] | sim | sim | sim | não | sim, como sistema (cartas de comunicações) | em parte: o texto de apoio cita por quanto tempo cada sistema de energia funciona | do objetivo ao dia do lançamento |
| Kerbal Space Program, no estudo [S10] | em parte: quantidade de combustível e razão empuxo/peso | não | não | não | não | não | projeto do foguete, lançamento, voo até a lua e retorno |
| ESA Academy, Concurrent Engineering [S11] | não | sim (equipe de energia) | sim (estimativa de custo) | não | não | não | "from preliminary concept to feasibility study" |
| Jogo do telescópio [S9] | não | não | não | não | não | não | escolha de ciência, comprimentos de onda, instrumentos e óptica; lançamento animado e resultados |
| NASA Mission Viz [S9] | não | não | não | não | não | não | visualização de trajetórias |
| Mission Design Lab [S9] | não | sim | sim (custo) | não | sim | não | "the complete mission", da órbita ao planejamento do fim de missão; é serviço profissional |

A página do Mission Design Lab, fora da aba, fala ainda em estimativas de massa, potência e taxa
de dados ([`desafios/13-recursos.md`](desafios/13-recursos.md)).

**Leitura de quem redigiu (inferência a validar pelo grupo):**

- Nas descrições lidas, nenhuma das cinco experiências educativas (Space Voyagers, Marsbound, o
  projeto com o KSP, a oficina da ESA e o jogo do telescópio) reúne os seis recursos. A descrição
  do KSP é a de um estudo de 2013, feito com a versão de demonstração do jogo. A que
  menciona mais deles é o Marsbound (massa, energia, orçamento e o sistema de comunicações), para
  *grades* 3 a 5 e até o lançamento.
- O Mission Design Lab é descrito como tratando a missão completa, mas é serviço para
  profissionais.
- Em nenhuma foi encontrado resultado publicado de aprendizado (4.2).
- Colaboração não é coluna dos quadros, mas aparece em cinco descrições: Space Voyagers (que
  também pode ser jogado sozinho), Marsbound, o projeto com o KSP, a oficina da ESA e o Mission
  Design Lab, que a aba chama de ambiente colaborativo.

Esse é um achado sobre sete descrições, não prova de que a combinação não exista em outro lugar:
a busca não foi sistemática `[VERIFICAR]`. A única redação que o pitch pode usar está na
tabela 12.2.

O critério dos seis recursos foi escolhido por quem redigiu, a partir de uma lista opcional do
enunciado ("Important resources could include"). Ele serve para comparar descrições. **Não é meta
de escopo:** quantos e quais recursos entram na primeira versão é escolha do grupo (Q1), e a
alegação de lacuna só cabe no pitch se combinar com o que o grupo entregar.

## 6. Quem é afetado

- **Público descrito pelo enunciado:** estudantes e aspirantes a engenheiros [S8]. A dificuldade
  do desafio no evento (iniciante/jovem e intermediário) classifica o desafio para as equipes, não
  o público do jogo.
- **Outros públicos:** nenhum outro público tem fonte levantada. Se o grupo quiser citar alguém
  além de quem o enunciado descreve (por exemplo, professores), precisa ouvir essas pessoas ou
  achar fonte antes de levar a afirmação ao pitch (12.2).

## 7. Contexto brasileiro e local

**Lacuna:** nenhuma fonte brasileira foi lida e verificada nesta rodada, então nenhum dado de
contexto local entra como fato. `[VERIFICAR]`.

Fontes candidatas para uma próxima leitura, todas ainda não lidas:

- Escola Virtual da Agência Espacial Brasileira (cursos gratuitos de engenharia espacial);
- Relatório de gestão da AEB de 2024;
- Catálogo da indústria espacial brasileira (AEB).

## 8. Lentes do evento

### 8.1 Critérios de julgamento

Os cinco critérios são Impacto, Criatividade, Validade, Relevância e Apresentação (guia de
julgamento, resumido em [`entrega.md`](entrega.md)). A problemática os toca assim:

- **Validade:** o critério olha base científica, viabilidade técnica, o quanto está desenvolvido
  e a facilidade de uso. A base científica depende de as ligações da tabela 3.1 serem fiéis às
  fontes ([S2], [S8]).
- **Relevância:** o critério pede que o dado da NASA seja parte central, não enfeite. Os recursos
  da primeira versão já foram escolhidos pelo grupo
  ([ADR 0005](adr/0005-recursos-nasa-primeira-versao.md)); a pergunta que resta é como eles mudam
  uma decisão da prática (Q5).
- **Impacto:** depende do público e da escala de uso (Q4).
- **Criatividade:** a problemática não impõe forma; o grupo escolhe.
- **Apresentação:** o pitch não pode afirmar aprendizado sem medida. Se a demo não medir, precisa
  dizer isso (Q6).

### 8.2 Regras do evento

- Entrega em inglês; apenas o vídeo pode ser falado em português, com legenda em inglês
  ([`entrega.md`](entrega.md)).
- Nenhum nome, voz, imagem ou outra representação reconhecível de menor de 18 anos.
- Todo recurso externo usado entra no registro de fontes de `entrega.md`, com link, licença e
  data de acesso.
- Conteúdo gerado com IA é identificado.
- Prazo: 15/11/2026, 23h59, no horário do evento local.

## 9. Tensões que a solução vai ter de resolver

Descrevem o campo de decisão. **Nenhuma escolhe um lado.**

- **Prática aberta × avaliação comparável:** quanto mais livre a prática, mais difícil medir o mesmo
  resultado em todos os alunos.
- **Realismo × acessibilidade:** o enunciado sugere restrições realistas e um jogo acessível a
  participantes com níveis diferentes de conhecimento [S8].
- **Profundidade × prazo:** o escopo é amplo, e o prazo termina em 15/11/2026, 23h59.
- **Multijogador × avaliação individual:** o grupo decidiu adiar o multijogador para depois da primeira
  versão (ADR 0006); o enunciado cita colaboração entre papéis diferentes [S8]. Medir o aprendizado
  de cada um em equipe é um problema próprio.
- **Dado real × modelo simplificado:** o enunciado aceita modelos realistas ou simplificados [S8]; o
  critério de Relevância pede dado da NASA central.
- **Explicar o porquê × pontuar:** o enunciado sugere ensinar por que uma decisão afeta o
  desempenho, e também sugere um sistema de pontuação [S8]. São duas sugestões distintas do
  enunciado.

## 10. Perguntas de decisão para o grupo

Cada pergunta indica a pendência que ela informa (`pendencias.md`) e a seção que a sustenta.

- **Q1 (pendência 6):** que decisões acopladas a prática precisa exercitar na primeira versão, e que
  trecho da missão ela cobre? Base: 3.1 e 12.1.
- **Q2 (pendência 6):** o grupo vai medir se a prática ensinou algo? Se sim, como e com quem?
  "Não na primeira versão" é resposta possível. Base: 4.2.
- **Q3 (pendência 6):** o jogo vai explicar o porquê de um resultado, e não só o resultado? Se sim,
  como? Base: 4.1 (citação do enunciado).
- **Q4 (pendência 6):** qual público vem primeiro, dentro do público descrito pelo enunciado? As ferramentas
  lidas atendem *grades* 3 a 5, *grades* 6 a 12 e universitários. Base: 4.3.
- **Q5 (pendências 6 e 7):** como os recursos escolhidos no ADR 0005 entram como parte central de
  uma decisão do jogo, e não como enfeite? Base: 8.1, ADR 0005 e registro de fontes de `entrega.md`.
- **Q6 (pendência 10):** como a demo mostra a prática e a evidência, sem afirmar aprendizado que não
  foi medido? Base: 8.1.
- **Q7 (pendência 6):** o público-alvo já tem acesso a algum simulador (por exemplo GMAT ou KSP)? Se
  sim, por que não usa? A resposta testa a hipótese H2, e pode ficar para depois da primeira
  versão. Base: 5.
- **Q8 (pendência 8):** que stack atende às respostas das perguntas de escopo (Q1 a Q5 e Q7)?
  Base: 9.

## 11. Lacunas de evidência e hipóteses

- **L1:** nenhum estudo revisado por pares sobre ganho de aprendizagem em jogos ou práticas de
  projeto de missão foi encontrado nas buscas (4.2).
- **L2:** percentuais de margem de massa e de energia por fase não foram confirmados
  `[VERIFICAR]`. Uma apresentação do Goddard (2014), encontrada em busca, cita números, mas não foi
  lida. O Handbook lista margens de massa e margens de potência entre as medidas técnicas mínimas a
  acompanhar (apêndice J, item 7.4, p. 231), sem percentuais [S2].
- **L3:** redação exata da causa-raiz no relatório oficial do Mars Climate Orbiter não lida (3.3).
- **L4:** da seção 6.8 do Handbook só a frase citada foi conferida; o restante da seção não foi
  lido (3.1).
- **L5:** contexto brasileiro sem fonte verificada (7).
- **L6:** as citações do GAO foram conferidas no texto integral baixado em 14/11/2026. Os
  relatórios têm mais de 20 anos, e a prática atual pode ter mudado.
- **L7:** itens só vistos em resumo de busca, sem leitura integral: Wouters et al. (2013); Sinha e
  Kapur (2021); UCL Systemisers; Purdue AeroQuest; KerbalEDU; e a edição de 2018 da oficina da ESA,
  que por isso saiu do quadro de público (4.3).
- **L8:** o estudo do KSP (S10) mede autoeficácia e atitude, não aprendizado das decisões de
  projeto. Ele não serve de evidência de que o jogo ensine decisões acopladas.
- **H1 (hipótese a validar):** prática com retorno explicativo melhora a decisão posterior em
  missões com decisões acopladas. O enunciado sugere esse caminho [S8]; nenhuma fonte levantada mede
  esse efeito.
- **H2 (hipótese a testar, Q7):** o principal problema é "a falta de ferramentas práticas e
  interativas", como diz a tese do grupo, lida sem o peso em "completas". A evidência lida em
  14/11/2026 não a confirma, porque ferramentas existem; a leitura com o peso em "completas" está
  na seção 2.

## 12. Para o MVP e o pitch

Esta seção organiza o que as anteriores estabelecem, para o grupo fechar o escopo e o pitch.
**Não escolhe solução, público nem mecânica.**

### 12.1 O que o enunciado pede e o que só sugere

O enunciado tem um pedido, dito de duas formas, e muitas sugestões. A força de cada trecho vem do
verbo usado [S8].

| Força | O que diz | Onde |
|---|---|---|
| **Pedido** | "create an interactive game that allows participants to design, manage, and simulate a complete space mission while making engineering decisions, managing limited resources, and evaluating how each choice shapes the success of their mission" | Descrição |
| **Pedido** | "create an interactive Space Mission Design Game that allows participants to experience the process of designing and managing a complete space mission" | Objectives |
| Incentivo (`encouraged`) | "develop creative alternatives that make the experience engaging while preserving the fundamental trade-offs of real-world space mission design" | Background |
| Incentivo (`encouraged`) | "develop creative game mechanics, visualizations, scoring systems, and mission scenarios that make the experience engaging while requiring players to solve problems, make trade-offs, and collaborate to achieve mission success" | Objectives |
| Afirmações do enunciado, sem verbo de pedido | "Players benefit from seeing how their decisions affect other parts of the mission"; "Clear objectives and feedback help participants understand why a mission succeeds or fails"; "Scientific and engineering concepts work best when explained in simple terms"; um jogo ajuda ao permitir "learn from both successful and unsuccessful missions" | Objectives, Considerações e Background |
| Solução forte (`might include`) | jogo ou simulação funcional com interface de usuário clara, sistema de configuração da missão, mecanismos de gestão de recursos, colaboração ou multijogador para até quatro pessoas, e sistema de simulação e avaliação da missão | Objectives |
| Recomendação (`should`, única ocorrência, dentro da lista opcional) | "The game should clearly display the main resources available to the mission team" | Considerações, Resource Management |
| Sugestão (`could`, `may`, `consider`) | os itens das sete listas de considerações e a lista final de funcionalidades: papéis em equipe, níveis de dificuldade, eventos aleatórios, verificação de compatibilidade com o lançador, explicação do porquê, análise pós-missão e os demais | Objectives e Considerações |

A lista de considerações abre com "You may (but are not required to) consider the following".

As duas formas do pedido não são idênticas. A da Descrição tem três verbos para o que o
participante faz com a missão (`design`, `manage`, `simulate`) e três coisas que ele faz enquanto
isso: tomar decisões de engenharia, gerenciar recursos limitados e avaliar como cada escolha afeta
o sucesso. A de Objectives fala em viver o processo de projetar e gerenciar, sem `simulate`. As
duas dizem "a complete space mission".

**Leitura de quem redigiu (a validar pelo grupo):**

- Os termos do pedido são: jogo interativo; missão espacial completa; projetar, gerenciar e
  simular; decisões de engenharia; recursos limitados; e avaliar o efeito de cada escolha no
  sucesso da missão.
- O enunciado não define o que conta como missão "completa". O Background fala em "from concept to
  operation". Onde a primeira versão começa e termina é escolha do grupo (Q1).
- Fora desses termos, o restante do enunciado é margem de escolha. Há condições que não vêm do
  enunciado: usar ao menos um dado ou recurso da NASA para concorrer a prêmio global, e os
  requisitos de submissão ([`entrega.md`](entrega.md)).

### 12.2 O que os materiais de entrega podem afirmar

Vale para o one-liner, os slides, o vídeo e a página do projeto. Os limites de cada formato estão
em [`entrega.md`](entrega.md). As frases em inglês repetem os verbos do original; trocar "can" ou
"may" por afirmação direta muda o que a fonte diz.

**Sobre o problema**

| Afirmação | Situação | Base |
|---|---|---|
| "A decision that improves one aspect of a mission can create limitations in another." Um instrumento mais capaz pode subir o valor científico e, junto, massa, consumo, dados e custo | pode afirmar, com "pode" e citando o enunciado | [S8], 3.1 |
| "Students and aspiring engineers rarely have access to an environment where they can experiment with an entire mission from concept to operation"; as ferramentas existentes costumam tratar temas isolados | pode afirmar **como premissa do desafio** ("o desafio aponta que...") | [S8], 4.1 |
| "Das sete ferramentas cujas descrições lemos, sem testá-las, nenhuma das educativas reúne os seis recursos que o desafio lista: massa, energia, orçamento, dados, comunicações e tempo." Em inglês: "Of the seven tools whose descriptions we read, without testing them, none of the educational ones combines the six resources the challenge lists: mass, power, budget, data, communications and time." | pode afirmar **só com essa redação e essas ressalvas**, depois de o grupo validar a leitura (pendência 17) e só se combinar com o que for entregue. É a única forma permitida da alegação de lacuna. As cinco educativas e a ressalva sobre o KSP estão em 5.2 | 5.2 |
| "Não existe ferramenta que faça isso", "é o primeiro jogo que..." | **não pode**: a busca não foi sistemática | 5.2, H2 |
| A Mars Climate Orbiter foi perdida por uso de unidades inglesas onde deveriam ser métricas | pode afirmar | [S5], [S3], 3.3 |
| Investigações da NASA levantaram a preocupação de que lições não eram aplicadas aos projetos seguintes | pode afirmar, com o ano dos relatórios do GAO (2001 e 2002) | [S3], [S4], 3.3 |
| "Professores precisam de..." ou qualquer necessidade de quem não foi ouvido | **não pode**: é hipótese sem fonte | seção 6 |
| Jogos melhoram o aprendizado em geral; o estudo com o KSP mostra que jogo ensina | **não pode**: fontes não lidas, e o estudo mede autoeficácia | L7, L8 |
| Percentuais de margem de massa ou de potência | **não pode**: sem fonte lida | L2 |
| Qualquer dado sobre o Brasil ou sobre Ceres-GO | **não pode**: sem fonte lida | L5, seção 7 |

**Sobre o que o grupo entregar**

| Afirmação | Situação | Base |
|---|---|---|
| "O jogo ensina" ou "melhora o aprendizado" | **não pode**: nada foi medido | 4.2, H1 |
| "Testado com estudantes", "validado" | **não pode**, a menos que o grupo teste e registre como testou | Q2 |
| "Aprovado", "apoiado" ou "endossado pela NASA" | **não pode**: a aba diz "NASA does not endorse any non-U.S. Government entity", e o guia veda usar ou alterar marcas da NASA | [S9]; `entrega.md`, "Uso de IA" |
| "Usa dados reais da NASA" | só depois que algum número entrar no produto e no registro de fontes. Os valores disponíveis são de projeto, anteriores ao lançamento, e não medidos: dizer "valores de projeto publicados pela NASA" | `entrega.md`, ADR 0005 |
| Citar os números de NISAR e de Europa Clipper | pode citar com a página e a data. Do Europa Clipper não há potência nem taxa de dados. Se os números podem entrar no produto antes de a NASA responder sobre os termos de reuso é decisão do grupo, em aberto (pendência 7) | `entrega.md`, ADR 0005 |
| "Simulação realista" ou "fiel" | **não pode** sem dizer qual modelo foi usado e de onde vem; nenhum modelo de simulação foi lido | 12.4 |
| "Missão completa, do conceito à operação", dito do próprio jogo | só se o que for entregue cobrir isso; depende de Q1 | 12.1 |
| "Colaborativo" ou "multijogador" | **não pode** na primeira versão: descrever só o que for entregue | ADR 0006 |
| "Segue os níveis de maturidade (CML) do JPL" | **não pode**: o artigo não foi lido | `desafios/13-recursos.md` |
| "Integra o GMAT" ou "integra o Mission Viz" | **não pode**: o GMAT está fora e o Mission Viz entra só por link | ADR 0005 |

O checklist do one-liner está em [`pitch.md`](pitch.md).

### 12.3 Como as perguntas dependem umas das outras

**Leitura de quem redigiu (a validar pelo grupo)**, a partir do texto das perguntas (seção 10) e
das dependências de [`pendencias.md`](pendencias.md). Não ordena prioridades do grupo.

- **Escopo da primeira versão (pendência 6):** Q1, Q3, Q4 e Q5 pedem resposta para o escopo fechar.
  Q2 e Q7 também são perguntas de escopo, mas admitem "depois da primeira versão" como resposta;
  nesse caso, os materiais de entrega ficam limitados ao que a tabela 12.2 permite.
- **Stack (pendência 8):** Q8 depende das respostas de escopo. O primeiro código sem CI exige ADR
  ou a pendência 15 resolvida (`../CLAUDE.md` §6b).
- **Demo e pitch (pendências 10 e 16):** Q6 depende de Q3 e da resposta dada a Q2.

### 12.4 Números com fonte lida

Inventário do que existe, para o grupo saber de onde um número pode vir. **Não indica o que
usar.** Os valores, as páginas e os limites de cada fonte estão no registro de
[`entrega.md`](entrega.md) e em [`desafios/13-recursos.md`](desafios/13-recursos.md). Todos os
valores dos kits de imprensa são de páginas anteriores ao lançamento.

| Decisão ou recurso (3.1) | Há número em fonte lida? |
|---|---|
| Massa de nave | sim: NISAR e Europa Clipper (kits de imprensa, valores de projeto); CubeSat de 1U (CubeSat 101) |
| Energia | sim, só NISAR; a página do Europa Clipper dá o tamanho dos painéis, não a potência |
| Comunicações | sim, só NISAR (taxas dos enlaces de descida) |
| Dados gerados pelos instrumentos | não |
| Orçamento | as páginas dos kits de imprensa trazem o investimento total de cada missão; nenhum custo por componente foi lido |
| Tempo | duração da missão principal nos kits de imprensa; prazos de desenvolvimento por etapa no CubeSat 101 |
| Instrumentos (massa, consumo, dados e custo de cada um) | não |
| Órbitas e suas características | só a cobertura e a revisita da NISAR; nenhuma altitude, nem comparação entre órbitas |
| Veículos lançadores (capacidade e custo) | não; os kits só dizem qual lançador cada missão usa |
| Margens | não (L2) |

Uma ficha da missão MAVEN, com massa e potência, foi baixada e não está entre os recursos
escolhidos pelo grupo; está descrita em [`desafios/13-recursos.md`](desafios/13-recursos.md).

## 13. Fontes

Todas consultadas em 14/11/2026. Grau de evidência: **primária** (documento oficial ou relatório da
agência), **secundária oficial** (página da agência que resume outro documento), **material
educativo** (sem avaliação de resultado publicada), **estudo** (pesquisa com avaliação), **oficial
do evento** (página do Space Apps) e **notícia institucional** (texto de divulgação da agência).

| # | Fonte | Tipo e grau | Link | Licença e termos |
|---|---|---|---|---|
| S1 | Wright, M. R. (2018). *Flight Systems Integration & Test: Lessons Learned for Future Success*. NASA Goddard. NTRS 20180003229 (número conforme o endereço do arquivo) | primária; artigo para os anais da conferência SpaceOps 2018, hospedado no NTRS; revisão por pares `[VERIFICAR]` | https://ntrs.nasa.gov/api/citations/20180003229/downloads/20180003229.pdf | documento do governo dos EUA; termos específicos `[VERIFICAR]` |
| S2 | NASA. *NASA Systems Engineering Handbook*, NASA/SP-2016-6105 Rev2 | primária, guia de referência da agência | https://www.nasa.gov/sites/default/files/atoms/files/nasa_systems_engineering_handbook_0.pdf | documento do governo dos EUA; termos específicos `[VERIFICAR]` |
| S3 | GAO. *NASA: Better Mechanisms Needed for Sharing Lessons Learned*, GAO-02-195 (2002) | primária, relatório de auditoria | https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-02-195/html/GAOREPORTS-GAO-02-195.htm | domínio público (GAO) `[VERIFICAR]` |
| S4 | GAO. *Survey of NASA's Lessons Learned Process*, GAO-01-1015R (2001) | primária, relatório de auditoria | https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-01-1015R/html/GAOREPORTS-GAO-01-1015R.htm | domínio público (GAO) `[VERIFICAR]` |
| S5 | NASA Science. *Mars Climate Orbiter* | secundária oficial (resumo; o relatório da comissão não foi lido) | https://science.nasa.gov/mission/mars-climate-orbiter/ | página oficial da NASA `[VERIFICAR]` |
| S6 | NASA JPL Education. *NASA Space Voyagers: The Game* | material educativo; sem avaliação de resultado | https://www.jpl.nasa.gov/edu/learn/project/nasa-space-voyagers-the-game/ | não indicada na página `[VERIFICAR]` |
| S7 | Arizona State University, Mars Education Program, sob contrato do JPL (NASA). *Marsbound! Mission to the Red Planet*, guia completo | material educativo; fichas antes e depois e rubricas, sem resultados no guia | https://d2pn8kiwq2w21t.cloudfront.net/documents/marsbound-fullguide.pdf (redirecionamento de `jpl.nasa.gov/edu/pdfs/marsbound-fullguide.pdf`) | "These materials may be distributed freely for non-commercial purposes. Copyright 2014; 2012; 2010; 2000." Restrição a uso não comercial: não é licença OSI, que é o que os termos do evento exigem de material de terceiros (`entrega.md`) |
| S8 | NASA Space Apps Challenge 2026. *Space Mission Design Game* (enunciado) | oficial do evento, regra do desafio | https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/ (texto em `assets/desafio-13-detalhes.txt`; impressão em `assets/NASA Space Apps Challenge.pdf`) | uso de conteúdo do evento conforme os termos do evento `[VERIFICAR]` |
| S9 | NASA Space Apps Challenge 2026. *Aba Recursos* do desafio 13 | oficial do evento, lista de recursos | https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/?tab=resources (texto em `assets/desafio-13-recursos.txt`; impressão em `assets/Resources.pdf`) | igual a S8 `[VERIFICAR]` |
| S10 | Ranalli, J.; Ritzko, J. (2013). *Assessing the Impact of Video Game Based Design Projects in a First Year Engineering Design Course*. Penn State Hazleton (ano e *Frontiers in Education* conforme o nome do arquivo, `Ranalli2013FIE.pdf`; ano e local de publicação `[VERIFICAR]`) | estudo preliminar; questionário de autoeficácia e atitude antes e depois da atividade | https://jranalli.github.io/preprints/Ranalli2013FIE.pdf (pré-publicação na página do autor; baixada em 14/11/2026) | não indicada `[VERIFICAR]` |
| S11 | ESA Academy. *116 students tackle real-world space mission design at ESA Academy's Concurrent Engineering Challenge 2025* | notícia institucional; oficina sem avaliação de aprendizagem reportada | https://esa.int/Education/ESA_Academy/116_students_tackle_real-world_space_mission_design_at_ESA_Academy_s_Concurrent_Engineering_Challenge_2025 | não indicada `[VERIFICAR]` |
| S12 | Levri, J. (NASA). *Design and Develop Science Missions*, série de webinars de engenharia de sistemas "Access to Space for All", 26/03/2025 (recurso 1 da aba). A capa traz o endereço `nasa.gov/smallsat-institute` | primária; material de treinamento da agência | https://www.nasa.gov/wp-content/uploads/2025/04/250323-design-and-develop-science-mission.pdf?emrc=a454cf | documento da NASA; termos de reuso não indicados no arquivo `[VERIFICAR]` |

Fontes encontradas em busca e **não usadas** por não terem sido lidas: apresentação do Goddard
(2014) sobre margens; artigo de Baker e Whalen sobre estudos de trade; relatório de Orion sobre
equilíbrio entre desempenho e massa; SEBoK (*System Analysis*); Wouters et al. (2013); Sinha e
Kapur (2021); UCL Systemisers; Purdue AeroQuest; KerbalEDU; e as fontes sobre o contexto brasileiro
(seção 7).
