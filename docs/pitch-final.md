# Pitch final de 3 minutos: desafio 13

Guia para montar, ensaiar e apresentar o pitch ao vivo para a banca local. Traz estrutura, tempos,
lacunas e regras. **A ideia da solução é do grupo** ([`entrega.md`](entrega.md), seção "Uso de IA";
[`../CLAUDE.md`](../CLAUDE.md) §1): este documento não propõe mecânica, público, recurso da NASA
nem solução. Toda lacuna `[...]` é do grupo.

O one-liner de 10 s está em [`pitch.md`](pitch.md). A demo da submissão (vídeo de 30 s ou 7 slides
em inglês) segue as regras de [`entrega.md`](entrega.md), seção "Demo", e é outra peça.

## 1. Status e origem

| O quê | Situação | Base |
|---|---|---|
| Existe um pitch final ao vivo para a banca | dica da palestra de pitch do evento local (14/11/2026), **não regra do evento** | `assets/Pitch em Órbita (4).html` |
| Duração de 3 min | sugerida pela palestra; `[VERIFICAR]` com a organização de Ceres-GO | [`pendencias.md`](pendencias.md), item 14 |
| Divisão 40 s · 80 s · 30 s · 30 s e os cinco estágios | exemplo da palestra, não regra | palestra, slides "como dividir os 3 minutos" e "os cinco estágios do foguete" |
| Horário, sala, projetor, tempo de perguntas, quem é a banca | `[VERIFICAR]` com a organização | pendência 14 |
| Idioma | **decisão do grupo: tudo em português** (fala e slides do pitch). Confirmar com a organização que a banca local aceita `[VERIFICAR]` | decisão de 15/11/2026 |
| Peso no resultado | o julgamento global usa a página do projeto e a demo, não este pitch. Se o pitch ao vivo conta no julgamento local, e quanto, é `[VERIFICAR]` | [`entrega.md`](entrega.md), "Campos da página do projeto" e "Critérios de julgamento" |

Se a organização confirmar outra duração, mantenha a proporção dos estágios (seção 3) e refaça o
orçamento de palavras (seção 4).

## 2. O que a banca avalia

Os critérios oficiais estão em [`entrega.md`](entrega.md), "Critérios de julgamento" (nota de 1 a
5 em cada um). Se a banca local usar outros critérios, `[VERIFICAR]`. A coluna da direita mostra
onde o pitch responde a cada critério.

| Critério | Onde o pitch responde |
|---|---|
| Impacto | Problema (estágio 1): o tamanho do problema e para quem ele existe |
| Criatividade | Diferencial (estágio 4): o que é novo, ou o que melhora sobre o que existe |
| Validade | Prova (estágio 3): o que funciona de fato na demo, e de onde vêm os números |
| Relevância | Solução e Prova (estágios 2 e 3): responde ao pedido do desafio e usa dado da NASA **como parte central, não como enfeite** |
| Apresentação | o pitch inteiro: clareza, narrativa e tempo |

O pedido do desafio, nas palavras do enunciado, está na seção 12.1 de
[`problematica.md`](problematica.md). Em Relevância, a banca compara o que vê com esse pedido.

## 3. Estrutura: cinco estágios em quatro blocos de tempo

Estrutura da palestra. Solução e Prova dividem os 80 s: a dica da palestra é "falem pouco e
mostrem a demo".

| Bloco | Tempo | Estágio | Pergunta que responde |
|---|---|---|---|
| 0:00–0:40 | 40 s | 1. Problema | Por que isso importa, e para quem? |
| 0:40–2:00 | 80 s | 2. Solução | O que vocês construíram? |
| | | 3. Prova | A demo funcionando com dados da NASA |
| 2:00–2:30 | 30 s | 4. Diferencial | Por que isso, e não o que já existe? |
| 2:30–3:00 | 30 s | 5. Próximo passo | O que vem depois, e quem são vocês? |

### Estágio 1: Problema (40 s)

- **Contém:** quem tem o problema, o que acontece e por que importa. Sem tecnologia e sem solução.
- **Dica da palestra:** começar pelas pessoas, "com um número que dê escala". **Atenção:** hoje não
  há número com fonte lida sobre público, Brasil ou Ceres-GO (seção 12.2 de
  [`problematica.md`](problematica.md), lacuna L5 e seção 6). Sem fonte, não use número: abra
  pela situação, não por uma estatística.
