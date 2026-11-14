# 0001 — Fluxo de Git: branch curta e pull request

- **Data:** 14/11/2026
- **Situação:** aceita

## Contexto

Cinco pessoas vão trabalhar no mesmo repositório ao mesmo tempo, com prazo curto e níveis de
experiência diferentes. A `main` é a versão que será demonstrada na entrega: se ela quebrar perto
do prazo, o grupo fica sem demo. Ainda não há CI nem testes que barrem um erro automaticamente.

Decidido pelo dono do repositório em 14/11/2026 e confirmado por ele em 15/11/2026, antes da
entrada dos demais integrantes. A `main` não está protegida no GitHub, então a regra vale por
acordo.

## Decisão

Cada mudança nasce em uma branch curta e entra na `main` por pull request aprovado por um
colega. Correção trivial de documentação pode ir direto na `main`.

## Alternativas consideradas

- **Todos enviam direto para a `main`.** É o mais rápido, mas um envio ruim quebra a demo de
  todos e ninguém mais viu a mudança antes de ela entrar.
- **Uma branch longa por pessoa, juntando tudo no fim.** Adia os conflitos para o pior momento,
  perto do prazo.
- **Branch `develop` além da `main`.** Dá uma etapa a mais de integração que um projeto de
  poucos dias não aproveita.

## Consequências

- Toda mudança é vista por duas pessoas, o que também espalha o conhecimento do código no grupo.
- A revisão pode virar fila se só uma pessoa revisar. Qualquer integrante pode aprovar.
- Sem CI, a aprovação depende de o autor ter rodado o projeto na própria máquina.

## Revisitar quando

- A revisão atrasar a entrega nas últimas horas antes do prazo: o grupo pode combinar envio
  direto para a `main` nesse trecho.
- Houver CI com o portão do projeto: a aprovação passa a exigir CI verde.
