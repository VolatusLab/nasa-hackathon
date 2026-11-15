# 0005 — Recursos da NASA usados na primeira versão

- **Data:** 14/11/2026
- **Situação:** aceita

## Contexto

O critério "Relevância" do julgamento pede que o dado da NASA seja parte central, não enfeite
([`../entrega.md`](../entrega.md)). A aba Recursos do desafio lista nove recursos
([`../desafios/13-jogo-de-projeto-de-missao.md`](../desafios/13-jogo-de-projeto-de-missao.md)). A
análise de 14/11/2026 verificou o conteúdo de cada um e as licenças. Os números de referência
precisam de data, e a licença de algumas fontes não foi confirmada.

## Decisão

O grupo aprovou, em 14/11/2026, a seguinte lista para a primeira versão:

1. **Números de projeto de missões reais** dos kits de imprensa do JPL para NISAR e Europa Clipper,
   usados como valores de referência para massa, potência e taxa de dados. Cada valor leva a data e
   a nota de fase (lançamento previsto ou já realizado).
2. **NASA Mission Viz**, apenas como link. O código não é copiado e não é incorporado enquanto a
   licença não for confirmada com a NASA.
3. **Jogo do Webb**, apenas como link, como referência de design.

Ficam de fora na primeira versão: o GMAT, por custo de integração, e o Mission Design Lab, por
acesso restrito a formulário.

## Alternativas consideradas

- **GMAT como fonte de cálculo:** dá números de trajetória, mas a integração não cabe no prazo da
  primeira versão.
- **Mission Viz incorporado:** a licença do repositório não foi confirmada, e o arquivo de
  ontologia diz que o uso comercial exige negociação.
- **Mission Design Lab:** o serviço só é acessado por formulário, e a página informa que não é
  atualizada.

## Consequências

- Os números dos kits de imprensa são de projeto ou previstos. Cada uso cita a página e a data de
  acesso, e não apresenta o valor como medido.
- A licença do Mission Viz e os termos de reuso dos números precisam de confirmação com a NASA. Até
  lá, o uso é só por link. Essa pendência está no item 7 de [`../pendencias.md`](../pendencias.md).
- A decisão não altera o multijogador, que foi adiado pelo ADR 0006
  diante do prazo.
- Conferência de 14/11/2026 nas páginas baixadas: a do NISAR traz massa, potência e taxa de dados;
  a do Europa Clipper traz a massa e as dimensões dos painéis solares, **sem potência em watts nem
  taxa de dados**. Para esses dois valores do Europa Clipper é preciso outra fonte da NASA, ou
  deixá-los de fora. Os valores lidos estão no registro de fontes de
  [`../entrega.md`](../entrega.md).

## Revisitar quando

- A NASA confirmar a licença do Mission Viz, e o grupo quiser incorporá-lo.
- O grupo decidir usar o GMAT, depois da primeira versão.
- Os kits de imprensa forem substituídos por dados oficiais com licença clara.

## Atualizações

- 14/11/2026: a consequência sobre o multijogador dizia "continua registrado no ADR 0004 e
  pendente de revisão diante do prazo". Foi atualizada quando o ADR 0006 o adiou.
- 14/11/2026, revisão: acrescentada a conferência dos números nas páginas baixadas. A decisão não
  mudou.
- 14/11/2026, revisão: duas descrições deste ADR são imprecisas. O Mission Design Lab é um serviço
  de estudo de conceito do Goddard para clientes, não uma ferramenta nem um conjunto de dados; o
  formulário citado é o de parceria com o Goddard. O aviso da página é "Due to the lapse in federal
  government funding, NASA is not updating this website", e o rodapé diz que ela foi atualizada em
  23/07/2026. A frase sobre uso comercial está em uma ontologia de terceiro dentro do repositório
  do Mission Viz, e vale para essa ontologia. Os motivos para deixar os dois de fora continuam.
