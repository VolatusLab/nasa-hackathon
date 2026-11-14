# Como contribuir

Vale para os cinco integrantes do Grupo 2 e para qualquer assistente de código usado no projeto.

## Fluxo de trabalho

A `main` é a versão que será demonstrada: ela precisa funcionar o tempo todo.

1. Atualize a sua cópia:

   ```bash
   git switch main
   git pull
   ```

2. Crie uma branch curta (ex.: `feat/mapa-de-queimadas`, `docs/roteiro-da-demo`):

   ```bash
   git switch -c tipo/descricao-curta
   ```

3. Faça commits pequenos, uma intenção por commit.
4. Envie a branch e abra um pull request para a `main`:

   ```bash
   git push -u origin tipo/descricao-curta
   ```

   O GitHub mostra o botão "Compare & pull request" na página do repositório. Quem usa a linha
   de comando pode rodar `gh pr create`.
5. Um colega revisa e aprova. Depois disso o autor faz o merge pelo botão do pull request e
   apaga a branch.

Se a `main` andou enquanto você trabalhava, traga as mudanças para a sua branch antes do merge:

```bash
git pull origin main
```

Se aparecer conflito e você não souber resolver, peça ajuda no grupo antes de forçar qualquer
coisa.

Correção trivial de documentação (erro de digitação, link quebrado) pode ir direto na `main`.

A `main` não está protegida no GitHub: a regra de revisão vale por acordo do grupo. O motivo
desse fluxo está em
[`docs/adr/0001-fluxo-de-git-branch-curta-e-pr.md`](docs/adr/0001-fluxo-de-git-branch-curta-e-pr.md).

## Mensagem de commit

[Conventional Commits](https://www.conventionalcommits.org/pt-br/) em pt-BR, com escopo, primeira
linha com até ~72 caracteres:

```text
feat(mapa): exibe focos de calor das últimas 24 h
fix(api): trata resposta vazia do serviço de dados
docs(entrega): registra fonte dos dados de precipitação
chore: configura lint
```

Tipos usados: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`. O corpo, quando existir,
explica o **porquê**. Trabalho feito com assistente de IA termina com a linha `Co-Authored-By`
dele.

## Antes de abrir o pull request

- O que você mudou roda na sua máquina.
- O portão do projeto passa (typecheck, lint, teste e build), quando ele existir. Os comandos
  ficam no `README.md`.
- `git diff` revisado: sem segredo, sem dado pessoal, sem arquivo gerado.
- A documentação afetada foi atualizada **no mesmo pull request**.

## Nunca versionar

- Segredo: chave de API, token, senha, arquivo `.env` (só o `.env.example` entra, sem valores
  reais), credenciais do Earthdata (`.netrc`).
- Dado pessoal real: nome, CPF, telefone ou e-mail em teste, exemplo ou dado de apoio. Use
  fictícios ("Maria Exemplo", `000.000.000-00`).
- Arquivo gerado: `node_modules`, `dist`, `.venv`, cache.
- Arquivo grande de dados: guarde em `data/raw/`, que o Git ignora, e registre a fonte e o link
  em `docs/entrega.md`. O GitHub recusa arquivo acima de 100 MB.

Se um segredo for enviado por engano, avise o grupo na hora: apagar o commit não basta, a chave
precisa ser trocada.

## Dados e fontes

A entrega é avaliada também pelo uso de dados abertos, e os termos do evento exigem que toda
fonte seja citada. Todo dado ou recurso usado entra na tabela de fontes de
[`docs/entrega.md`](docs/entrega.md), com link, licença e data de acesso, no mesmo pull request
que passa a usá-lo.

- Material que não seja da NASA nem de agência parceira precisa ser público e sem restrição, ou
  ter licença de código aberto. Confira a licença **antes** de usar uma biblioteca, imagem ou
  conjunto de dados.
- Número sem fonte não entra no produto nem nos slides.

## Uso de IA

O evento permite IA como ferramenta, com três regras (detalhe em
[`docs/entrega.md`](docs/entrega.md)):

- a **ideia** de como resolver o desafio deve ser do grupo, não da IA;
- imagem e vídeo gerados levam marca d'água visível; código, dados e áudio gerados levam aviso
  no texto e nos metadados;
- nada gerado pode usar ou alterar marca da NASA.

Registre em `docs/entrega.md` cada ferramenta usada e para quê. É mais fácil anotar na hora do
que reconstruir no fim.

Assistente de código não faz commit nem envia (`push`) sem a aprovação de quem o opera, e nunca
usa `push --force`, `reset --hard`, `clean -fd` ou `--no-verify` sem pedido explícito.

## Entrega em inglês

A página de submissão, os slides, a interface do produto e tudo o que os links da submissão
abrem precisam estar em inglês. Só o vídeo pode ser falado em português, com legenda em inglês.

A documentação deste repositório continua em pt-BR. Por isso ele não é o link da submissão: a
versão de entrega em inglês sai em fork ou repositório novo, gerada a partir do estado final
([ADR 0002](docs/adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md)).

## Documentação

Cada informação tem um lugar só:

| O fato é… | Vai para |
|---|---|
| o que mudou e quando | [`CHANGELOG.md`](CHANGELOG.md), em 1 a 3 linhas |
| como algo funciona | o documento do assunto em `docs/` |
| decisão com alternativas | um ADR em `docs/adr/` |
| o que ainda falta decidir | [`docs/pendencias.md`](docs/pendencias.md) |
| como instalar, rodar e testar | [`README.md`](README.md) |

Idioma: documentação interna e commits em pt-BR; nomes no código em inglês, sem acento;
interface do produto em inglês.