- **Base que pode ser usada:** a seção 12.2 de [`problematica.md`](problematica.md), "Sobre o
  problema". Exemplos de frases que só descrevem o problema estão em [`pitch.md`](pitch.md); os
  exemplos 3 e 4 precisam vir atribuídos ao desafio ("o desafio aponta que...").
- **Lacunas:** `[quem]`, `[o que essa pessoa não consegue fazer hoje]`, `[por que isso importa]`.

### Estágio 2: Solução (parte dos 80 s)

- **Contém:** o nome do projeto e, em uma ou duas frases, o que o jogo permite fazer. Descreva só o
  que **foi entregue**, não o que está planejado.
- **Lacunas:** `[nome do projeto]` (pendência 9), `[o que o jogador faz]`, `[que decisões ele toma]`.
- **Liga ao desafio:** usar os termos do pedido (seção 12.1 de [`problematica.md`](problematica.md))
  só no que o jogo de fato cobre. "Missão completa, do conceito à operação" só vale se o entregue
  cobrir isso (Q1).

### Estágio 3: Prova (parte dos 80 s)

- **Contém:** a demo ao vivo, mostrando uma decisão e a consequência dela, e onde o dado da NASA
  aparece no jogo.
- **Dado da NASA:** dizer qual recurso, como ele entra e de onde vem. Os recursos da primeira versão
  estão no [ADR 0005](adr/0005-recursos-nasa-primeira-versao.md); como os números entram no jogo é a
  pendência 7. Os números de kit de imprensa são **valores de projeto publicados pela NASA**, de
  páginas anteriores ao lançamento: diga assim, não "dados medidos".
- **Lacunas:** `[cenário da demo]`, `[decisão mostrada]`, `[consequência mostrada]`,
  `[recurso da NASA e onde ele aparece na tela]`.
- **Fala:** narre o que a banca está vendo; não leia o slide. A demo consome parte do tempo sem
  fala corrida (seção 4).

### Estágio 4: Diferencial (30 s)

- **Contém:** por que isto, e não o que já existe.
- **Única forma permitida da alegação de lacuna:** a frase da seção 12.2 de
  [`problematica.md`](problematica.md) sobre as sete ferramentas lidas, com as ressalvas, depois de o
  grupo validar a leitura (pendência 17) e só se o entregue combinar com ela.
- **Proibido:** "não existe nada parecido", "é o primeiro jogo que...". A busca não foi
  sistemática.
- **Lacunas:** `[o que o jogo faz que as ferramentas lidas não fazem, dentro do que foi entregue]`.

### Estágio 5: Próximo passo e quem somos (30 s)

- **Contém:** dois ou três próximos passos concretos e quem é a equipe.
- **Próximos passos:** podem citar o que ficou para depois por decisão registrada, como o
  multijogador ([ADR 0006](adr/0006-multijogador-depois-da-primeira-versao.md)), **dito como
  plano**, nunca como algo que já existe.
- **Quem somos:** equipe ASTRIX11, sede Ceres-GO. Nomes só de integrantes maiores de idade que
  concordarem (pendência 13). O integrante menor de 18 anos não é citado por nome
  ([ADR 0007](adr/0007-integrante-menor-por-iniciais.md)); se o grupo citar a equipe por
  iniciais, siga o ADR, e as iniciais não entram neste repositório.
- **Lacunas:** `[próximo passo 1]`, `[próximo passo 2]`, `[frase de fechamento]`.

## 4. Orçamento de palavras

Mesma faixa de fala usada em [`pitch.md`](pitch.md): de 22 a 27 palavras a cada 10 s. **É
estimativa, não medida:** `[VERIFICAR]` lendo em voz alta com cronômetro (seção 9).

| Bloco | Tempo | Palavras faladas (faixa) |
|---|---|---|
| Problema | 40 s | 88 a 108 |
| Solução + Prova | 80 s | 176 a 216, **menos** o tempo em que a demo fala sozinha |
| Diferencial | 30 s | 66 a 81 |
| Próximo passo | 30 s | 66 a 81 |
| **Total** | 3 min | cerca de 400 a 480, menos as pausas da demo |

Regra prática: se a demo tem 30 s sem fala, tire de 66 a 81 palavras do bloco de 80 s. Roteiro
acima da faixa é roteiro que estoura o tempo.

## 5. Roteiro modelo

Preencha as lacunas e cronometre cada bloco. O texto fixo é só costura; reescreva à vontade.

