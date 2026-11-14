# 0006 — Multijogador fica para depois da primeira versão

- **Data:** 14/11/2026
- **Situação:** aceita (substitui a parte do ADR 0004 que incluía o multijogador na primeira versão)

## Contexto

O ADR 0004 decidiu, em 14/11/2026, incluir o modo multijogador para até quatro pessoas já na
primeira versão. O prazo de submissão é 15/11/2026, 23h59 ([`../entrega.md`](../entrega.md)). Até
esta data não há código, stack nem protótipo. O enunciado diz que a solução "pode" incluir jogo
funcional, e não exige multijogador ([`../desafios/13-enunciado-completo.md`](../desafios/13-enunciado-completo.md)).

## Decisão

O multijogador para até quatro pessoas fica para depois da primeira versão. A primeira versão
será definida sem ele.

## Alternativas consideradas

- **Manter o multijogador na primeira versão:** não cabe no prazo, porque exige servidor,
  sincronização e papéis por jogador, e não há código iniciado.
- **Multijogador simulado ou por revezamento:** não foi avaliado pelo grupo. Qualquer forma dessa
  decisão exige nova decisão registrada.

## Consequências

- O critério de colaboração do enunciado fica menos atendido na primeira versão.
- A versão em inglês e a página do projeto precisam descrever apenas o que for entregue.
- Se o multijogador voltar, a parte técnica (servidor, persistência e autenticação) muda o perfil
  de segurança do projeto, conforme o `CLAUDE.md` §6b.

## Revisitar quando

- A primeira versão estiver demonstrável sem o multijogador, e ainda houver tempo de escopo.
- O grupo decidir um prazo posterior à submissão para a versão completa.
