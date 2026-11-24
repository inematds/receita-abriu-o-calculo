# Handoff — 2026-11-24 — explicativo "Receita abriu o cálculo": fase 2 (banners, personagens, vídeo lives1)

## Projeto e escopo
Projeto ~/projetos/receita-abriu-o-calculo (repo inematds/receita-abriu-o-calculo, Pages em /guia/ PT/EN/ES). Pedido do Nei (24/11): explicativo de que a Receita abriu o cálculo do imposto, com logo da Receita como fonte, as duas notas R$ 56,76 / R$ 72,88, link para o guia calculadora-da-reforma; publicado no portal e INEMA.VIBE. Segundo pedido: fazer o explicavideo e publicar no lives1; corrigir guia sem banner padrão e sem personagem nos cards "Para você".

## Objetivo atual
(1) banners live+grade em PT/EN/ES no guia e README; (2) imagem de personagem em cada card de #voce (4 perfis), nos 3 idiomas; (3) explicavideo do projeto publicado no lives1 e embutido no #video do guia PT/EN/ES + README. Pronto = 3 páginas 200 com os itens no ar + link do YouTube no lives1.

## Estado aceito
- [confirmed] Guia PT/EN/ES no ar — evidência: commit 9bc3881; fetch das 3 URLs → 200 com texto novo
- [confirmed] Revisor independente: R1 7 reprovado, R2 7 reprovado, R3 8 aprovado — evidência: ~/projetos/wifi/revisor-falhas.md e revisor-nota.py
- [confirmed] Portal publicado — evidência: portal 3b9292b, inemabuscas 5071f9a, inemapro 209e173
- [confirmed] Tópico INEMA.VIBE https://t.me/c/3650752323/4364, MENU msg 4380 — evidência: saída do postar_topico.py
- [confirmed] Críticas do Nei (banner, personagem) registradas como dono — evidência: ~/projetos/wifi/revisor-falhas.md

## Proposto / tentado, não confirmado
- [unverified] 6 banners gerando em segundo plano (/tmp/claude-1000/banners.sh) — saída em guia/assets/banner{,-en,-es}.jpg e banner-grade{,-en,-es}.jpg; conferir texto de cada um
- [unverified] 4 personagens gerando (/tmp/claude-1000/quem.sh) → guia/assets/quem-{comprador,vendedor,contador,dev}.jpg
- [?] pages.yml usa upload-pages-artifact v3; a sessão calculadora trocou para v4 (commit 9938ebf lá) porque v3 deixava deploy sem artefato. Trocar aqui também.

## Decisões
- Imagem das notas sai de kit/notas.html (HTML→screenshot), nunca de gerador — para não errar dígito.
- 8,8% = só número de teste do exemplo da Receita; 11,3% = TCU, não aprovada (revisor R2).
- Logo da Receita só como fonte, com link e aviso "não oficial" (CLAUDE.md).

## Não fazer (restrições e travas)
- Logo da Receita nunca em banner/imagem gerada por IA — fonte: CLAUDE.md
- Números só os de ~/projetos/calculadora-da-reforma/kit/MEDICOES.md — fonte: CLAUDE.md
- Nunca API sem autorização; tradução por inema-traduz; imagem por Codex — fonte: ~/.claude/CLAUDE.md
- Vídeo: explicavideos v2 + avatar do Nei pelo estúdio HeyGen; nunca trocar plano HeyGen — fonte: ~/.claude/CLAUDE.md
- Commit autor inematds; portal autor NeiMaldaner (o publica.sh resolve) — fonte: ~/.claude/CLAUDE.md
- Exclusão no Telegram só com aprovação individual — fonte: ~/.claude/CLAUDE.md

## Arquivos alterados
- `guia/index.html`, `guia/en/index.html`, `guia/es/index.html` — página
- `kit/notas.html` — gerador da imagem das notas (?lang=, &v=1 vertical)
- `README.md`, `README.en.md`, `README.es.md`, `CLAUDE.md`, `FALHAS.md`
- Fora: `~/projetos/portal/src/{components/Portal.tsx,data/courses.ts,data/translated-courses.ts}`, `~/projetos/inemapro-mono/packages/content-base/enrichment.json`, `~/projetos/output/posts-telegram/2026-11-24-receita-abriu-o-calculo.md`

## Memória e regras duráveis tocadas
- `CLAUDE.md` (deste repo) — lição: seguir a skill projetos-landing-guia inteira (banner + personagem)
- `~/projetos/wifi/revisor-falhas.md` — R1, R2 e 2 críticas do dono

