# Pendências

Decisões em aberto. Item resolvido sai daqui e vai para o documento do assunto (ou vira ADR).

Atualizado em 14/11/2026. **Prazo de submissão: 15/11/2026, 23h59** ([`entrega.md`](entrega.md)).

## Bloqueiam a submissão

| # | Pendência | Quem decide | Depende de |
|---|---|---|---|
| 1 | Confirmar que os cinco, inclusive o dono do time, estão inscritos no mesmo evento local, fora da lista de espera e na aba "Members" | grupo | — |
| 2 | Há integrante menor de 18 anos: confirmar que foi inscrito por responsável legal e que está acompanhado por ele durante o evento | grupo | — |
| 3 | Perguntar à organização local como listar o integrante menor nos slides: o guia pede os nomes dos integrantes e os termos vetam nome reconhecível de menor | grupo | — |
| 4 | Confirmar que nenhum integrante participa por vínculo com a China ou com entidade de propriedade chinesa | grupo | — |
| 5 | Convidar os outros quatro integrantes como colaboradores do repositório | dono da conta `VolatusLab` | usuário do GitHub de cada um |
| 6 | Definir o restante do escopo da primeira versão: o que entra e o que fica de fora. O multijogador para até quatro pessoas já entra (decidido em 14/11/2026, [`desafio.md`](desafio.md)) | grupo | — |
| 7 | Escolher quais recursos da NASA entram no jogo. O uso já foi decidido em 14/11/2026, e o critério "Relevância" pede dado como parte central. A aba Recursos oficial tem nove links, listados em [`desafios/13-jogo-de-projeto-de-missao.md`](desafios/13-jogo-de-projeto-de-missao.md) | grupo | — |
| 8 | Definir a stack e registrar em ADR | grupo | 6 |
| 9 | Definir o nome do projeto (o nome da equipe, ASTRIX11, já está definido) e quem edita a página do projeto no site do evento | grupo | — |
| 10 | Definir o formato da demo (slides ou vídeo) e quem a conduz | grupo | 6 |
| 11 | Publicar a versão de entrega em inglês (fork, repositório novo ou site), com link público, licença e fontes, e produzir em inglês a página de submissão e os slides ([ADR 0002](adr/0002-documentacao-em-pt-br-e-entrega-em-ingles.md)). Se for site novo, considerar o pedido de classificação no FortiGuard | grupo | 8 |
| 12 | Ler os termos e condições e a política de privacidade: quem marca o aceite na submissão precisa ter lido | quem submete | — |

## Não bloqueiam

| # | Pendência | Quem decide | Depende de |
|---|---|---|---|
| 13 | Decidir se os nomes dos integrantes maiores de idade entram no `README.md` | cada integrante | — |
| 14 | Confirmar com a organização de Ceres-GO os horários do julgamento e da premiação locais, e a duração do pitch final para a banca (a palestra de 14/11/2026 citou 3 min, `[VERIFICAR]`) | grupo | — |
| 15 | Configurar CI com o portão do projeto | grupo | 8 |
| 16 | Redigir o one-liner de 10 s com a ideia do grupo, a partir do modelo em [`pitch.md`](pitch.md) | grupo | 6 |
| 17 | Validar a problemática em [`problematica.md`](problematica.md) antes de fechar o escopo e a stack: confirmar as fontes (incluindo as lacunas `[VERIFICAR]`) e responder às perguntas Q1 a Q8 | grupo | — |
