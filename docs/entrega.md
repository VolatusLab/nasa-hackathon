# Entrega

O que a submissão exige, o que já está pronto e os dois registros que alimentam a página de
submissão: fontes de dados e uso de IA.

## Fontes

Páginas oficiais da edição 2026, lidas em 14/11/2026:

- Guia de submissão (13/11/2026): <https://www.spaceappschallenge.org/resources/project-submission-guide/>
- Guia de julgamento e prêmios (13/11/2026): <https://www.spaceappschallenge.org/resources/judging-awards-guide>
- Termos e condições do participante: <https://www.spaceappschallenge.org/legal/>
- Perguntas frequentes: <https://www.spaceappschallenge.org/resources/participant-faqs/>

Não lidos: o guia de formação de times (que as perguntas frequentes citam para menores de 18
anos) e a política de privacidade.

## Datas

| Item | Quando |
|---|---|
| Abertura da submissão | sábado, 14/11/2026, 9h00, no horário do evento local |
| **Prazo de submissão** | **domingo, 15/11/2026, 23h59, no horário do evento local** |
| Julgamento e premiação locais em Ceres-GO | `[VERIFICAR]` com a organização local (pode ter horário próprio) |
| Anúncio dos indicados globais (Global Nominees) | 03/12/2026 |
| Anúncio dos finalistas globais e menções honrosas | 17/12/2026 |
| Anúncio dos vencedores globais | 26/01/2027 |

Projeto salvo ou enviado depois do prazo não é julgado. Dá para editar e reenviar quantas vezes
quiser até o prazo; vale a última versão salva. Quem submete recebe certificado de participação.

## Requisitos para ser julgado

A situação do desafio fica em [`desafio.md`](desafio.md); as decisões em aberto, em
[`pendencias.md`](pendencias.md).

| Requisito | Situação |
|---|---|
| Responder a um dos desafios oficiais | ver [`desafio.md`](desafio.md) |
| Todos os integrantes, inclusive o dono do time, inscritos no Space Apps, no **mesmo evento local**, fora da lista de espera e visíveis na aba "Members" do time | `[VERIFICAR]` |
| Time com no máximo 6 pessoas; não entra integrante novo depois do prazo. Cada pessoa em um só time; cada time em um só desafio | atendido (5) |
| Todos os campos obrigatórios da página do projeto preenchidos (sem isso o botão de submeter não funciona) | pendente |
| Todo o conteúdo da página e dos materiais ligados **em inglês** | pendente |
| Demo: slides (até 7, contando título e introdução) **ou** vídeo (até 30 segundos). Passou do limite, fica fora do julgamento global | pendente |
| Links da demo e do projeto final **públicos**, sem senha, permissão ou cadastro | pendente: o link do projeto apontará para a versão de entrega em inglês ([ADR 0002](adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md)) |
| Usar ao menos um dado ou recurso da NASA (condição para prêmio global) | recursos escolhidos ([ADR 0005](adr/0005-recursos-nasa-primeira-versao.md)); uso no produto pendente |
| Sem **nome reconhecível, voz, imagem, vídeo ou outra representação de menor de 18 anos** em nada do que for submetido | **há integrante menor de 18 anos**: o nome, a voz e a imagem dele ficam fora da página, da demo e do projeto. Nos materiais de entrega ele aparece só por iniciais (ADR 0007), e o repositório não registra as iniciais; confirmação da organização `[VERIFICAR]` |
| Menor de 18 anos inscrito por pai, mãe ou responsável legal e acompanhado por ele durante todo o evento; o evento local pode ter exigências próprias | `[VERIFICAR]` com o grupo e com a organização local |
| Nenhum integrante participa por vínculo com a China ou com entidade de propriedade chinesa, inclusive universidades (o critério é vínculo institucional, não nacionalidade) | `[VERIFICAR]` |
| Marcar as duas caixas e clicar em "Submit for Judging" | pendente |

As duas caixas da submissão:

