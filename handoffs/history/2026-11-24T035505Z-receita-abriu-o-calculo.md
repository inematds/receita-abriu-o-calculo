# Handoff — 2026-11-24 — receita-abriu-o-calculo: banners e personagens no ar; vídeo lives1 na cadeia + vigia

## Projeto e escopo
~/projetos/receita-abriu-o-calculo (explicativo PT/EN/ES, Pages /guia/). Pedido do Nei 24/11: explicavideo no lives1; corrigir o guia sem banner padrão e sem personagem no "Para você".

## Objetivo atual
Vídeo lives1 publicado e embutido no guia. A fase 2 é feita pelo vigia continua (bilhete em ~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/CONTINUAR.md).

## Estado aceito
- [confirmed] Banners live+grade PT/EN/ES e 4 personagens no #voce — evidência: commit 240830a; fetch das 3 URLs → "novo", assets 200
- [confirmed] Críticas do Nei registradas (--quem dono) — evidência: ~/projetos/wifi/revisor-falhas.md
- [confirmed] Cadeia do vídeo rodando — evidência: systemctl --user is-active ev-receita-abriu-lives1; cadeia.log "ficha: claude -p"
- [confirmed] Vigia registrado — evidência: continua.py saída "receita-abriu-lives1 esperando", msg 688 no v3

## Proposto / tentado, não confirmado
- nenhum

## Decisões
- Hero = banner.jpg (padrão); imagem das notas abre a seção #notas; banner-grade abaixo do #resumo.
- Vídeo segue a mesma cadeia da calculadora (roda.sh copiado em textos/receita-abriu-o-calculo/).

## Não fazer (restrições e travas)
- Logo da Receita nunca no vídeo nem em imagem de IA — fonte: CLAUDE.md
- Números só do MEDICOES.md — fonte: CLAUDE.md
- Não reenviar avatar ao HeyGen; nunca trocar plano — fonte: ~/.claude/CLAUDE.md
- Telegram: responder no tópico 4364, não criar outro — fonte: CONTINUAR.md do lives1

## Arquivos alterados
- `guia/index.html`, `guia/en/index.html`, `guia/es/index.html`, `README*.md`, `.github/workflows/pages.yml` (v4), `CLAUDE.md` (lição)
- `guia/assets/banner*.jpg`, `guia/assets/quem-*.jpg`
- Fora: `~/projetos/explicavideos/textos/receita-abriu-o-calculo/{FATOS.md,regras-comuns.md,roda.sh,avatar-fila.sh}`, `~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/{pedido.txt,regras.md,CONTINUAR.md}`

## Memória e regras duráveis tocadas
- `CLAUDE.md` — lição: seguir a skill inteira (banner + personagem)

## Verificação
- Rodado: pronto-para-revisar.py → PRONTO
- Rodado: fetch das 3 URLs → conteúdo novo; banner/quem 200
- Não rodado: revisor independente depois de banners/personagens — mudança só visual

## Estado em execução
- Processos: unit systemd de usuário `ev-receita-abriu-lives1` (cadeia do vídeo); parar com `systemctl --user stop ev-receita-abriu-lives1`
- Vigia continua: receita-abriu-lives1 (timer a cada 5 min)

## Perguntas abertas e adiados
- nenhum

## Pela metade
- Vídeo — parou em: fase ficha — falta: avatar, visual, entrega (cadeia) e fase 2 (vigia)

## Próxima ação exata
Nada manual: o vigia abre sessão quando a cadeia terminar e segue o CONTINUAR.md. Se o Nei perguntar, ver `tail ~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/cadeia.log`.

## Mapa de retomada
- `~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/CONTINUAR.md` — fase 2
- `CLAUDE.md` — regras do repo
- `guia/index.html` — página

