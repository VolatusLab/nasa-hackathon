# nasa-hackathon

Projeto do **Grupo 2** no **NASA Space Apps Challenge 2026**, sede **Ceres-GO**.

> **Prazo de submissão: domingo, 15/11/2026, 23h59** (horário do evento local).
> O que falta decidir, em ordem de urgência: [`docs/pendencias.md`](docs/pendencias.md).

## O que é

O Space Apps é um hackathon global da NASA: cada equipe escolhe um dos desafios oficiais e
entrega uma solução. Usar ao menos um dado ou recurso da NASA é condição para prêmio global;
dados de agências parceiras são incentivados. Aqui ficam o código, os dados de apoio e o
material de entrega do Grupo 2.

- Os 14 desafios de 2026, resumidos e comparados: [`docs/desafios/`](docs/desafios/README.md)
- Desafio escolhido e por quê: [`docs/desafio.md`](docs/desafio.md)
- O que a entrega exige e o que já está pronto: [`docs/entrega.md`](docs/entrega.md)

## Equipe

Equipe **ASTRIX11**, Grupo 2, com cinco integrantes. Os nomes dos integrantes maiores de idade
entram aqui com o acordo de cada um (ver [`docs/pendencias.md`](docs/pendencias.md)).

Desafio: **13 — Space Mission Design Game** ([ADR 0004](docs/adr/0004-desafio-13-jogo-de-projeto-de-missao.md)).

## Como começar

1. Aceite o convite do GitHub para o repositório. Ele é privado, e o convite é enviado pelo dono
   da conta `VolatusLab`.
2. Clone: `git clone https://github.com/VolatusLab/nasa-hackathon.git`
3. Leia o [`CONTRIBUTING.md`](CONTRIBUTING.md) antes do primeiro commit.
4. Enquanto o desafio não estiver escolhido, leia o comparativo em
   [`docs/desafios/README.md`](docs/desafios/README.md) e leve seus candidatos ao grupo.

Ainda não há o que instalar nem rodar. Quando a stack for escolhida, os comandos de instalação,
execução e teste entram nesta seção.

## Estrutura

```text
nasa-hackathon/
├── README.md            visão geral (este arquivo)
├── CONTRIBUTING.md      como trabalhar no repositório
├── CHANGELOG.md         o que mudou e quando
├── CLAUDE.md            regras para assistentes de código
├── LICENSE              Apache License 2.0
├── .github/             modelo de pull request
└── docs/
    ├── README.md        índice da documentação
    ├── desafios/        um documento por desafio (14) e o comparativo
    ├── desafio.md       critérios do grupo e desafio escolhido
    ├── entrega.md       requisitos da submissão, fontes de dados e uso de IA
    ├── pendencias.md    decisões em aberto
    └── adr/             registros de decisão
```

## Documentação

O índice completo está em [`docs/README.md`](docs/README.md).

A documentação deste repositório é em pt-BR. A versão de entrega em inglês, exigida pelo evento,
sai em fork ou repositório novo
([ADR 0002](docs/adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md)).

## Licença

[Apache License 2.0](LICENSE). Os termos do evento exigem licença de código aberto para o
conteúdo submetido; o motivo da escolha está no
[ADR 0003](docs/adr/0003-licenca-apache-2-0.md).
