# 03 — Build a Junior Astronaut Mission Trainer

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/junior-astronaut-mission-trainer/>
  (lida em 14/11/2026)
- **Nível:** iniciante/jovem, intermediário
- **Temas:** jogos, planetas e luas, software, exploração espacial, Sol

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Construir um jogo ou app interativo em que crianças de 7 a 12 anos administram uma base na Lua
ou em Marte e sentem, nas próprias decisões, as trocas que definem o sucesso de uma missão.

## Contexto

Manter gente viva na Lua ou em Marte exige equilibrar demandas que competem: a energia limitada
se divide entre suporte à vida, comunicação e ciência; a exposição à radiação é pesada contra os
objetivos; cada decisão tem um custo que se acumula. Os planejadores da NASA lidam com isso
usando dados reais.

O conteúdo educativo para crianças costuma falhar por um dos lados: ou é abstrato demais
(cartazes, fatos gerais), ou técnico demais. Conteúdo só educativo perde a atenção; conteúdo só
de entretenimento perde a precisão.

## O que é pedido

Um jogo ou app em que a criança toma decisões reais sobre **suporte à vida, blindagem contra
radiação, orçamento de energia, produção de comida e atraso de comunicação**, e vê as
consequências ao longo de uma missão simulada.

- O objetivo é um **protótipo que funcione** e mostre a mecânica de troca com clareza: a
  criança sai entendendo uma restrição real, não só tendo jogado algo divertido.
- Formato aberto: navegador, celular ou desktop. Exemplos citados: jogo de sobrevivência com
  gestão de recursos, simulador narrativo de decisões, painel estilo controle de missão.
- Interpretações criativas de "base" ou "missão" além da Lua e de Marte são aceitas, desde que
  o objetivo educativo continue no centro.
- O enunciado incentiva o uso de **dados abertos reais da NASA** em vez de números inventados.
  Fontes que ele nomeia: clima espacial (DONKI), saúde e radiação de astronautas (OSDR) e dados
  ambientais das missões Artemis e de superfície de Marte.

## O que o enunciado sugere considerar

**Público e acessibilidade**

- Alvo de 7 a 12 anos; pode servir também a irmãos mais velhos, pais e sala de aula.
- Linguagem simples; termo científico inevitável é explicado no contexto.
- Barreira baixa: jogar no navegador, sem download nem cadastro, alcança mais gente inclusive
  no julgamento.

**Dados reais**

- Mesmo pouco dado real (uma leitura de radiação, uma foto de Marte) dá mais credibilidade do
  que uma simulação inteira inventada.
- Citar as fontes **dentro da ferramenta**.
- Se chamada de API ao vivo não couber no prazo, um conjunto real embutido é alternativa
  honesta, desde que dado estático não seja apresentado como ao vivo.

**Armadilhas apontadas**

- Não criar uma escolha "segura" sem custo: o valor educativo vem de toda decisão ter troca.
- Polimento visual não substitui precisão da mecânica: jogo simples que ensina uma restrição
  real vale mais que um bonito que não ensina.
- Não sobrecarregar: dois ou três recursos centrais costumam funcionar melhor que cinco ou seis.

**O que destacaria uma solução**

- Ligar a escolha do jogo a uma consequência do mundo real (por exemplo, dados atuais de clima
  espacial).
- Rejogabilidade: eventos que variam a cada partida.
- Acompanhar o protótipo de uma explicação curta de quais dados da NASA foram usados e por quê.

## Dados e recursos indicados

### NASA

| Recurso | O que oferece |
|---|---|
| [NASA Open APIs](https://api.nasa.gov/) | portal de APIs públicas (foto astronômica do dia, fotos dos rovers de Marte, DONKI); chave gratuita na hora |
| [DONKI](https://ccmc.gsfc.nasa.gov/tools/DONKI/) | dados atualizados de erupções solares, ejeções de massa coronal e outros eventos de clima espacial |
| [OSDR](https://osdr.nasa.gov/bio/repo/) | acervo de biologia espacial e saúde de astronautas, pesquisável por palavra-chave ([API de busca](https://osdr.nasa.gov/osdr/data/search?term=KEYWORD)) |
| [RadLab](https://visualization.osdr.nasa.gov/radlab/gui/data-api/) | medições reais de dose de radiação a bordo da Estação Espacial Internacional |
| [Mars Trek](https://trek.nasa.gov/mars/) | imagens, elevação e terreno reais de Marte, com download |

### Agências parceiras

| Recurso | O que oferece |
|---|---|
| [Recursos de espaço para educação (CSA)](https://www.asc-csa.gc.ca/eng/youth-educators/resources-stem-and-youth-organizations.asp) | ferramentas e atividades gratuitas para engajar jovens |
| [Produção de comida na Lua e em áreas remotas (CSA)](https://www.asc-csa.gc.ca/eng/youth-educators/toolkits/food-production/) | material sobre comida no espaço, saúde e nutrição de astronautas |

## Para a escolha do grupo

- **Público declarado:** crianças de 7 a 12 anos.
- **Entrega esperada:** protótipo jogável.
- **Natureza dos dados:** APIs públicas simples, com chave gratuita; dá para embutir um conjunto
  real se a API ao vivo não couber.
- **Onde está a dificuldade** (leitura de quem resumiu): o enunciado é o mais detalhado sobre o
  que os jurados valorizam, e isso é desenho de jogo: toda escolha com custo, poucos recursos,
  precisão acima de visual. A parte técnica de dados é leve.
- **Semelhança com outro desafio:** o [13](13-jogo-de-projeto-de-missao.md) também pede um jogo,
  mas sobre projetar a missão inteira, não sobre operar a base.
- **Perguntas para o grupo responder antes de escolher:**
  - Quais dois ou três recursos entram na mecânica?
  - Conseguimos testar com uma criança da faixa etária antes do prazo?
  - O jogo roda no navegador, sem instalação?
  - Lembrete do evento: nenhum nome reconhecível, imagem, vídeo ou voz de menor de 18 anos na
    submissão, o que inclui gravação de teste com crianças.
