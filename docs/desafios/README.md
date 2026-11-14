# Os 14 desafios de 2026

Um documento por desafio, para apoiar a escolha do grupo. Cada um traz o contexto, o que é
pedido, o que o enunciado sugere considerar, os dados e recursos indicados (com link) e uma
seção final com pontos para a decisão.

## Como estes documentos foram feitos

- **Fonte:** a página de detalhes e a página de recursos de cada desafio em
  <https://www.spaceappschallenge.org/2026/challenges/>, lidas em 14/11/2026. As páginas avisam
  que mais recursos podem ser acrescentados.
- **São resumos em português, não tradução integral.** Antes de decidir, leia o enunciado
  original do desafio escolhido. Exceção: o desafio 13 tem a tradução integral do enunciado em
  [`13-enunciado-completo.md`](13-enunciado-completo.md), feita a partir do texto oficial de 14/11/2026.
- **Redigidos com IA** (Claude Code), registrado em [`../entrega.md`](../entrega.md).
- **Não trazem proposta de solução.** O guia do evento diz que a IA não deve ser usada para
  conceber como resolver o desafio, então cada documento descreve o problema e levanta
  perguntas; a ideia é do grupo.
  Os exemplos de solução que aparecem são os citados pelo próprio enunciado.
- O trecho "Onde está a dificuldade" é leitura de quem resumiu, não informação do evento.
- O evento chama IA de "Super Intelligence (SI)".

## Comparativo

| # | Desafio | Nível | Entrega pedida | Dado central | Público do produto |
|---|---|---|---|---|---|
| [01](01-equipamentos-abandonados.md) | Abandoned but not Forgotten | iniciante/jovem, intermediário | narrativa ou ferramenta educativa (formato livre) | catálogo NSSDCA e páginas de missão | estudantes e público casual |
| [02](02-detetive-de-tendencias.md) | Be An Earth System Trend Detective! | avançado | ferramenta com série temporal e teste de significância | variáveis de ciências da Terra (Giovanni, AppEEARS) | estudantes e público com base científica |
| [03](03-treinador-de-astronauta-junior.md) | Build a Junior Astronaut Mission Trainer | iniciante/jovem, intermediário | jogo ou app jogável | APIs abertas da NASA (DONKI, OSDR, RadLab) | crianças de 7 a 12 anos |
| [04](04-saude-de-astronautas.md) | Create Health Monitoring Software for Astronauts | intermediário | software com interface visual | artigos do programa de pesquisa humana da NASA | astronautas |
| [05](05-dancando-com-os-sars.md) | Dancing with the SARs | intermediário, avançado | aplicação interativa de código aberto | radar da missão NISAR (obrigatório) | cientistas, gestores, educadores, público |
| [06](06-rotacao-de-culturas.md) | Field Shift: Adapting Farms with NASA Data | intermediário, avançado | ferramenta de apoio à decisão | observação da Terra (SMAP, GPM, Landsat, POWER) mais dado local | produtores rurais |
| [07](07-chama-em-queda-livre.md) | Flame in Freefall | intermediário, avançado | painel web com IA | banco PSI de combustão (obrigatório) | acadêmicos e engenheiros aeroespaciais |
| [08](08-focos-de-calor-modis-viirs.md) | Harmonization of MODIS and VIIRS Hot Spots | intermediário, avançado | aplicação web com calendário de queima | focos de calor MODIS e VIIRS (obrigatório); o FIRMS é a fonte sugerida | resposta a emergências, gestores, bombeiros |
| [09](09-analogos-terrestres.md) | Identify Earth Locations that Analog the Permanent Moon Base Locations and Mars | iniciante/jovem, intermediário, avançado | mapa, visualização, relatório ou outra forma | dados da Terra mais dados da Lua ou de Marte | cientistas, engenheiros, público |
| [10](10-mapa-marciano.md) | Interplanetary Survival Guide: Martian Map | intermediário | mapa, ferramenta ou interface | camadas de Marte (Mars Trek, mapa geológico, imagens de rover) | astronauta em Marte |
| [11](11-navegador-de-pouso-lunar.md) | Lunar Landing Site Navigator | intermediário, avançado | ferramenta de comparação com visualização | efemérides do JPL Horizons, topografia lunar | planejadores de missão, educadores, público |
| [12](12-planeta-x-e-spherex.md) | Planet X and SPHEREx | avançado | ferramenta web pública | imagens da missão SPHEREx (obrigatório) | cientistas cidadãos |
| [13](13-jogo-de-projeto-de-missao.md) | Space Mission Design Game | iniciante/jovem, intermediário | jogo ou simulação | documentos e ferramentas de projeto de missão | estudantes e aspirantes a engenheiros |
| [14](14-jukebox-da-terra.md) | The Earth Information Jukebox | iniciante/jovem, intermediário | ferramenta interativa ou coleção de áudios | visualizações do EIC (obrigatório) | público geral, com foco em acessibilidade |

## Agrupamentos que ajudam a filtrar

**Por nível indicado pelo evento**

- Com nível iniciante/jovem: 01, 03, 09, 13, 14.
- Só intermediário: 04, 10.
- Intermediário e avançado: 05, 06, 07, 08, 11.
- Só avançado: 02, 12.

**Por tipo de entrega**

- Jogo: 03, 13.
- Narrativa ou arte: 01 (código não é obrigatório) e 14 (aceita coleção de áudios gerados, sem
  aplicação interativa); o 09 aceita relatório escrito.
- Ferramenta ou aplicação com dados de observação da Terra: 02, 05, 06, 08 (só o 08 pede
  expressamente aplicação web).
- Ferramenta para missão na Lua ou em Marte: 10, 11.
- Painel ou software de apoio: 04, 07.
- Ferramenta web de astronomia: 12.

**Por natureza do dado**

- Dado pronto, de acesso direto (imagens, vídeos, páginas, APIs simples): 01, 03, 14.
- Dado tabular ou calculado: 08 (focos de calor), 11 (efemérides), 02 (séries temporais).
- Dado de sensoriamento que exige processamento especializado: 05 (radar), 06 (várias fontes),
  12 (imagens astronômicas), 09 (acervo planetário).
- Camadas e imagens em portais de visualização, a extrair: 10 (Marte).
- Banco de registros de experimentos, em formato a descobrir: 07 (combustão).
- Sem conjunto de dados numérico indicado (recursos são artigos e documentos): 04, 13. Nesses,
  mostrar o dado da NASA como parte central do produto exige mais cuidado.

**Com escopo descrito de forma mais fechada** (entrada e saída definidas pelo enunciado)

08, 11 e 12. O 12 traz inclusive alvos de teste.

## Lembretes do evento que pesam na escolha

- A submissão fecha em **15/11/2026, 23h59**. O que não der para demonstrar até lá não conta.
- É preciso usar **ao menos um dado ou recurso da NASA** para concorrer a prêmio global.
- "Relevância" (um dos cinco critérios) mede o quanto o dado da NASA é parte central da solução.
- A entrega é **em inglês**.
- Detalhes em [`../entrega.md`](../entrega.md). Critérios do grupo e registro da decisão em
  [`../desafio.md`](../desafio.md).