1. **Leitura e aceite:** declara que leu e entendeu o guia de submissão e aceita os termos e
   condições e a política de privacidade. Quem marca precisa ter lido.
2. **Trabalho original:** declara que o projeto é trabalho original do time, que todo recurso
   externo usado (código, texto, imagem, mesmo aberto ou gratuito) está listado no campo de
   referências, e que nenhum material com direito autoral foi usado sem permissão.

Quem está em lista de espera pede aceite ao líder local; sem resposta, o time inteiro precisa
mudar para um evento local com vaga.

## O que os termos exigem do conteúdo

- **Licença do conteúdo original:** fica disponível sem restrição ou sob licença de código
  aberto reconhecida pela Open Source Initiative (OSI). Se o time não indicar uma licença, a
  NASA distribui o conteúdo sob **Apache 2.0**. Tudo o que é submetido fica disponível para
  outros baixarem e usarem. O grupo adotou a Apache 2.0 (`LICENSE`,
  [ADR 0003](adr/0003-licenca-apache-2-0.md)).
- **Material de terceiros** (dado ou código que não seja da NASA nem de agência parceira):
  precisa ser público e sem restrição, ou ter licença OSI. As licenças desse material têm de
  constar na documentação submetida; sem isso a NASA não aceita nem publica a solução.
- **Toda fonte é citada**, mesmo aberta ou gratuita. Fonte não citada pode levar à remoção do
  material e à perda de indicação ou prêmio.
- **Não entra na submissão:** dado pessoal identificável (data de nascimento, endereço,
  telefone), material que promova produto ou serviço comercial, informação sujeita a controle
  de exportação dos Estados Unidos.
- **Uso de nome e imagem:** submeter autoriza a NASA a usar nome, local de residência, foto e
  imagem dos participantes na divulgação do evento. Quem aparece em vídeo precisa ter dado
  consentimento por escrito, e o time deve conseguir comprová-lo.
- **Menor de 18 anos:** além do que está na tabela, as perguntas frequentes dizem que o menor
  não deve usar foto própria no avatar nem na página do time. O guia de submissão pede os nomes
  dos integrantes nos slides, e os termos vetam nome reconhecível de menor. O grupo decidiu
  listá-lo só por iniciais ([ADR 0007](adr/0007-integrante-menor-por-iniciais.md)); falta a
  confirmação da organização local `[VERIFICAR]` ([`pendencias.md`](pendencias.md), item 3).

## Campos da página do projeto