## Perguntas-teste
1. Tarefa atual? → vídeo lives1 pela cadeia + vigia — fonte: ~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/CONTINUAR.md — chave: `lives1`
2. Última decisão? → banner no hero, notas na seção #notas — fonte: commit 240830a — chave: `banner`
3. O que não pode mudar? → não reenviar avatar ao HeyGen — fonte: CONTINUAR.md — chave: `HeyGen`
4. Pela metade? → cadeia do vídeo na fase ficha — fonte: cadeia.log — chave: `ficha`
5. Próxima ação? → esperar o vigia; nada manual — fonte: CONTINUAR.md — chave: `vigia`

## Checagem de compartilhamento
- Sem segredos, tokens ou dados pessoais: sim


<!-- handoff-estado:inicio -->
## Estado gravado pelo script (não editar)

Gravado por handoff-grava.py no momento do handoff. `--conferir` compara com o projeto agora.

- commit: 240830aa62bcf36490a3922642875ff5003219c3 · branch: main
- arquivos sujos fora de handoffs/: 0
- `guia/index.html` · sha256:57e281c5003d · citado
- `guia/en/index.html` · sha256:a81998fe5930 · citado
- `guia/es/index.html` · sha256:3dc90688d83e · citado
- `.github/workflows/pages.yml` · sha256:716ee3dd84d5 · citado
- `CLAUDE.md` · sha256:057cf5b57bd2 · citado

