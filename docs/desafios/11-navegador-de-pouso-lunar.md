# 11 — Lunar Landing Site Navigator

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/lunar-landing-site-navigator/>
  (lida em 14/11/2026)
- **Nível:** intermediário, avançado
- **Temas:** exploração humana, Lua, software, exploração espacial

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Criar uma ferramenta intuitiva para comparar rapidamente locais e datas de pouso na Lua,
mostrando a posição do Sol e da Terra em relação ao horizonte para avaliar geração de energia e
janelas de comunicação direta com a Terra.

## Contexto

O programa CLPS da NASA e outras missões lunares dependem da escolha de local e data de pouso.
Duas coisas pesam:

- a **posição do Sol** define a energia disponível para os painéis e as condições térmicas;
- a **posição da Terra** define se há comunicação direta, sem satélite de retransmissão.

No **polo sul lunar**, onde muitas missões são planejadas por causa do gelo de água, a geometria
cria variações extremas de iluminação e de visibilidade da Terra. Mudanças pequenas de local ou
data alteram muito a energia e as janelas de comunicação.

Cronogramas mudam: atrasos de hardware ou de lançamento obrigam a reavaliar local e data, e os
engenheiros precisam comparar alternativas depressa. As ferramentas que existem (Quickmap, Moon
Trek, JPL Horizons) servem à análise detalhada e são difíceis para comparação rápida por quem
não é especialista: é preciso passar por várias interfaces e interpretar dado bruto.

## O que é pedido

Uma ferramenta ou aplicação para avaliação rápida de opções de pouso lunar. Exibir a posição
do Sol e da Terra em relação ao horizonte é o núcleo do desafio; os demais itens são
possibilidades:

- **Seleção e comparação de locais:** lista de locais notáveis (missões Apollo, alvos futuros do
  CLPS, missões comerciais, programas de outros países) e entrada de coordenadas próprias;
  comparação lado a lado ou em sequência.
- **Data e hora flexíveis:** escolher data e hora e explorar a variação ao longo de dias e
  estações lunares.
- **Posição do Sol e da Terra** em relação ao horizonte no local e na data; tempo restante até
  o pôr do Sol ou da Terra.
- **Avaliação de energia e comunicação:** ângulo de elevação solar, duração da luz, janelas de
  visibilidade da Terra.
- **Várias formas de visualizar:** mapa 2D, superfície 3D, outras.
- **Dinâmica no tempo:** animação ou linha do tempo ao longo de um dia lunar ou de vários dias.
- **Vários níveis de usuário:** do planejador de missão ao educador e ao público.

Formato aberto: aplicação web, app de celular, visualização interativa, jogo educativo.

## O que o enunciado sugere considerar

**Abordagem técnica**

- Efemérides (posição e movimento dos corpos celestes) podem ser calculadas com o JPL Horizons
  ou vir de conjuntos pré-calculados.
- Topografia lunar do LOLA ajuda em visualização realista e cálculo correto do horizonte.
- A Lua não tem atmosfera: sem refração, o horizonte é definido pelo terreno local e pela borda
  da esfera lunar.
- O ângulo de elevação solar é a métrica-chave de energia e merece destaque.

**Experiência de uso**

- Priorizar a comparação rápida de combinações de local e data.
- Comunicar com clareza o tempo que falta para o pôr do Sol ou da Terra.
- Tornar visíveis as diferenças entre a Lua e a Terra.
- Ajudar o usuário a entender por que mudanças pequenas têm impacto grande.

**Dados e precisão**

- Considerar a topografia real: a elevação do terreno altera horizonte e janelas.
- Decidir se a ferramenta trata a libração da Terra e as variações da órbita lunar.
- O terreno do polo sul é complexo: encostas íngremes e crateras profundas criam sombra extrema.

## Dados e recursos indicados

### NASA

| Recurso | O que oferece |
|---|---|
| [Quickmap](https://quickmap.lroc.asu.edu/) | mapa interativo com imagens de alta resolução, topografia e outros dados do Lunar Reconnaissance Orbiter |
| [Moon Trek](https://trek.nasa.gov/moon/) | visualização 3D interativa da superfície lunar, com topografia |
| [JPL Horizons](https://ssd.jpl.nasa.gov/horizons/) | cálculo de efemérides: posição do Sol e da Terra vistos de qualquer ponto da Lua, em qualquer momento |

### Agências parceiras

| Recurso | O que oferece |
|---|---|
| [Exploração da Lua (CSA)](https://www.asc-csa.gc.ca/eng/astronomy/moon-exploration/) | missões passadas, atuais e futuras, e a participação canadense no programa Artemis |

## Para a escolha do grupo

- **Público declarado:** planejadores de missão, educadores e público.
- **Entrega esperada:** ferramenta de comparação com visualização.
- **Natureza dos dados:** posições calculadas (ângulos no tempo) e, opcionalmente, topografia.
  O JPL Horizons entrega as posições; não é imagem nem acervo volumoso.
- **Onde está a dificuldade** (leitura de quem resumiu): a geometria. Converter efemérides em
  "acima ou abaixo do horizonte" para um ponto da Lua, e fazer isso certo, é o que sustenta o
  critério "Validade". Incluir o terreno real aumenta bastante o trabalho; o enunciado o trata
  como consideração, não como exigência.
- **Escopo bem delimitado:** entradas (local, data) e saídas (posições, métricas) estão
  descritas com clareza.
- **Perguntas para o grupo responder antes de escolher:**
  - Conseguimos obter do Horizons a posição do Sol e da Terra para um ponto da Lua ainda hoje?
  - A primeira versão considera o terreno ou só a esfera lunar?
  - Quantos locais e que intervalo de datas cabem no prazo?
  - Alguém do grupo se sente à vontade com trigonometria e sistemas de coordenadas?