Acesso: ícone do perfil → "My Team" → aba "Project" → "Edit". Salve com frequência ("Save
Progress"). O que é salvo fica visível só para o time até a submissão.

Há uma trava de edição ("Lock") para avisar que alguém está editando, mas outro integrante
consegue removê-la e sobrescrever o que não foi publicado. Combinem quem edita.

| Campo | O que pede |
|---|---|
| Project Name | nome do projeto |
| High-Level Project Summary | o que foi feito, como responde ao desafio, por que importa |
| Link to Project Demo | link público para os slides ou o vídeo |
| Link to Final Project | link público para o projeto (site, repositório, pasta na nuvem) |
| Detailed Project Description | o que faz, como funciona, benefícios, objetivos, ferramentas e linguagens usadas |
| Use of Super Intelligence (SI) | se houve uso de IA e como (ver abaixo) |
| NASA Data | quais dados e recursos da NASA foram usados, com detalhe |
| Space Agency Partner Data and Other References | todos os dados, recursos e ferramentas usados, inclusive código, texto e imagem de terceiros |

A página aceita imagens (JPG, PNG, GIF, até 10 MB). Vídeo e documento entram só por link.
Teste cada link em janela anônima antes de submeter.

**A maior parte da avaliação vem da página do projeto.** A demo conta, principalmente para o
critério "Apresentação".

Se o projeto final for um site novo, o guia recomenda (sem exigir) pedir a classificação do
site no FortiGuard Web Filter, para reduzir o risco de os jurados não conseguirem abri-lo. O
passo a passo está no guia de submissão.

## Demo

- **Vídeo, até 30 segundos.** Pode ser falado em português, desde que tenha legenda em inglês.
  Roteiro sugerido pelo guia: apresentação do time (0:00), desafio e motivação (0:02), nome e
  chamada do projeto (0:05), como funciona e como os dados abertos tornaram a solução possível
  (0:10), visão de futuro (0:20 a 0:30).
- **Slides, até 7**, em inglês. Precisam trazer o nome do time, os nomes dos integrantes e o
  desafio escolhido, além de imagem do projeto, a experiência do usuário e como os dados da NASA
  e de agências parceiras tornam a solução possível.
- Hospedagem externa (YouTube, Google Drive, GitHub etc.), com link público.
- O guia recomenda definir cedo o formato e indicar um integrante para conduzir a demo.
- A palestra de pitch da organização local (14/11/2026) sugeriu um pitch final de 3 min para a
  banca, ao vivo, e gravar a demo antes como plano B. É dica da palestra, não regra do evento.
  Estrutura, roteiro, ensaio e o que fica `[VERIFICAR]` estão em [`pitch-final.md`](pitch-final.md).

## Uso de IA

O guia de 2026 chama de "Super Intelligence (SI)" o que aqui se chama de IA (aprendizado de
máquina, chatbots, geração de imagem, modelos de linguagem).

- O uso é permitido como ferramenta para acelerar o trabalho.
- O guia diz que a IA **não deve ser usada para conceber a ideia** de como resolver o desafio.
- Conteúdo gerado não pode usar nem alterar marcas da NASA (logotipos, bandeiras,
  identificadores de missão).
- É obrigatório indicar onde e como a IA foi usada:
  - imagem e vídeo: marca d'água visível;
  - áudio: aviso no texto descritivo e nos metadados;
  - código e dados: aviso no texto descritivo e nos metadados.
- A resposta ao campo de IA não é vista pelos jurados, mas as indicações dentro do projeto são.

## Critérios de julgamento

Nota de 1 a 5 em cada critério, em todas as fases.

| Critério | O que os jurados olham |
|---|---|
| Impacto | o tamanho do problema atacado e quantas pessoas a solução ajuda ou inspira |
| Criatividade | originalidade: conceito novo ou melhoria relevante sobre ideias existentes |
| Validade | base científica, viabilidade técnica, o quanto está desenvolvida e a facilidade de uso |
| Relevância | o quanto responde ao desafio e usa dado da NASA como parte central, não como enfeite |
| Apresentação | clareza e narrativa ao comunicar o desafio, a solução e a importância; vale a demo e o projeto inteiro |

O guia pede a mesma atenção ao quinto critério que aos outros quatro, e recomenda reservar tempo
e gente para o pitch.

## Registro de fontes de dados

Preencha no mesmo pull request que passa a usar o dado. Alimenta os campos "NASA Data" e
"Space Agency Partner Data and Other References". A coluna de licença é obrigatória para todo
material que não seja da NASA nem de agência parceira.

| Dado ou recurso | Agência ou origem | Link | Licença | Acessado em | Para que usamos |
|---|---|---|---|---|---|
| Enunciado do desafio 13 (página oficial) | NASA Space Apps Challenge 2026 | <https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/> | termos do evento `[VERIFICAR]` | 14/11/2026 | regra do desafio; tradução e problemática |
| Aba Recursos do desafio 13 | NASA Space Apps Challenge 2026 | <https://www.spaceappschallenge.org/2026/challenges/space-mission-design-game/?tab=resources> | termos do evento `[VERIFICAR]` | 14/11/2026 | lista de recursos do desafio |
| Design and Develop Science Missions (webinar "Access to Space for All", 26/03/2025; recurso 1 da aba) | NASA (a capa traz o endereço do SmallSat Institute) | <https://www.nasa.gov/wp-content/uploads/2025/04/250323-design-and-develop-science-mission.pdf?emrc=a454cf> | documento da NASA; termos não indicados `[VERIFICAR]` | 14/11/2026 | problemática: etapas de projeto e ligação entre requisito e verificação |
| Demais recursos da aba: GMAT, Concept Maturity Levels, CubeSat 101, desafio de 2023 e CSA | NASA, JPL, CSA | links, termos e limites de leitura de cada um em [`desafios/13-recursos.md`](desafios/13-recursos.md) | ver o documento; CML com CC0 1.0 na página do repositório; os demais `[VERIFICAR]` | 14/11/2026 | descritos a partir da página de cada recurso ou da aba; o conteúdo principal não foi lido no CML, no desafio de 2023 e nos jogos da CSA, e só em parte no CubeSat 101. Ainda não usados no produto |
| Flight Systems Integration & Test: Lessons Learned for Future Success (Wright, 2018), NTRS 20180003229 | NASA Goddard | <https://ntrs.nasa.gov/api/citations/20180003229/downloads/20180003229.pdf> | governo dos EUA `[VERIFICAR]` | 14/11/2026 | problemática: integração e teste como etapa de verificação |
| NASA Systems Engineering Handbook, NASA/SP-2016-6105 Rev2 | NASA | <https://www.nasa.gov/sites/default/files/atoms/files/nasa_systems_engineering_handbook_0.pdf> | governo dos EUA `[VERIFICAR]` | 14/11/2026 | problemática: margem de projeto e estudos de trade |
| GAO-02-195, NASA: Better Mechanisms Needed for Sharing Lessons Learned | GAO | <https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-02-195/html/GAOREPORTS-GAO-02-195.htm> | domínio público `[VERIFICAR]` | 14/11/2026 | problemática: lições não aplicadas e perda da Mars Polar Lander |
| GAO-01-1015R, Survey of NASA's Lessons Learned Process | GAO | <https://www.govinfo.gov/content/pkg/GAOREPORTS-GAO-01-1015R/html/GAOREPORTS-GAO-01-1015R.htm> | domínio público `[VERIFICAR]` | 14/11/2026 | problemática: barreiras culturais ao registro de lições |
| Mars Climate Orbiter (página oficial da NASA) | NASA Science | <https://science.nasa.gov/mission/mars-climate-orbiter/> | página oficial `[VERIFICAR]` | 14/11/2026 | problemática: causa resumida da perda; relatório da comissão ainda não lido |
| NASA Space Voyagers: The Game | NASA JPL Education | <https://www.jpl.nasa.gov/edu/learn/project/nasa-space-voyagers-the-game/> | não indicada `[VERIFICAR]` | 14/11/2026 | problemática: ferramentas existentes |
| Marsbound! Mission to the Red Planet (guia completo) | Arizona State University (Mars Education Program), sob contrato do JPL (NASA) | <https://d2pn8kiwq2w21t.cloudfront.net/documents/marsbound-fullguide.pdf> | "may be distributed freely for non-commercial purposes", com copyright de 2000 a 2014. Não é licença OSI: só citar e apontar por link | 14/11/2026 | problemática: ferramentas existentes, com fichas antes e depois da atividade |
| NASA Mission Viz | NASA | <https://nasa.github.io/mission-viz/> | sem arquivo de licença na raiz do repositório (zip baixado em 14/11/2026; API do GitHub retorna licença nula). A consulta à API é de 14/11/2026, sem cópia guardada. A pasta `X3Dom/` traz a licença da biblioteca X3DOM (MIT e GPL), que não cobre o restante. O repositório embute outras obras de terceiros com termos próprios: three.js e jQuery (MIT), CanvasMatrix (Apple) e a ontologia `OntologyDrivenOrrery/SSAO_Rovetto.owl` (© Robert John Rovetto), que diz "Not authorized for commercial use unless explicitly negotiated with the copyright holder" e exige atribuição. Essa restrição cobre a ontologia, não o repositório, e não é licença OSI. Código não copiado; `[VERIFICAR]` com a NASA | 14/11/2026 | uso decidido no ADR 0005: só link, sem incorporação |
| Mission Design Lab | NASA GSFC | <https://etd.gsfc.nasa.gov/capabilities/integrated-design-center/mission-design-lab/> | página oficial da NASA; termos de reuso não indicados `[VERIFICAR]` | 14/11/2026 | problemática: níveis de estudo do MDL |
| A Learning Game About Telescopes (Webb) | NASA Science | <https://science.nasa.gov/mission/webb/game-build-it-yourself/> | sem termos de reuso na página (14/11/2026); conteúdo do jogo não verificado `[VERIFICAR]`; imagem com nome de arquivo CC BY-NC 2.0 não usada | 14/11/2026 | uso decidido no ADR 0005: só link, como referência de design |
| Ranalli e Ritzko (2013), *Assessing the Impact of Video Game Based Design Projects in a First Year Engineering Design Course* | pesquisa acadêmica | <https://jranalli.github.io/preprints/Ranalli2013FIE.pdf> | não indicada `[VERIFICAR]` | 14/11/2026 | problemática: estudo preliminar, com questionário de autoeficácia antes e depois de um projeto feito no jogo |
| ESA Academy, Concurrent Engineering Challenge 2025 | ESA Academy | <https://esa.int/Education/ESA_Academy/116_students_tackle_real-world_space_mission_design_at_ESA_Academy_s_Concurrent_Engineering_Challenge_2025> | termos em página separada do site da ESA, não lida `[VERIFICAR]` | 14/11/2026 | problemática: oficina de projeto de missão para universitários |
| Números de projeto da missão NISAR (kit de imprensa JPL, *quick facts*) | NASA/JPL | <https://www.jpl.nasa.gov/press-kits/nisar/quick-facts/> | sem cláusula de uso para os números; imagens sob a política de imagem do JPL, apontada no rodapé e não lida `[VERIFICAR]` | 14/11/2026 | valores de referência (ADR 0005), ainda não usados no produto. A página traz: massa de lançamento de cerca de 2.380 kg, com propelente; cerca de 5 kW dos painéis solares; dois enlaces de descida em banda Ka, de 2,88 Gbps para a estação da ISRO e de 4,0 Gbps para estações da NASA; missão principal de três anos; cobertura das superfícies de terra e gelo entre 77,5° N e 87,5° S, duas vezes a cada 12 dias; lançador GSLV, da ISRO; investimento da NASA de US$ 1,1589 bilhão e da ISRO de ₹ 7,88 bilhões. A página é anterior ao lançamento ("Targeted for July 30, 2025"): valores de projeto, não medidos |
| Números de projeto da missão Europa Clipper (kit de imprensa JPL, *quick facts*) | NASA/JPL | <https://www.jpl.nasa.gov/press-kits/europa-clipper/quick-facts/> | sem cláusula de uso para os números `[VERIFICAR]` | 14/11/2026 | valores de referência (ADR 0005), ainda não usados no produto. A página traz: massa de lançamento de cerca de 5.800 kg, dos quais cerca de 2.750 kg de propelente; painéis solares de cerca de 14,2 m por 4,1 m cada; lançador Falcon Heavy; cerca de 5 anos e meio de viagem até Júpiter e missão principal de pouco mais de quatro anos depois da chegada; investimento total de cerca de US$ 5,2 bilhões. Não traz potência em watts nem taxa de dados. A página é anterior ao lançamento (período previsto de 10 a 30 de outubro; o ano, 2024, vem da lista de marcos da mesma página). Ela traz uma imagem com processamento de terceiro sob CC BY 3.0, não usada |

Dado de agência parceira é incentivado, não exigido. As parceiras de 2026 incluem a Agência
Espacial Brasileira; a lista completa está no guia de submissão.

## Registro de uso de IA

Alimenta o campo "Use of Super Intelligence (SI)".

| Ferramenta | Para quê | Onde aparece | Data |
|---|---|---|---|
| Claude Code (Anthropic) | redação da documentação de base e dos arquivos de configuração do repositório | raiz do repositório, `.github/`, `docs/` | 14/11/2026 |
| Claude Code (Anthropic) | leitura das páginas oficiais e resumo em português dos 14 desafios, sem proposta de solução | `docs/desafios/` | 14/11/2026 |
| Claude Code (Anthropic) | revisão da documentação contra as páginas oficiais e correções | raiz do repositório, `docs/` | 14/11/2026 |
| Claude Code (Anthropic) | redação do registro da escolha do desafio 13 (ADR 0004) e atualização de estado, pendências e README | `docs/adr/`, `docs/`, `README.md`, `CLAUDE.md`, `CHANGELOG.md` | 14/11/2026 |
| Claude Code (Anthropic) | leitura da lista de recursos do evento e das notas da palestra de pitch, e registro nos documentos do desafio 13 e da entrega | `docs/desafios/13-jogo-de-projeto-de-missao.md`, `docs/entrega.md` | 14/11/2026 |
| Claude Code (Anthropic) | redação do modelo de pitch de 10 segundos, com lacunas e exemplos de problema (sem solução) | `docs/pitch.md` | 14/11/2026 |
| Claude Code (Anthropic) | tradução integral do enunciado do desafio 13 e da aba Recursos para pt-BR, a partir dos textos oficiais impressos em PDF | `docs/desafios/13-enunciado-completo.md`, `docs/desafios/13-jogo-de-projeto-de-missao.md` | 14/11/2026 |
| Claude Code (Anthropic) | redação da problemática do desafio 13 (camadas, tensões e perguntas de decisão), a partir das fontes listadas no registro de fontes | `docs/problematica.md` | 14/11/2026 |
| Claude Code (Anthropic) | reescrita da problemática com foco em prática e avaliação | `docs/problematica.md` | 14/11/2026 |
| Claude Code (Anthropic) | análise e revisão por pares dos recursos da NASA, redação do ADR 0005 e dos registros de fontes do ADR 0005 | `docs/adr/0005-recursos-nasa-primeira-versao.md`, `docs/entrega.md` | 14/11/2026 |
| Claude Code (Anthropic) | redação dos ADRs 0006 e 0007 e ajustes de consistência | `docs/adr/`, `docs/`, `CLAUDE.md`, `CHANGELOG.md` | 14/11/2026 |
| Claude Code (Anthropic) | leitura dos nove recursos da aba oficial nos arquivos baixados e descrição de cada um, sem recomendação de uso | `docs/desafios/13-recursos.md` | 14/11/2026 |
| Claude Code (Anthropic) | consolidação da problemática: o que o enunciado pede e o que sugere, e o que o pitch pode afirmar com fonte | `docs/problematica.md` | 14/11/2026 |
| Claude Code (Anthropic) | revisão geral do repositório, seguida de revisão por pares com agentes: conferência das citações e da tradução contra os arquivos-fonte, correções nos documentos, no `.gitattributes` e no `.gitignore` | raiz do repositório, `docs/` | 14/11/2026 |
| Claude Code (Anthropic) | redação do guia do pitch final de 3 minutos (estrutura, tempos, lacunas, regras e checklists, sem proposta de solução), a partir das notas da palestra de pitch e dos documentos do repositório | `docs/pitch-final.md`, `docs/entrega.md`, `docs/pitch.md`, `docs/README.md`, `CLAUDE.md`, `CHANGELOG.md` | 15/11/2026 |

## Material da entrega

| Item | Link | Situação |
|---|---|---|
| Página do projeto no Space Apps | | pendente |
| Demo (slides ou vídeo) | | pendente |
| Projeto final (site, repositório ou pasta) | | pendente |