## Verificação
- Rodado: `pronto-para-revisar.py .` → PRONTO (antes da rodada R2)
- Rodado: fetch das 3 URLs do guia → 200, conteúdo novo
- Rodado: `npm test` no portal → 13 pass, 0 fail
- Não rodado: pronto-para-revisar depois das mudanças de R3 — não refeito

## Estado em execução
- Processos em segundo plano: banners.sh (shell bsstki3bg) e quem.sh (shell bcpi2zsrk), ambos codex exec; terminam sozinhos
- Servidores / portas: nenhum
- Worktrees / branches abertos: nenhum

## Perguntas abertas e adiados
- Adiado: explicavideo — ainda não estudei o fluxo; modelo: cadeias ev-calculadora-reforma-lives4 e pastas ~/projetos/explicavideos/textos/calculadora-da-reforma-lives4

## Pela metade
- Banners e personagens — parou em: geração em segundo plano — falta: conferir imagens, inserir no HTML (hero: banner.jpg? manter notas? banner-grade abaixo do #resumo; .quem-img nos cards de #voce), EN/ES com ../assets e -en/-es, README com banner, commit+push
- Vídeo — falta tudo

## Próxima ação exata
Conferir os 6 banners e 4 personagens, inserir no guia PT/EN/ES e README, push. Depois montar a cadeia do explicavideo para o lives1 (seguir o modelo da calculadora-da-reforma-lives4) e deixar CONTINUAR.md + continua --add para a fase 2 (embed no #video).

## Mapa de retomada
- `CLAUDE.md` — regras do repo e lição
- `guia/index.html` — página PT
- `~/.claude/skills/projetos-landing-guia/SKILL.md` — padrão de guia (banner, #quem com imagem, vídeo D21)
- `~/projetos/calculadora-da-reforma/CONTINUAR-SESSAO.md` — como a outra sessão montou as cadeias de vídeo

## Perguntas-teste
1. Qual é a tarefa atual e o critério de pronto? → banners + personagens no guia e explicavideo no lives1 embutido no guia — fonte: só nesta conversa — chave: `lives1`
2. Qual foi a última decisão e por quê? → seguir a skill inteira (banner live+grade, imagem por perfil) após crítica do Nei — fonte: CLAUDE.md — chave: `banner`
3. O que não pode mudar? → logo da Receita só como fonte, nunca em imagem de IA — fonte: CLAUDE.md — chave: `fonte`
4. O que está pela metade? → geração de banners e personagens; vídeo não começado — fonte: só nesta conversa — chave: `quem-`
5. Próxima ação? → inserir imagens no guia e push; depois cadeia do vídeo lives1 (publicação YouTube autorizada pelo pedido) — fonte: só nesta conversa — chave: `explicavideo`

## Checagem de compartilhamento
- Sem segredos, tokens, cookies, dados pessoais ou endpoints privados: sim


<!-- handoff-estado:inicio -->
## Estado gravado pelo script (não editar)

Gravado por handoff-grava.py no momento do handoff. `--conferir` compara com o projeto agora.

- commit: b7f9bdff1fbb633dffa89af9e475aa6cf9da2dc5 · branch: main
- arquivos sujos fora de handoffs/: 7
- `CLAUDE.md` · sha256:057cf5b57bd2 · sujo
- `guia/assets/banner-en.codex.log` · sha256:cb129cf2a83e · sujo
- `guia/assets/banner-es.codex.log` · sha256:070d9b2c5516 · sujo
- `guia/assets/banner-grade-en.codex.log` · sha256:c498bc5a3214 · sujo
- `guia/assets/banner-grade-es.codex.log` · sha256:f7fd0ff253fa · sujo
- `guia/assets/banner-grade.codex.log` · sha256:28753c101c8e · sujo
- `guia/assets/banner.codex.log` · sha256:4f82aefe2ba5 · sujo
- `guia/index.html` · sha256:76ff3cdacf18 · citado
- `guia/en/index.html` · sha256:cddbc9daacbc · citado
- `guia/es/index.html` · sha256:30ebe110a7e1 · citado
- `kit/notas.html` · sha256:51361b4488f3 · citado
- `README.md` · sha256:6585d66b466a · citado
- `README.en.md` · sha256:6f80446f3bc0 · citado
- `README.es.md` · sha256:081cb9edb185 · citado
- `FALHAS.md` · sha256:473d2d996e5c · citado
<!-- handoff-estado:fim -->
