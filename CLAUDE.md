# CLAUDE.md — nasa-hackathon

Projeto do Grupo 2 no NASA Space Apps Challenge 2026 (sede Ceres-GO): código, dados de apoio e
material de entrega.

Perfil: GLOBAL (provisório; redefinir quando a stack for escolhida — ver
`C:\dev\docs\padroes\release-e-auditoria.md`)

Complementa o `C:\dev\CLAUDE.md` do workspace. Em conflito, este arquivo prevalece. O workspace
`C:\dev` só existe na máquina do dono do repositório: quem não o tem segue este arquivo e o
`CONTRIBUTING.md`.

## 1. Regras invioláveis

- **Não invente dado, número, regra do evento nem fonte.** Sem fonte, marque `[VERIFICAR]`.
- **Regra do evento vem das páginas oficiais da edição 2026**, não de edição anterior nem de
  memória. O resumo conferido está em `docs/entrega.md`.
- **A ideia da solução é do grupo.** O guia de 2026 diz que a IA não deve ser usada para
  conceber como resolver o desafio: o assistente implementa, revisa e documenta, não escolhe a
  solução.
- **Todo dado ou recurso externo usado** (NASA, agência parceira, outro) entra no registro de
  `docs/entrega.md` com link, licença e data de acesso, no mesmo pull request que passa a
  usá-lo. Material de terceiros precisa ser público ou ter licença de código aberto (OSI).
- **Todo uso de IA** que gere código, dados, texto, imagem, áudio ou vídeo da entrega entra no
  registro de `docs/entrega.md`.
- **Conteúdo gerado por IA é identificado:** marca d'água visível em imagem e vídeo; aviso no
  texto e nos metadados para código, dados e áudio. Nunca gerar nem alterar marca da NASA.
- **Nada de menor de 18 anos na submissão:** nome reconhecível, voz, imagem, vídeo ou outra
  representação. Há integrante menor de 18 anos no grupo: o nome dele não entra em slide,
  página, vídeo, crédito nem em arquivo deste repositório.
- **Sem dado pessoal real** em código, teste, exemplo ou commit. Nome de integrante só entra no
  repositório com o acordo dele.
- **Segredo fora do Git.** `.env*` é ignorado; só `.env.example` é versionado, e completo.
- **A `main` precisa estar sempre demonstrável:** é dela que sai a demo.
- **Não commitar nem enviar (`push`) sem aprovação** de quem opera o assistente.
- **Proibido sem pedido explícito:** `push --force`, `reset --hard`, `clean -fd`, rebase de
  histórico publicado, `--no-verify`.

## 2. Convenções

- Documentação interna e commits em pt-BR. Código (identificadores) em inglês, sem acento.
  A versão de entrega em inglês sai em fork ou repositório novo, não aqui (ADR 0002).
- **Interface do produto e material de entrega em inglês:** página de submissão, slides e tudo
  o que os links da submissão abrem. Só o vídeo pode ser falado em português, com legenda em
  inglês (`docs/entrega.md`).
- Conventional Commits em pt-BR, com escopo, terminando com a linha `Co-Authored-By` do
  assistente quando houver.
- Branch curta + pull request para a `main` (`CONTRIBUTING.md`, ADR 0001).
- Datas: ISO 8601 nos dados, `dd/mm/aaaa` nos documentos.
- Gerenciador de pacotes: a definir com a stack.

## 3. Estrutura

```text
README.md  CONTRIBUTING.md  CHANGELOG.md  CLAUDE.md  LICENSE
.github/pull_request_template.md
docs/README.md      índice
docs/desafios/      um documento por desafio (14) e o comparativo
docs/desafio.md     critérios do grupo e desafio escolhido
docs/entrega.md     requisitos da submissão, fontes de dados, uso de IA
docs/problematica.md  problemática do desafio escolhido, com fontes e perguntas de decisão
docs/pendencias.md  decisões em aberto
docs/adr/           registros de decisão
```

## 4. Comandos

Nenhum ainda: não há código. Quando houver, os comandos de instalação, execução e do portão
(typecheck, lint, test, build — o que a stack tiver) ficam no `README.md`, e o portão vira
pré-condição de merge.

## 5. Estado (substitua a linha, não acumule)

- 14/11/2026: repositório privado `VolatusLab/nasa-hackathon` (renomeado de `nasa-hackaton`
  nessa data), branch `main`, sem proteção de branch; só documentação.
- 14/11/2026: desafio 13, Space Mission Design Game, escolhido (ADR 0004), com multijogador para até quatro pessoas na primeira versão e uso de recursos da NASA; equipe ASTRIX11; stack não definida; sem CI; licença Apache 2.0 (ADR 0003).
- 14/11/2026: os outros quatro integrantes ainda não foram convidados como colaboradores.
- Prazo de submissão: 15/11/2026, 23h59, horário do evento local (`docs/entrega.md`).

## 6. Armadilhas já pagas

- `www.spaceappschallenge.org` falha com erro de cadeia de certificado (raiz não confiável) no
  `curl` e no WebFetch da máquina do dono do repositório (14/11/2026). Não contorne com `-k`:
  leia a página pelo Chrome, que abre normalmente.

## 6b. Segurança

- Ainda não há autenticação, API nem dado sensível. Ao introduzir qualquer um deles, redefina o
  perfil e siga `C:\dev\docs\padroes\seguranca-aplicacao.md`.
- Exceções aceitas ao perfil: nenhuma por ora. O perfil GLOBAL pede portão no CI: o primeiro
  código sem CI exige ADR ou a pendência de CI resolvida.

## 7. Onde está cada coisa

| Vai mexer em… | Leia antes |
|---|---|
| escolha ou escopo do desafio | `docs/desafios/README.md` (comparativo), `docs/desafio.md` (decisão) |
| página de submissão, demo, slides, licença | `docs/entrega.md`, `docs/adr/0003-licenca-apache-2-0.md` |
| versão de entrega em inglês | `docs/adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md` |
| dado da NASA ou de agência parceira | `docs/entrega.md` (registro de fontes) |
| fluxo de branch, commit e PR | `CONTRIBUTING.md`, `docs/adr/0001-fluxo-de-git-branch-curta-e-pr.md` |
| algo ainda não decidido | `docs/pendencias.md` |
| decisão nova com alternativas | `docs/adr/README.md` (modelo) |
