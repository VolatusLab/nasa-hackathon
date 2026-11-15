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
  página, vídeo, crédito nem em arquivo deste repositório. Nos materiais de entrega ele aparece
  só por iniciais, e as iniciais também não entram em arquivo deste repositório (ADR 0007).
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
docs/pitch.md       modelo do pitch de 10 segundos
docs/pitch-final.md guia do pitch final de 3 minutos para a banca local
docs/pendencias.md  decisões em aberto
docs/adr/           registros de decisão
assets/             texto e impressões das páginas oficiais e material do evento local (terceiros; não
                    vai para a versão pública de entrega)
data/raw/           arquivos-fonte baixados, fora do Git; só o MANIFEST.tsv é versionado (URL,
                    hash e data de cada arquivo)
```

## 4. Comandos

Nenhum ainda: não há código. Quando houver, os comandos de instalação, execução e do portão
(typecheck, lint, test, build — o que a stack tiver) ficam no `README.md`, e o portão vira
pré-condição de merge.

## 5. Estado (substitua a linha, não acumule)

- 14/11/2026: repositório privado `VolatusLab/nasa-hackathon` (renomeado de `nasa-hackaton`
  nessa data), branch `main`, sem proteção de branch; só documentação.
- 14/11/2026: desafio 13, Space Mission Design Game, escolhido (ADR 0004); equipe ASTRIX11;
  recursos da NASA da primeira versão (ADR 0005); multijogador adiado para depois da primeira
  versão (ADR 0006); integrante menor só por iniciais na entrega (ADR 0007); stack não definida;
  sem CI; licença Apache 2.0 (ADR 0003).
- 15/11/2026: nome do projeto: ASTRIX Mission Studio.
- 14/11/2026: os outros quatro integrantes ainda não foram convidados como colaboradores.
- Prazo de submissão: 15/11/2026, 23h59, horário do evento local (`docs/entrega.md`).

## 6. Armadilhas já pagas

- `www.spaceappschallenge.org` falha com erro de cadeia de certificado (raiz não confiável) no
  `curl` e no WebFetch da máquina do dono do repositório (14/11/2026). Não contorne com `-k`:
  leia a página pelo Chrome, que abre normalmente.
- `* text=auto` trata como texto um PDF sem nenhum byte nulo, e o checkout no Windows o corrompe
  (aconteceu com `assets/Recursos_Dados_NASA_Ceres_2026.pdf`, 14/11/2026). Binário novo precisa da
  extensão marcada como `binary` no `.gitattributes`. Quem clonou no Windows antes dessa correção
  fica com a cópia corrompida mesmo depois de atualizar: apague o arquivo e rode `git restore` nele.
  Não rode `git add --renormalize` antes disso, porque ele levaria a cópia corrompida para o commit.
- Citação de fonte se confere no arquivo baixado (`data/raw/`), não em resumo de busca nem em
  relato de agente: a revisão de 14/11/2026 achou estudo descrito como medida de aprendizado que
  media autoeficácia, e número sem fonte lida.

## 6b. Segurança

- Ainda não há autenticação, API nem dado sensível. Ao introduzir qualquer um deles, redefina o
  perfil e siga `C:\dev\docs\padroes\seguranca-aplicacao.md`.
- Exceções aceitas ao perfil: nenhuma por ora. O perfil GLOBAL pede portão no CI: o primeiro
  código sem CI exige ADR ou a pendência de CI resolvida.

## 7. Onde está cada coisa

| Vai mexer em… | Leia antes |
|---|---|
| escolha ou escopo do desafio | `docs/desafios/README.md` (comparativo), `docs/desafio.md` (decisão) |
| escopo, público ou mecânica do jogo | `docs/problematica.md` (perguntas Q1 a Q8), `docs/adr/0005-recursos-nasa-primeira-versao.md`, `docs/adr/0006-multijogador-depois-da-primeira-versao.md` |
| pitch ou one-liner | `docs/pitch.md` (10 s), `docs/pitch-final.md` (3 min) |
| nome ou crédito de integrante | `docs/adr/0007-integrante-menor-por-iniciais.md` |
| página de submissão, demo, slides, licença | `docs/entrega.md`, `docs/adr/0003-licenca-apache-2-0.md` |
| versão de entrega em inglês | `docs/adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md` |
| dado da NASA ou de agência parceira | `docs/entrega.md` (registro de fontes), `docs/desafios/13-recursos.md` (o que cada recurso da aba traz) |
| fluxo de branch, commit e PR | `CONTRIBUTING.md`, `docs/adr/0001-fluxo-de-git-branch-curta-e-pr.md` |
| algo ainda não decidido | `docs/pendencias.md` |
| decisão nova com alternativas | `docs/adr/README.md` (modelo) |
