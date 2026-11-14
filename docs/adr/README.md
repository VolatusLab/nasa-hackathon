# Registros de decisão (ADR)

Um ADR registra uma escolha que alguém pode querer desfazer depois sem saber por que foi feita:
desafio, stack, arquitetura, fluxo de Git, licença.

- Arquivo `NNNN-slug.md`, numeração sequencial.
- **Só cresce:** decisão superada ganha `Situação: substituída por NNNN` e não é apagada.

| Nº | Decisão | Situação |
|---|---|---|
| [0001](0001-fluxo-de-git-branch-curta-e-pr.md) | Fluxo de Git: branch curta e pull request | aceita |
| [0002](0002-documentacao-em-pt-br-e-entrega-em-ingles.md) | Documentação em pt-BR; entrega em inglês em fork ou repositório novo | aceita |
| [0003](0003-licenca-apache-2-0.md) | Licença Apache 2.0 | aceita |
| [0004](0004-desafio-13-jogo-de-projeto-de-missao.md) | Desafio 13: Space Mission Design Game | aceita |

## Modelo

```markdown
# NNNN — <título da decisão>

- **Data:** dd/mm/aaaa
- **Situação:** aceita | substituída por NNNN | rejeitada

## Contexto
<O problema e as restrições.>

## Decisão
<O que foi decidido, em uma ou duas frases.>

## Alternativas consideradas
<E por que perderam.>

## Consequências
<O que fica mais fácil, o que fica mais difícil, o risco aceito.>

## Revisitar quando
<Gatilho objetivo para reabrir a decisão.>
```