**0:00–0:40 · Problema**

> [Abertura com a situação de quem tem o problema.] [O que essa pessoa precisa fazer e não
> consegue.] [Por que isso importa.] O desafio 13 do NASA Space Apps aponta que [premissa do
> desafio, atribuída].

**0:40–2:00 · Solução e Prova**

> Por isso criamos o [nome do projeto]: [o que o jogo permite, em uma frase].
> Vou mostrar. [Demo: o cenário.] Aqui o jogador decide [decisão]. Vejam o que acontece com
> [consequência]. Esses números vêm de [recurso da NASA], valores de projeto publicados pela NASA.

**2:00–2:30 · Diferencial**

> [Frase do diferencial dentro dos limites da seção 3, estágio 4.]

**2:30–3:00 · Próximo passo e quem somos**

> Os próximos passos são [passo 1] e [passo 2]. Somos a ASTRIX11, de Ceres. [Frase de fechamento.]

## 6. Slides do pitch

São slides próprios do pitch, em português, separados dos 7 slides da submissão (que são em inglês
e têm conteúdo obrigatório: nome do time, integrantes, desafio, imagem do projeto, experiência do
usuário e uso dos dados; [`entrega.md`](entrega.md), "Demo"). Dá para partir dos da submissão e
traduzir.

- **Uma ideia por slide** (dica da palestra): se a banca precisa ler o slide, o slide está fazendo o
  trabalho de quem fala.
- Mapa sugerido, a ajustar pelo grupo:

| Slide | Estágio | Conteúdo |
|---|---|---|
| 1 | Problema | uma imagem ou frase curta da situação |
| 2 | Solução | nome do projeto e uma frase |
| 3 | Prova | a demo ao vivo (ou o vídeo do plano B) |
| 4 | Prova | onde o dado da NASA entra, com a fonte |
| 5 | Diferencial | uma frase |
| 6 | Próximo passo | próximos passos e equipe |

- **Fontes visíveis:** o slide que mostra número da NASA traz a página e a data de acesso, como no
  registro de [`entrega.md`](entrega.md).
- **IA:** imagem ou vídeo gerado por IA leva marca d'água visível ([`entrega.md`](entrega.md), "Uso
  de IA"). Nunca gerar nem alterar marca da NASA (logotipo, bandeira, identificador de missão).
- **Nada de menor de 18 anos:** nome, voz, imagem ou vídeo reconhecível dele não entra em slide.

## 7. Demo ao vivo e plano B

"Internet de evento não é confiável" (palestra). **Grave a demo antes.** O vídeo de 30 s da
submissão, se o grupo escolher esse formato (pendência 10), serve de plano B.

**Checklist técnica**

- [ ] A demo roda sem internet, ou o plano B está baixado na máquina (não só no link).
- [ ] Notebook carregado, com fonte; cabo e adaptador de vídeo testados no projetor da sala
  `[VERIFICAR]` o conector com a organização.
- [ ] Notificações desligadas; abas e janelas abertas só as da demo; zoom legível de longe.
- [ ] Cenário da demo pronto no ponto de partida, sem tela de carregamento nem login.
- [ ] Slides abertos em tela cheia, com uma cópia em PDF em um pendrive.

**Quando a demo falhar** (protocolo da palestra, a partir da Apollo 13):

1. **Respire** 2 segundos.
2. **Diga o que houve**, em uma frase e com calma.
3. **Siga o plano B:** o vídeo gravado, ou as capturas de tela nos slides.

A palestra lembra que a banca também avalia a compostura.

## 8. Quem apresenta

Os papéis são do grupo (pendência 10, "quem conduz").

| Papel | Quem |
|---|---|
| Fala o Problema e o Diferencial | `[integrante]` |
| Opera e narra a demo | `[integrante]` |
| Fala o Próximo passo | `[integrante]` |
| Marca o tempo e aciona o plano B | `[integrante]` |
| Responde as perguntas sobre dados e fontes | `[integrante]` |

- O integrante menor de 18 anos **não aparece em nada que vá para a submissão** ([`entrega.md`](entrega.md)).
  Se ele pode estar no palco no julgamento local, com foto ou gravação da organização, é
  `[VERIFICAR]` com a organização e com o responsável legal (pendências 2 e 3).
- Quem aparecer em vídeo precisa ter dado consentimento por escrito ([`entrega.md`](entrega.md),
  termos sobre imagem).
