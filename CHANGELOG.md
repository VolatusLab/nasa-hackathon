# Changelog

O que mudou e quando, do mais recente para o mais antigo. De 1 a 3 linhas por entrada; o detalhe
fica no documento do assunto.

## 15/11/2026

- Guia do pitch final de 3 minutos para a banca local em `docs/pitch-final.md`: cinco estágios com tempos, orçamento de palavras, roteiro com lacunas, demo e plano B, perguntas prováveis e ensaio. Pitch todo em português; duração e formato `[VERIFICAR]` com a organização.

## 14/11/2026

- Os nove recursos da aba oficial descritos um a um em `docs/desafios/13-recursos.md`, a partir dos arquivos baixados. Texto oficial das abas Details e Resources guardado em `assets/`.
- Problemática consolidada, com 12 fontes: ganha a seção 12, com o que o enunciado pede e o que só sugere, o que os materiais de entrega podem afirmar, como as perguntas dependem umas das outras e quais números têm fonte lida. Passou por três rodadas de revisão por pares.
- Revisão geral e revisão por pares com agentes: citações da problemática e tradução do enunciado conferidas contra os arquivos-fonte, e textos desatualizados depois dos ADRs 0005 a 0007 corrigidos.
- Problemática corrigida: o estudo com o KSP mede autoeficácia, não aprendizado; saiu um número sem fonte lida; sugestões do enunciado deixaram de aparecer como exigência; inferências passam a ser rotuladas como leitura de quem redigiu.
- `.gitattributes` passa a marcar PDF e outros binários: o `text=auto` corrompia um PDF de `assets/` no checkout do Windows. O `data/raw/MANIFEST.tsv` passa a ser versionado.
- Multijogador para até quatro pessoas fica para depois da primeira versão (ADR 0006). O integrante menor aparece só por iniciais nos materiais de entrega (ADR 0007).
- Recursos da NASA da primeira versão aprovados (ADR 0005): números de kits de imprensa como referência, Mission Viz e Webb só por link.
- Problemática do desafio 13 em `docs/problematica.md`, reescrita com foco em prática e avaliação, 11 fontes e 8 perguntas de decisão. Lacunas de evidência e de contexto brasileiro ficam marcadas `[VERIFICAR]`.
- Datas corrigidas: registros que descreviam fatos de 14/11/2026 com data de 15/11/2026 foram ajustados. O prazo de submissão, 15/11/2026, continua.
- Enunciado completo e aba Recursos do desafio 13 traduzidos para pt-BR em `docs/desafios/13-enunciado-completo.md`; lista de recursos conferida com a aba oficial; modelo de pitch de 10 s em `docs/pitch.md`.
- Impressões oficiais (desafio, aba Recursos, recursos do evento e palestra de pitch) versionadas em `assets/`.
- Desafio 13 (Space Mission Design Game) escolhido, registrado no ADR 0004; nome da equipe: ASTRIX11.
- Escopo decidido: multijogador para até quatro pessoas na primeira versão, e uso de recursos da NASA (ADR 0004). O multijogador foi adiado depois, no ADR 0006.
- Revisão de toda a documentação contra as páginas oficiais, com correções. Entraram as regras dos termos do evento (licença aberta, material de terceiros, menor de 18 anos) e a interface do produto passou a ser em inglês.
- `docs/pendencias.md` separa o que bloqueia a submissão; `.gitignore` ampliado e `.gitattributes` criado.
- Decisões registradas: documentação em pt-BR com entrega em inglês em fork ou repositório novo (ADR 0002) e licença Apache 2.0 (ADR 0003). Fluxo de Git confirmado (ADR 0001).
- Repositório renomeado de `nasa-hackaton` para `nasa-hackathon`.
- Regras de submissão e julgamento conferidas nos guias oficiais de 2026 (`docs/entrega.md`).
- Um documento por desafio e comparativo dos 14 desafios (`docs/desafios/`).
- Repositório criado (privado) e documentação de base: `README`, `CONTRIBUTING`, `CLAUDE.md`, índice de `docs/`, desafio, entrega, pendências e ADR 0001 (fluxo de Git).
