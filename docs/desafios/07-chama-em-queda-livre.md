# 07 — Flame in Freefall: SI-Powered Fire Safety Insights from Microgravity Combustion Data

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/flame-in-freefall/>
  (lida em 14/11/2026)
- **Nível:** intermediário, avançado
- **Temas:** exploração espacial

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.
O evento chama IA de "Super Intelligence (SI)".

## Em uma frase

Criar um painel web interativo, com IA, que resume, classifica por relevância e interpreta os experimentos de
combustão em microgravidade da NASA para tirar deles orientações de segurança contra fogo na
exploração espacial humana.

## Contexto

Fogo é um dos maiores perigos em missão espacial. O enunciado lembra o alarme de fumaça que
disparou na Artemis II, a explosão de tanque de oxigênio da Apollo 13, o incêndio na estação Mir
e a morte da tripulação da Apollo 1 em teste antes do lançamento (1967).

Em microgravidade a chama se comporta de outro jeito: sem empuxo, os gases quentes não sobem, e
uma chama de vela vira uma esfera azulada que depende de difusão para receber oxigênio.

O trabalho de segurança da NASA tem três frentes, cada uma com experimentos próprios:

| Frente | O que estuda | Experimentos citados |
|---|---|---|
| Prevenção | fontes de ignição e escolha de materiais (limites de inflamabilidade de tecidos e plásticos) | BASS, BASS-II, Saffire-I, II e III |
| Detecção | fumaça e aerossóis em microgravidade | SAME, SAME-R |
| Supressão | diluição da atmosfera com dióxido de carbono e hélio | FLEX |

## O que é pedido

Um **painel web com IA** sobre os experimentos de combustão disponíveis no banco PSI (Physical
Sciences Informatics) da NASA. Os dados são públicos, mas são muitos: difíceis de achar, de
comparar e de interpretar. O painel poderia permitir ao usuário:

- identificar os experimentos mais relevantes para a segurança de ambientes habitados (naves,
  estações, bases na Lua e em Marte, rovers pressurizados);
- extrair dados que apoiem modelos preditivos de inflamabilidade e de cenários de fogo;
- destacar pesquisas que orientam a próxima geração de controles e equipamentos.

Também pode tratar de aplicações na Terra (extintores de névoa fina, detectores de fumaça,
equipamento de bombeiro, todos com origem em tecnologia espacial).

**Fora do escopo:** segurança de foguetes e propelentes, que o banco PSI em geral não cobre.

## O que o enunciado sugere considerar

- **Público:** professores, estudantes de graduação e pós, pesquisadores e engenheiros
  aeroespaciais.
- **Atributos a resumir e exibir:** objetivos do experimento; combustíveis (forma e tamanho das
  amostras ou queimadores); condições de teste (concentração de oxigênio, velocidade do fluxo de
  ar); o que variou e o que ficou igual entre testes do mesmo experimento; sensores e tipos de
  medição.
- **Comparar** semelhanças e diferenças entre experimentos.
- **Outros experimentos no PSI:** DAFT e DAFT-2 (o mesmo instrumento de fumaça usado para
  poeira); BRE, do projeto ACME (inflamabilidade em atmosfera parada).
- **Equipamento:** os seis experimentos do ACME usaram o mesmo conjunto modular no rack CIR;
  FLEX, FLEX-2 e CFI queimaram gotas de combustível líquido no aparato MDCA; BASS, BASS-II,
  SPICE e SLICE usaram a Microgravity Science Glovebox.
- **Trajes e oxigênio:** o traje espacial usa 100% de oxigênio a 4,3 psi (ao nível do mar a
  pressão é 14,7 psi). A base lunar e os rovers devem operar em condição intermediária,
  provavelmente com 30% de oxigênio ou mais e 10,2 psi ou menos, o que torna os materiais bem
  mais inflamáveis. Os testes com mais oxigênio (até 85%) foram os do CFI-G.
- **Gravidade parcial:** **ainda não há dado de gravidade parcial no PSI.** Estão previstos os
  experimentos LUCI e FM2. O E-FIELD Flames imitou gravidade parcial com campo elétrico.
  Resultados em microgravidade e em gravidade normal podem delimitar o que ocorre no meio.

## Dados e recursos indicados

| Recurso | O que oferece |
|---|---|
| [PSI Data Repository: Combustion Science](https://psi.nasa.gov/physci/repo/search?q=combustion) | **a fonte dos dados em que o projeto deve se basear** |
| [NASA Combustion Science](https://www.nasa.gov/glenn/glenn-expertise-space-exploration/physical-sciences-program/combustion-science/) | informação básica sobre a maioria dos experimentos do PSI |
| [Vídeo: combustão na estação espacial](https://www.youtube.com/watch?v=W1oXykoz9zg) | introdução de 3,6 minutos (2018) |
| [Guia do pesquisador: combustão na ISS](https://www.nasa.gov/missions/station/a-researchers-guide-to-combustion-science/) | revisão de 2015, com mais de 50 páginas |
| [Apollo 1](https://sma.nasa.gov/sma-disciplines/accllp/apollo-1) | o incêndio, a investigação e as lições |
| [Apollo 13](https://sma.nasa.gov/sma-disciplines/accllp/apollo-13) | a explosão, a investigação e as lições |
| [Incêndio na Mir](https://www.nasa.gov/history/25-years-ago-fire-aboard-space-station-mir/) | o incêndio de 1997 |
| [Tanques de ar de bombeiro](https://spinoff.nasa.gov/node/9582) | adaptação de tecnologia de traje espacial (anos 1970) |
| [Detector de incêndio](https://spinoff.nasa.gov/node/9407) | detector que distingue fumaça de poeira |
| [Roupa de combate a incêndio](https://spinoff.nasa.gov/node/9918) | aplicação de tecnologia de traje espacial (anos 1980) |

A página não lista recursos de agências parceiras para este desafio.

## Para a escolha do grupo

- **Público declarado:** acadêmicos e engenheiros aeroespaciais.
- **Entrega esperada:** painel web com IA.
- **Dado obrigatório:** o banco PSI.
- **Natureza dos dados:** registros de experimentos científicos (descrição, condições,
  medições), em volume grande e formato a descobrir no próprio PSI.
- **Onde está a dificuldade** (leitura de quem resumiu): o domínio é especializado (ciência da
  combustão) e o público é técnico, então uma interpretação errada da IA aparece. O critério
  "Validade" pede que o que o painel afirma esteja de acordo com os experimentos. Há também a
  regra do evento de identificar conteúdo gerado por IA.
- **Perguntas para o grupo responder antes de escolher:**
  - Conseguimos abrir o PSI e entender a forma dos dados ainda hoje? Há download ou API?
  - Como o grupo confere que o que o painel afirma bate com os experimentos, e quem faz isso?
  - Usar IA no produto tem custo ou chave de API? De quem?
