# 0003 — Licença Apache 2.0

- **Data:** 14/11/2026
- **Situação:** aceita

## Contexto

Os termos do evento exigem que o conteúdo original submetido fique disponível sem restrição ou
sob licença de código aberto reconhecida pela Open Source Initiative (OSI). Se o time não
indicar uma licença, a NASA distribui o conteúdo sob Apache 2.0
([`../entrega.md`](../entrega.md)). O dono do repositório decidiu por licença aberta em
14/11/2026, sem indicar qual.

## Decisão

O projeto adota a Apache License 2.0. O texto está no arquivo `LICENSE`, na raiz.

## Alternativas consideradas

- **MIT ou BSD.** São mais curtas e igualmente aceitas pela OSI. Perderam porque a Apache 2.0 é
  a licença que o evento já aplicaria na falta de escolha: adotá-la explicitamente não muda o
  resultado e evita divergência entre o que o repositório diz e o que a NASA publica.
- **Não escolher.** O efeito prático seria o mesmo, mas o repositório ficaria sem arquivo
  `LICENSE`, o que confunde quem chega.

A escolha da Apache 2.0 entre as licenças abertas foi de quem redigiu este registro; o grupo
pode trocá-la por outra licença OSI.

## Consequências

- Qualquer pessoa pode usar, modificar e redistribuir o código, mantendo o aviso de licença.
- A licença vale para o conteúdo original do grupo. Material de terceiros mantém a própria
  licença, que precisa ser compatível e constar no registro de fontes.
- O repositório de entrega em inglês (ADR 0002) leva o mesmo arquivo `LICENSE`.

## Revisitar quando

- O grupo preferir outra licença OSI, antes da submissão.
- Entrar no projeto uma dependência com licença incompatível com a Apache 2.0.