- Menos trocas de quem fala = menos tempo perdido. Cada troca custa alguns segundos; ensaie as
  passagens.

## 9. O que pode e o que não pode ser dito

A regra completa é a tabela da seção 12.2 de [`problematica.md`](problematica.md). Ao vivo, sob
pressão, estas são as frases que mais escapam:

| Não diga | Diga, se for verdade |
|---|---|
| "O jogo ensina" / "melhora o aprendizado" | "o jogo permite [decisão]"; nada foi medido |
| "Testado com estudantes" / "validado" | só se o grupo testou e registrou como |
| "Aprovado", "apoiado" ou "endossado pela NASA" | "usa [recurso] publicado pela NASA" |
| "Usa dados reais da NASA" | "valores de projeto publicados pela NASA", e só se o número estiver no produto e no registro de fontes |
| "Simulação realista" / "fiel" | dizer qual modelo foi usado e de onde vem |
| "Multijogador" / "colaborativo" | "o próximo passo é o multijogador" (ADR 0006) |
| "Não existe nada parecido" / "o primeiro" | a frase das sete ferramentas lidas, com as ressalvas |
| Qualquer número sem fonte | omita o número |

## 10. Perguntas prováveis da banca

Lista de preparação **derivada dos critérios**, não de perguntas reais da banca. Se houver tempo de
perguntas e quanto dura, é `[VERIFICAR]`. Respostas curtas (até 20 s), dadas por quem conhece o
assunto (seção 8).

| Critério | Pergunta | Resposta do grupo |
|---|---|---|
| Relevância | Onde exatamente o dado da NASA muda o jogo? | `[...]` |
| Relevância | De onde vêm os números, e eles são medidos ou de projeto? | `[...]` |
| Validade | O que funciona hoje e o que ainda é protótipo? | `[...]` |
| Validade | Que modelo calcula as consequências das decisões? | `[...]` |
| Impacto | Para quem é o jogo, e quantas pessoas ele alcança? | `[...]`, sem número sem fonte |
| Criatividade | O que existe parecido, e o que vocês fazem de diferente? | `[...]` |
| Apresentação | Como um jogador sabe por que a missão deu certo ou errado? | `[...]` |
| Próximos passos | O que vocês fariam com mais tempo? | `[...]` |

"Não sabemos ainda; seria o próximo passo" é resposta melhor que um número inventado.

## 11. Ensaio

Dica da palestra: tempo estourado é o erro mais comum e o mais fácil de evitar.

1. Leia o roteiro em voz alta, sem slides, cronometrando cada bloco.
2. Corte até cada bloco caber no tempo da seção 3.
3. Ensaie com slides e demo, na máquina que vai para o palco.
4. Ensaie a falha: no meio da demo, alguém diz "caiu" e o grupo passa ao plano B.
5. Faça um ensaio completo para alguém de fora do grupo e anote o que a pessoa não entendeu.

| Ensaio | Problema (40 s) | Solução + Prova (80 s) | Diferencial (30 s) | Próximo passo (30 s) | Total (3:00) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

## 12. Checklist final

- [ ] Duração, horário, idioma e tempo de perguntas confirmados com a organização.
- [ ] O pitch começa pelo problema, não pela tecnologia.
- [ ] Cada afirmação passa pela seção 9 e pela tabela 12.2 de [`problematica.md`](problematica.md).
- [ ] Todo número tem fonte no registro de [`entrega.md`](entrega.md); sem fonte, saiu.
- [ ] O recurso da NASA citado é o que o jogo de fato usa.
- [ ] Nenhum nome, voz, imagem ou vídeo reconhecível do integrante menor de 18 anos.
- [ ] Nenhum nome de integrante sem acordo, nem o nome do palestrante.
- [ ] Imagem ou vídeo feito com IA tem marca d'água; nenhuma marca da NASA alterada.
- [ ] Plano B gravado e salvo na máquina, testado.
- [ ] Último ensaio dentro de 3:00.

## Onde mais aparece

- One-liner de 10 s: [`pitch.md`](pitch.md).
- Regras da demo, critérios de julgamento, uso de IA e registro de fontes: [`entrega.md`](entrega.md).
- O que o desafio pede e o que os materiais podem afirmar: [`problematica.md`](problematica.md), seção 12.
- Decisões em aberto que afetam o pitch: [`pendencias.md`](pendencias.md), itens 6, 7, 9, 10, 13, 14 e 17.
