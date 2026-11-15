# 0006 — Multijogador fica para depois da primeira versão

- **Data:** 14/11/2026
- **Situação:** aceita (substitui a parte do ADR 0004 que incluía o multijogador na primeira versão)

## Contexto

O ADR 0004 decidiu, em 14/11/2026, incluir o modo multijogador para até quatro pessoas já na
primeira versão. O prazo de submissão é 15/11/2026, 23h59 ([`../entrega.md`](../entrega.md)). Até
esta data não há código, stack nem protótipo. O enunciado pede um jogo interativo e trata o modo
em equipe como opcional: "You may consider enabling a player to participate individually or
collaborate with a team of up to four people"
([`../desafios/13-enunciado-completo.md`](../desafios/13-enunciado-completo.md), seção "Objetivos").

## Decisão

O multijogador para até quatro pessoas fica para depois da primeira versão. A primeira versão
será definida sem ele.

## Alternativas consideradas

- **Manter o multijogador na primeira versão:** não cabe no prazo, porque exige servidor,
  sincronização e papéis por jogador, e não há código iniciado.
- Outras formas de multijogador não foram avaliadas pelo grupo.

## Consequências

- As considerações opcionais de colaboração do enunciado ficam fora da primeira versão.
- A versão em inglês e a página do projeto precisam descrever apenas o que for entregue.
- Se o multijogador voltar, a parte técnica (servidor, persistência e autenticação) muda o perfil
  de segurança do projeto, conforme o `CLAUDE.md` §6b.

## Revisitar quando

- A primeira versão estiver demonstrável sem o multijogador, e ainda houver tempo antes do prazo.
- O grupo decidir um prazo posterior à submissão para a versão completa.

## Atualizações

- 14/11/2026, revisão do texto, sem mudar a decisão. O Contexto dizia: 'O enunciado diz que a
  solução "pode" incluir jogo funcional, e não exige multijogador'. Foi corrigido, porque o
  enunciado pede um jogo interativo e o que é opcional é o modo em equipe. Em Alternativas, saiu o
  item "Multijogador simulado ou por revezamento", que não veio do grupo. Em Consequências,
  "critério de colaboração" virou "considerações opcionais de colaboração".
