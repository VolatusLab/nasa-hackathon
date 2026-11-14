# 12 — Planet X and SPHEREx

- **Página oficial:** <https://www.spaceappschallenge.org/2026/challenges/planet-x-and-spherex/>
  (lida em 14/11/2026)
- **Nível:** avançado
- **Temas:** astrofísica, planetas e luas, software

Resumo em português feito a partir da página oficial. Para o enunciado completo, vale o original.

## Em uma frase

Criar uma ferramenta web pública que exibe imagens do céu da missão SPHEREx para uma coordenada
informada e mostra, como um pequeno vídeo, como aquele trecho muda ao longo do tempo.

## Contexto

Asteroides e cometas orbitam o Sol; estrelas próximas se deslocam no céu; a própria Terra se
move. Observar esses deslocamentos entre imagens tiradas em momentos diferentes revela objetos
novos e ajuda a medir distâncias. Plutão foi descoberto assim.

Buscas recentes com voluntários, por essa técnica, descobriram asteroides, cometas, estrelas e
anãs marrons. A maioria dos cometas e anãs marrons conhecidos foi achada por voluntários em
projetos como o [Backyard Worlds](http://backyardworlds.org/).

Desde maio de 2025, a missão SPHEREx mapeia o céu inteiro a cada seis meses, em **102 bandas**
do infravermelho próximo, o que a torna sensível a objetos ricos em hidrogênio, água, dióxido e
monóxido de carbono e outras moléculas. São imagens de mais de um bilhão de objetos, muitas
vezes sobrepostos ou de brilho variável: dado demais para uma pessoa ou um só programa.

## O que é pedido

Uma **ferramenta web aberta ao público** em que:

1. o usuário informa as coordenadas de um trecho do céu (ascensão reta e declinação);
2. a ferramenta mostra uma série de imagens daquele trecho em sequência, como um vídeo curto,
   para facilitar a identificação de objetos em movimento.

**Alvos de teste indicados pelo enunciado:**

- Estrela de Barnard;
- Epsilon Indi B (par de anãs marrons orbitando uma estrela);
- WISE 0855, anã marrom de movimento rápido (ascensão reta 08h55m10.831s, declinação
  -7d14m42.53s);
- as estrelas variáveis RW Aurigae e R Draconis.

## O que o enunciado sugere considerar

- Os dados chegam rápido: a ferramenta precisa ser **fácil de atualizar** com novas liberações.
- Pensar em como exibir as 102 bandas. Exemplo dado: somar separadamente os dados de cada um
  dos seis conjuntos de detectores para melhorar a relação sinal-ruído. Ponto extra se a
  ferramenta gerar espectros na hora.
- Opção de **somar ou subtrair** imagens de momentos diferentes.
- Deixar o usuário escolher o **campo de visão**: campo maior acompanha fontes mais rápidas, ao
  custo de transferência mais demorada.
- Sobrepor dados de outros telescópios, como as missões Gaia e WISE.
- Permitir consulta por coordenadas **na URL**, para incorporar a ferramenta em outros sites.
- Exibir metadados, como marcações de contaminação.
- Procurar ferramentas públicas para dados astronômicos: Astropy (o enunciado grafa "Astrophy")
  para tratar os dados e o Aladin, do centro de dados de Estrasburgo (CDS), para exibi-los.

## Dados e recursos indicados

### NASA

| Recurso | O que oferece |
|---|---|
| [NASA/IPAC Infrared Science Archive: SPHEREx](https://irsa.ipac.caltech.edu/Missions/spherex.html) | os recursos e dados da missão |
| [Notebooks de tutorial do SPHEREx](https://caltech-ipac.github.io/irsa-tutorials/spherex/) | exemplos em Jupyter de como acessar os dados com Python |
| [WiseView](http://byw.tools/wiseview) | ferramenta parecida, feita para a missão WISE, já usada pelo público em centenas de descobertas; indicada como modelo |
| [Dados da missão Gaia](https://archive.stsci.edu/missions-and-data/gaia) | usar a liberação mais recente (Data Release 3) |

### Agências parceiras

| Recurso | O que oferece |
|---|---|
| [NEOSSat (CSA)](https://www.asc-csa.gc.ca/eng/satellites/neossat/) | telescópio espacial canadense dedicado a asteroides, cometas, satélites e detritos |
| [Canadian Astronomy Data Centre](https://www.cadc-ccda.hia-iha.nrc-cnrc.gc.ca/en/) | acervo de observações de telescópios e missões canadenses e internacionais |
| [Tutorial de dados do NEOSSat](https://github.com/asc-csa/NEOSSAT_Tutorial) | passo a passo em Python |
| [Conjunto de dados do NEOSSat](https://data.asc-csa.gc.ca/dataset/neossat) | observações do telescópio |

## Para a escolha do grupo

- **Público declarado:** qualquer pessoa; cientistas cidadãos.
- **Entrega esperada:** ferramenta web pública.
- **Dado obrigatório:** imagens do SPHEREx.
- **Natureza dos dados:** imagens astronômicas em formato próprio da área, acessadas por
  consulta ao arquivo; há tutoriais em Python.
- **Onde está a dificuldade** (leitura de quem resumiu): só este e o
  [02](02-detetive-de-tendencias.md) são marcados apenas como avançados. Exige lidar com
  coordenadas celestes, recorte de imagens por posição e 102 bandas, e servir tudo isso pela
  web com tempo de resposta aceitável.
- **Especificação precisa:** entrada, saída e alvos de teste estão definidos, e existe uma
  ferramenta de referência (WiseView). Dá para saber objetivamente se funciona.
- **Perguntas para o grupo responder antes de escolher:**
  - Conseguimos rodar um dos notebooks de tutorial e obter uma imagem ainda hoje?
  - Quanto tempo leva buscar as imagens de um alvo? Dá para fazer sob demanda ou precisa de
    armazenamento prévio?
  - Onde a ferramenta fica hospedada, com link público, para o julgamento?
  - Alguém do grupo já trabalhou com dados astronômicos?