### Repo do trabalho: /home/nmaldaner/projetos/explicavideos
- commit: 53466f36ea02dfc7305c719a271efaffdef8c3da · branch: main
- arquivos sujos: 428 (lista cortada)
- impressão de todos os sujos: df3a153ea810747a
- `FALHAS.md` · sha256:65d4c10b6557 · sujo
- `README.md` · sha256:6ceb6c71b2ba · sujo
- `bot/entrega.sh` · sha256:18212fa82900 · sujo
- `engine/build_visual_block.py` · sha256:cad49c345580 · sujo
- `engine/v2/critico_chamada.py` · sha256:122e878d8fbd · sujo
- `examples/1AzRvvF3n5-v2.json` · sha256:2e008191171a · sujo
- `examples/1AzRvvF3n5.json` · sha256:8c5223f53b62 · sujo
- `examples/1DamuwTfJa-v2.json` · sha256:c35c0d100f41 · sujo
- `examples/1DamuwTfJa.json` · sha256:443bb5f65468 · sujo
- `examples/1KXMjGvJ3V-v2.json` · sha256:fea40c513394 · sujo
- `examples/1KXMjGvJ3V.json` · sha256:211be4f9d107 · sujo
- `examples/agent-skills-addy-v2.json` · sha256:9ad0204762dc · sujo
- `examples/agent-skills-addy.json` · sha256:5c442c38f282 · sujo
- `examples/agentes-autoaprimoram-v2-916.json` · sha256:2c1923c98eee · sujo
- `examples/agentes-autoaprimoram-v2.json` · sha256:3d4e514cbc17 · sujo
- `examples/agentes-autoaprimoram.json` · sha256:ad131c05ebeb · sujo
- `examples/agentic-app-framework-v2-916.json` · sha256:4aa119ffcdd0 · sujo
- `examples/agentic-app-framework-v2.json` · sha256:139af6d17f17 · sujo
- `examples/agentic-app-framework.json` · sha256:9e2734a970f1 · sujo
- `examples/agentic-app-ideia-v2-916.json` · sha256:86020923fe2c · sujo
- `examples/agentic-app-ideia-v2.json` · sha256:18888b26ac25 · sujo
- `examples/agentic-app-ideia.json` · sha256:2468f5c9a821 · sujo
- `examples/agentic-app-v2.json` · sha256:c99f76d6c8f7 · sujo
- `examples/agentic-app.json` · sha256:94b0e4c2807b · sujo
- `examples/ai-harness-en-v2.json` · sha256:b09427331b28 · sujo
- `examples/ai-harness-en.json` · sha256:7f55ecd84689 · sujo
- `examples/ai-harness-es-v2.json` · sha256:8c225a40ad85 · sujo
- `examples/ai-harness-es.json` · sha256:c1caae4e3c7e · sujo
- `examples/ai-harness-pro-en-v2.json` · sha256:6044d99333a0 · sujo
- `examples/ai-harness-pro-es-v2.json` · sha256:c46dcd225af0 · sujo
- `examples/ai-harness-pro-v2.json` · sha256:82a0cf7b27ce · sujo
- `examples/ai-harness-v2.json` · sha256:17615e01eecd · sujo
- `examples/ai-harness.json` · sha256:53a388c69613 · sujo
- `examples/ai2027-adiantado-v2-916.json` · sha256:ec73dff41d69 · sujo
- `examples/ai2027-adiantado-v2.json` · sha256:d6c46f3108ed · sujo
- `examples/ai2027-adiantado.json` · sha256:06089649c824 · sujo
- `examples/apagao-sem-gerador-v2-916.json` · sha256:d11be9da34b9 · sujo
- `examples/apagao-sem-gerador-v2.json` · sha256:dcc706677bed · sujo
- `examples/apagao-sem-gerador.json` · sha256:5b759516ea09 · sujo
- `examples/apocalipse-seguranca-v2-916.json` · sha256:a3db2de5e145 · sujo
- `examples/apocalipse-seguranca-v2.json` · sha256:f866ea2cabd2 · sujo
- `examples/apocalipse-seguranca.json` · sha256:53dbaf20c009 · sujo
- `examples/astra-caixa-preta-v2-916.json` · sha256:25464dede49f · sujo
- `examples/astra-caixa-preta-v2.json` · sha256:cf15c5357aa6 · sujo
- `examples/astra-caixa-preta.json` · sha256:eb4c6efd95d5 · sujo
- `examples/atende-academia-promo-v2.json` · sha256:fead886d2dd7 · sujo
- `examples/atende-academia-promo.json` · sha256:7ff7e4c97848 · sujo
- `examples/atende-fisioterapia-promo-v2.json` · sha256:63b963dcff02 · sujo
- `examples/atende-fisioterapia-promo.json` · sha256:80f787091913 · sujo
- `examples/atende-leads-demo-v2-916.json` · sha256:a175f3e76db7 · sujo
- `examples/atende-leads-demo-v2.json` · sha256:0840bd1c893d · sujo
- `examples/atende-leads-demo.json` · sha256:84b23ed447c1 · sujo
- `examples/atende-leads-promo-v2-916.json` · sha256:c1d04ef36254 · sujo
- `examples/atende-leads-promo-v2.json` · sha256:d9546c0d96b5 · sujo
- `examples/atende-leads-promo.json` · sha256:f7ecd433457e · sujo
- `examples/atende-nutricao-promo-v2.json` · sha256:990e1b2b5929 · sujo
- `examples/atende-nutricao-promo.json` · sha256:d8abd91ee368 · sujo
- `examples/bigtech-boazinhas-v2.json` · sha256:73a6c6fc36a0 · sujo
- `examples/bigtech-boazinhas.json` · sha256:6e725dd88814 · sujo
- `examples/bigtech-paga-b-v2.json` · sha256:65316fd6e7cd · sujo
- `examples/bigtech-paga-v2.json` · sha256:191277923e1e · sujo
- `examples/bigtech-paga.json` · sha256:8ebefd1a9d24 · sujo
- `examples/camada-contexto-v2.json` · sha256:2fdee0374316 · sujo
- `examples/camada-contexto.json` · sha256:d43a6c31b6ae · sujo
- `examples/ccdashboard-reel-v2.json` · sha256:0c5d76cea62d · sujo
- `examples/ccdashboard-reel.json` · sha256:d838b9059038 · sujo
- `examples/cerebro-niveis-v2.json` · sha256:a95ad96a56b5 · sujo
- `examples/cerebro-niveis.json` · sha256:8d4ce7c43df9 · sujo
- `examples/cga-a1-v2.json` · sha256:91e0b46ce07e · sujo
- `examples/cga-a1.json` · sha256:260c4ce04c6a · sujo
- `examples/cga-a2-v2.json` · sha256:6ed4a1b200d6 · sujo
- `examples/cga-a2.json` · sha256:8bf12d77d988 · sujo
- `examples/cga-a3-v2.json` · sha256:c479e734495d · sujo
- `examples/cga-a3.json` · sha256:54b7b58d96fb · sujo
- `examples/cga-a4-v2.json` · sha256:48310a8f7b6e · sujo
- `examples/cga-a4.json` · sha256:1ec38bc6d4dd · sujo
- `examples/cga-a5-v2.json` · sha256:0825ac19fe22 · sujo
- `examples/cga-a5.json` · sha256:9f5a8b2ab6fb · sujo
- `examples/cga-a6-v2.json` · sha256:09358cb46bb0 · sujo
- `examples/cga-a6.json` · sha256:ef4d5bd66ec4 · sujo
- `examples/cga-a7-v2.json` · sha256:6f424c7a63ac · sujo
- `examples/cga-a7.json` · sha256:6e9b4d429bc4 · sujo
- `examples/cga-a8-v2.json` · sha256:588f87836979 · sujo
- `examples/cga-a8.json` · sha256:3a3ff44dfd05 · sujo
- `examples/chatgpt-16-ferramentas-v2-916.json` · sha256:55be535b713c · sujo
- `examples/chatgpt-16-ferramentas-v2.json` · sha256:03761b9b83f6 · sujo
- `examples/chatgpt-16-ferramentas.json` · sha256:93f2a412f3db · sujo
- `examples/claude-estudio-video-v2.json` · sha256:afdb9a0f9528 · sujo
- `examples/claude-estudio-video.json` · sha256:7d9da0be39b8 · sujo
- `examples/clone-viral-hypit-v2.json` · sha256:c0dea4fb3de1 · sujo
- `examples/clone-viral-hypit.json` · sha256:2fffc442ec1d · sujo
- `examples/concat-anim-v2-916.json` · sha256:4a5a3aece349 · sujo
- `examples/concat-anim.json` · sha256:53c225fd0fad · sujo
- `examples/concat-viral-916-v2.json` · sha256:6ef93f48af79 · sujo
- `examples/concat-viral-916.json` · sha256:4791c7ce5b26 · sujo
- `examples/consultor-ia-2027-en-v2.json` · sha256:d1053f809fc7 · sujo
- `examples/consultor-ia-2027-en.json` · sha256:2b0c27df929b · sujo
- `examples/consultor-ia-2027-es-v2.json` · sha256:975981b70925 · sujo
- `examples/consultor-ia-2027-es.json` · sha256:0c3d5105d16a · sujo
- `examples/consultoria-ia-caminhos-en-v2.json` · sha256:7872b51291be · sujo
- `examples/consultoria-ia-caminhos-en.json` · sha256:73df53a074b1 · sujo
- `examples/consultoria-ia-caminhos-es-v2.json` · sha256:2ea5d5ef3fc1 · sujo
- `examples/consultoria-ia-caminhos-es.json` · sha256:43e3531e09a2 · sujo
- `examples/consultoria-ia-na-pratica-en-v2.json` · sha256:9a4260a201c9 · sujo
- `examples/consultoria-ia-na-pratica-en.json` · sha256:dbc7168400f7 · sujo
- `examples/consultoria-ia-na-pratica-es-v2.json` · sha256:59ba851b7cdc · sujo
- `examples/consultoria-ia-na-pratica-es.json` · sha256:bf626e47b22c · sujo
- `examples/consultoria-ia-na-pratica-v2.json` · sha256:bf69082e5382 · sujo
- `examples/consultoria-ia-na-pratica.json` · sha256:e2e5b348ae67 · sujo
- `examples/contexto-portatil-v2.json` · sha256:78153674fb68 · sujo
- `examples/contexto-portatil.json` · sha256:8e71552e5c0e · sujo
- `examples/craft-anything-v2-916.json` · sha256:bcec22b2cea3 · sujo
- `examples/craft-anything-v2.json` · sha256:666a5c7a80e2 · sujo
- `examples/craft-anything.json` · sha256:9b853ae8f8b1 · sujo
- `examples/csm-a1-v2.json` · sha256:79f5be7a983a · sujo
- `examples/csm-a1.json` · sha256:6e94ee938289 · sujo
- `examples/csm-a2-v2.json` · sha256:e3a874ce18e4 · sujo
- `examples/csm-a2.json` · sha256:4c238de76063 · sujo
- `examples/csm-a3-v2.json` · sha256:eff2c2d11dea · sujo
- `examples/csm-a3.json` · sha256:683bccf051bd · sujo
- `examples/csm-a4-v2.json` · sha256:808e25435339 · sujo
- `examples/csm-a4.json` · sha256:8b1e8a863de6 · sujo
- `examples/csm-a5-v2.json` · sha256:bec2a40d2068 · sujo
- `examples/csm-a5.json` · sha256:0748302f8bd0 · sujo
- `examples/csm-a6-v2.json` · sha256:b8253af48c0a · sujo
- `examples/csm-a6.json` · sha256:c4a6be50155f · sujo
- `examples/csm-a7-v2.json` · sha256:2434205d6321 · sujo
- `examples/csm-a7.json` · sha256:32d7e2086d43 · sujo
- `examples/csm-visao-v2.json` · sha256:4a19eb7474e6 · sujo
- `examples/csm-visao.json` · sha256:47e22b8195b4 · sujo
- `examples/decisions-jev-en-v2.json` · sha256:8ecb238e4653 · sujo
- `examples/decisions-jev-en.json` · sha256:676529ccb25d · sujo
- `examples/decisions-jev-es-v2.json` · sha256:f193bb3d2c2b · sujo
- `examples/decisions-jev-es.json` · sha256:84c618d6a478 · sujo
- `examples/decisions-jev-v2.json` · sha256:74806bcc1a3c · sujo
- `examples/decisions-jev.json` · sha256:5d3863296f9a · sujo
- `examples/deepseek-ia-hacker-v2-916.json` · sha256:1bd95abe02cd · sujo
- `examples/deepseek-ia-hacker-v2.json` · sha256:485a395b9cab · sujo
- `examples/deepseek-ia-hacker.json` · sha256:215e8d604fe5 · sujo
- `examples/devia62-m1-v2.json` · sha256:95aac03bab69 · sujo
- `examples/devia62-m1.json` · sha256:0fb26b5bad2c · sujo
- `examples/diga-o-que-importa-v2.json` · sha256:3a990601df58 · sujo
- `examples/diga-o-que-importa.json` · sha256:b30efd31b1c1 · sujo
- `examples/diga-v1-v2.json` · sha256:06de6e73d08e · sujo
- `examples/diga-v1.json` · sha256:231e9ddc6b1e · sujo
- `examples/empresa-chatgpt-v2.json` · sha256:a3f2a10c35f2 · sujo
- `examples/empresa-chatgpt.json` · sha256:feb75593f9c1 · sujo
- `examples/empresas-2027-en-v2.json` · sha256:324c3a9d1ce0 · sujo
- `examples/empresas-2027-en.json` · sha256:908f12e38fb4 · sujo
- `examples/empresas-2027-es-v2.json` · sha256:7b221127a6b4 · sujo
- `examples/empresas-2027-es.json` · sha256:9ae4854d5505 · sujo
- `examples/empresas-2027-v2.json` · sha256:1a682c49638b · sujo
- `examples/empresas-2027.json` · sha256:e4f1d8b77e9e · sujo
- `examples/emudhra-chave-4-v2.json` · sha256:4c0ff49dc558 · sujo
- `examples/emudhra-chave-4.json` · sha256:9d74ea643f0d · sujo
- `examples/escada-ia-carro-voador-v2.json` · sha256:75c18018f32f · sujo
- `examples/escada-ia-carro-voador.json` · sha256:6641990d7a5d · sujo
- `examples/esforco-fable-testes-v2-916.json` · sha256:80169187d862 · sujo
- `examples/esforco-fable-testes-v2.json` · sha256:0141f3d16666 · sujo
- `examples/esforco-fable-testes.json` · sha256:1e52d324e40f · sujo
- `examples/execucao-longa-pratica-v2.json` · sha256:6ece5cd6235b · sujo
- `examples/execucao-longa-pratica.json` · sha256:53615a8ca489 · sujo
- `examples/fable-opus-esforco-v2-916.json` · sha256:65953e4da967 · sujo
- `examples/fable-opus-esforco-v2.json` · sha256:fc0045bf116f · sujo
- `examples/fable-opus-esforco.json` · sha256:1af5b62e02de · sujo
- `examples/faxina-agentes-v2.json` · sha256:067c4fb48293 · sujo
- `examples/faxina-agentes.json` · sha256:1d22366b8e86 · sujo
- `examples/filme-em-codigo-lia-v2.json` · sha256:59b13ef968be · sujo
- `examples/filme-em-codigo-lia.json` · sha256:27c20d0a76e6 · sujo
- `examples/filme-por-conversa-v2.json` · sha256:9380f8ea7918 · sujo
- `examples/filme-por-conversa-viral-v2.json` · sha256:f6a0cb254a04 · sujo
- `examples/filme-por-conversa.json` · sha256:575284339684 · sujo
- `examples/fim-capitalismo-v2.json` · sha256:a0b54e1d5dd1 · sujo
- `examples/fim-capitalismo.json` · sha256:acef6679f896 · sujo
- `examples/fim-dos-agentes-v2-916.json` · sha256:8110479f1ec1 · sujo
- `examples/fim-dos-agentes-v2.json` · sha256:5f03948d0857 · sujo
- `examples/fim-dos-agentes.json` · sha256:ad95f0351db5 · sujo
- `examples/fim-mundo-1960-v2-916.json` · sha256:1a46781eec35 · sujo
- `examples/fim-mundo-1960-v2.json` · sha256:c5ba8e7b9aef · sujo
- `examples/fim-mundo-1960.json` · sha256:18d8d71dc026 · sujo
- `examples/form-gestao-v2.json` · sha256:143cc45600dd · sujo
- `examples/form-gestao.json` · sha256:6f7f6b54d880 · sujo
- `examples/form-loopr-v2.json` · sha256:488201c9f6ef · sujo
- `examples/form-loopr.json` · sha256:b31203efc0e9 · sujo
- `examples/form-prof2030-v2.json` · sha256:76ab9a045c6f · sujo
- `examples/form-prof2030.json` · sha256:c25dbad58cb0 · sujo
- `examples/form-seo-v2.json` · sha256:7ca2f25a8930 · sujo
- `examples/form-seo.json` · sha256:19f3bf532401 · sujo
- `examples/form-vendas-v2.json` · sha256:d2c7bb91a2aa · sujo
- `examples/form-vendas.json` · sha256:d75f11f41253 · sujo
- `examples/gates-sofrer-2027-v2-916.json` · sha256:1452b3c98e95 · sujo
- `examples/gates-sofrer-2027-v2.json` · sha256:a52d05546ed2 · sujo
- `examples/gates-sofrer-2027.json` · sha256:1842dccd8e66 · sujo
- `examples/gerente-de-agentes-en-v2.json` · sha256:ba9d00d8c13a · sujo
- `examples/gerente-de-agentes-en.json` · sha256:1291208e45a3 · sujo
- `examples/gerente-de-agentes-es-v2.json` · sha256:4ca686706cc4 · sujo
- `examples/gerente-de-agentes-es.json` · sha256:6526a599d511 · sujo
- `examples/gestao-ia-caminhos-en-v2.json` · sha256:6177c0beaf3e · sujo
- `examples/gestao-ia-caminhos-en.json` · sha256:e14b05d9c0d7 · sujo
- `examples/gestao-ia-caminhos-es-v2.json` · sha256:09ec9a427a69 · sujo
<!-- handoff-estado:fim -->
