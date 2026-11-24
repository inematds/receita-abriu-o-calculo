# Handoff — 2026-11-24 — receita-abriu-o-calculo: guia corrigido, vídeo lives1 na cadeia, 4 reels rtex da calculadora em produção

## Projeto e escopo
~/projetos/receita-abriu-o-calculo (guia PT/EN/ES). Também ~/projetos/rtex. Pedido do Nei 24/11: "quero 4 videos rtex no lives1,3,4,8 falando da calculadora", gancho "será que vc vai vender por 56 ou 72 o teu produto", imagem das duas notas, capa provocante com cara de apavorado e a nota, ~30 s, "manda eles para o v3"; CTA "o kit ta no inema.club so baixar"; pergunta "você já calculou quanto vão sair os produtos a partir de janeiro".

## Objetivo atual
4 reels rtex prontos no v3 e na fila de lives1/3/4/8. Explicavideo lives1 pelo vigia continua.

## Estado aceito
- [confirmed] Guia com banners e personagens no ar — evidência: commit 240830a
- [confirmed] rtex aceita duracao_alvo por roteiro — evidência: commit 4fe0158 (rtex); teste dur_alvo → (25,40)/(60,90)
- [confirmed] Fichas rodando — evidência: unit rtex-calculadora-fichas; ~/projetos/rtex/producao/pedidos-calculadora/fichas.log

## Proposto / tentado, não confirmado
- [unverified] Fichas passam no checar/crítico com 30 s — a estrutura rtex tem muitos blocos; ver <canal>.log

## Decisões
- Fichas rodadas por roda-fichas.sh (prompt do bot) e entregues ao timer rtex-producao, que faz avatar → montagem → revisor → v3 + fila.
- Ângulos: lives1 quem vende; lives3 quem compra; lives4 sistema de notas; lives8 contador/pequeno empresário.

## Não fazer (restrições e travas)
- Números só do FATOS.md; nunca dizer que 8,8% ou 11,3% é a alíquota — fonte: ~/projetos/explicavideos/textos/receita-abriu-o-calculo/FATOS.md
- Sem logo da Receita/governo/GitHub — fonte: CLAUDE.md
- Nunca "comenta PALAVRA" — fonte: ~/projetos/rtex/producao/pedidos-calculadora/lives1.txt
- Não reenviar avatar ao HeyGen; não trocar plano — fonte: ~/.claude/CLAUDE.md

## Arquivos alterados
- Fora: `~/projetos/rtex/rtex.py` (dur_alvo), `~/projetos/rtex/producao/pedidos-calculadora/` (4 pedidos + roda-fichas.sh)
- Fora: `~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/CONTINUAR.md`

## Memória e regras duráveis tocadas
- nenhuma nesta etapa

## Verificação
- Rodado: bash -n roda-fichas.sh → ok; teste dur_alvo → ok
- Não rodado: suíte de testes do rtex — mudança pequena e isolada

## Estado em execução
- Processos: unit `rtex-calculadora-fichas` (4 fichas em série, ao fim avisa no v3); unit `ev-receita-abriu-lives1` (explicavideo); vigia continua receita-abriu-lives1

## Perguntas abertas e adiados
- nenhuma

## Pela metade
- 4 reels — parou em: ficha lives1 — falta: fichas 3/4/8 e produção pelo timer

## Próxima ação exata
Conferir `~/projetos/rtex/producao/pedidos-calculadora/fichas.log` e `python3 ~/projetos/rtex/producao/producao.py --status`; ficha com ERRO → ler <canal>.log, corrigir o pedido, apagar nada e rodar o roda-fichas.sh de novo (pula as feitas).

## Mapa de retomada
- `~/projetos/rtex/producao/pedidos-calculadora/fichas.log` — estado das fichas
- `~/projetos/rtex/producao/pedidos-calculadora/lives1.txt` — pedido
- `~/projetos/explicavideos/textos/receita-abriu-o-calculo-lives1/CONTINUAR.md` — vídeo lives1

## Perguntas-teste
1. Tarefa atual? → 4 reels rtex lives1/3/4/8 — fonte: ~/projetos/rtex/producao/pedidos-calculadora/roda-fichas.sh — chave: `lives8`
2. Última decisão? → duracao_alvo [25,40] no roteiro — fonte: commit 4fe0158 — chave: `duracao_alvo`
3. O que não pode mudar? → nunca dizer que a alíquota é 8,8% ou 11,3% — fonte: FATOS.md — chave: `alíquota`
4. Pela metade? → fichas em série — fonte: fichas.log — chave: `ficha`
5. Próxima ação? → conferir fichas.log e producao --status — fonte: fichas.log — chave: `status`

## Checagem de compartilhamento
- Sem segredos, tokens ou dados pessoais: sim


<!-- handoff-estado:inicio -->
## Estado gravado pelo script (não editar)

Gravado por handoff-grava.py no momento do handoff. `--conferir` compara com o projeto agora.

- commit: 6395f39017a4fec4d81840142eb14f8077b05fe4 · branch: main
- arquivos sujos fora de handoffs/: 0

### Repo do trabalho: /home/nmaldaner/projetos/rtex
- commit: 4fe0158ae0b292baf1c59078257b3bf2eb6baba6 · branch: main
- arquivos sujos: 105
- impressão de todos os sujos: b3a46402cce2a5cf
- `FALHAS.md` · sha256:bc87e048d614 · sujo
- `edicoes/2026-11-01-comece-por-tres/critica.json` · sha256:81ef333fffa7 · sujo
- `edicoes/2026-11-01-comece-por-tres/metritds-texto.txt` · sha256:64e16a262d1e · sujo
- `edicoes/2026-11-01-comece-por-tres/roteiro.json` · sha256:17ea212cfa20 · sujo
- `edicoes/2026-11-01-prospeccao-por-sinal/critica.json` · sha256:ca1188615ec0 · sujo
- `edicoes/2026-11-01-prospeccao-por-sinal/metritds-texto.txt` · sha256:d8313a98f0b0 · sujo
- `edicoes/2026-11-01-prospeccao-por-sinal/roteiro.json` · sha256:b67548588910 · sujo
- `edicoes/2026-11-04-claude-code-2/critica.json` · sha256:1b99d5eb2e4d · sujo
- `edicoes/2026-11-04-claude-code-2/metritds.txt` · sha256:7ecc5205224a · sujo
- `edicoes/2026-11-04-claude-code-2/roteiro.json` · sha256:4ddd11470cf0 · sujo
- `edicoes/2026-11-04-claude-escritorio/critica.json` · sha256:2302efb0570c · sujo
- `edicoes/2026-11-04-claude-escritorio/metritds-texto.txt` · sha256:e93b08e89444 · sujo
- `edicoes/2026-11-04-claude-escritorio/roteiro.json` · sha256:0bc9be93a62f · sujo
- `edicoes/2026-11-04-jarvis-local/CONTINUAR.md` · sha256:10ab3725a500 · sujo
- `edicoes/2026-11-04-jarvis-local/CONTINUAR.resultado` · sha256:806563799da1 · sujo
- `edicoes/2026-11-04-jarvis-local/critica.json` · sha256:2549dfac49ba · sujo
- `edicoes/2026-11-04-jarvis-local/metritds-texto.txt` · sha256:baaf2f11d003 · sujo
- `edicoes/2026-11-04-jarvis-local/metritds.txt` · sha256:87909a6c9b65 · sujo
- `edicoes/2026-11-04-jarvis-local/roteiro.json` · sha256:1e04c6436795 · sujo
- `edicoes/2026-11-04-openduet/CONTINUAR.md` · sha256:bf1f1a92f76a · sujo
- `edicoes/2026-11-04-openduet/CONTINUAR.resultado` · sha256:90663999d4be · sujo
- `edicoes/2026-11-04-openduet/capa-azul.jpg` · sha256:695b1ba53193 · sujo
- `edicoes/2026-11-04-openduet/critica.json` · sha256:53e5db8a588d · sujo
- `edicoes/2026-11-04-openduet/metritds-texto.txt` · sha256:0f31b85af343 · sujo
- `edicoes/2026-11-04-openduet/metritds.txt` · sha256:ab869f2c7a59 · sujo
- `edicoes/2026-11-04-openduet/roteiro.json` · sha256:e41046409375 · sujo
- `edicoes/2026-11-04-openduet/video.jpg` · sha256:6551e87627b5 · sujo
- `edicoes/2026-11-07-curiosidade-viral/critica.json` · sha256:219c0b3f67fb · sujo
- `edicoes/2026-11-07-curiosidade-viral/roteiro.json` · sha256:1fa8977bc08b · sujo
- `edicoes/2026-11-08-kit-design-ia/DECISAO-EDITORIAL.md` · sha256:79c6450c64c3 · sujo
- `edicoes/2026-11-08-kit-design-ia/PUBLICACAO-PENDENTE.md` · sha256:92930e0c1b35 · sujo
- `edicoes/2026-11-08-kit-design-ia/critica.json` · sha256:d776b8b32c32 · sujo
- `edicoes/2026-11-08-kit-design-ia/roteiro.json` · sha256:15044f83cab2 · sujo
- `edicoes/2026-11-11-esforco-ou-produto/critica.json` · sha256:f07968b39306 · sujo
- `edicoes/2026-11-11-esforco-ou-produto/roteiro.json` · sha256:4ca6cc992388 · sujo
- `edicoes/2026-11-12-ia-acelerando/critica.json` · sha256:dac6e4e1b1f3 · sujo
- `edicoes/2026-11-12-ia-acelerando/roteiro.json` · sha256:ea8ec6344370 · sujo
- `edicoes/2026-11-12-nivel-escada/critica.json` · sha256:48047422d3e8 · sujo
- `edicoes/2026-11-12-nivel-escada/roteiro.json` · sha256:5091ba5b8460 · sujo
- `edicoes/2026-11-17-astra-placar/CONTINUAR.md` · sha256:badec8af7629 · sujo
- `edicoes/2026-11-17-astra-placar/CONTINUAR.resultado` · sha256:566ef00c92c2 · sujo
- `edicoes/2026-11-17-astra-placar/capa/abertura.codex.json` · sha256:511716814456 · sujo
- `edicoes/2026-11-17-astra-placar/capa/abertura.png` · sha256:2e846c15ab3e · sujo
- `edicoes/2026-11-17-astra-placar/capa/codex.log` · sha256:743ab4b9ef73 · sujo
- `edicoes/2026-11-17-astra-placar/capa/pedido.txt` · sha256:90ea8e4c40f5 · sujo
- `edicoes/2026-11-17-astra-placar/conferencia-telegram.json` · sha256:6149f04563fd · sujo
- `edicoes/2026-11-17-astra-placar/critica.json` · sha256:28c40f951c8d · sujo
- `edicoes/2026-11-17-astra-placar/plano.json` · sha256:72d1225337f3 · sujo
- `edicoes/2026-11-17-astra-placar/recibo-inemaytbot.json` · sha256:e38e74ea9e06 · sujo
- `edicoes/2026-11-17-astra-placar/roteiro.json` · sha256:aafe4c19e4e9 · sujo
- `edicoes/2026-11-17-astra-placar/youtube-id.txt` · sha256:a25db36490d0 · sujo
- `edicoes/2026-11-17-escada-da-ia/capa/abertura.codex.json` · sha256:31eae3b38301 · sujo
- `edicoes/2026-11-17-escada-da-ia/capa/abertura.png` · sha256:79f9dc6a27b0 · sujo
- `edicoes/2026-11-17-escada-da-ia/capa/codex.log` · sha256:38ea8d464082 · sujo
- `edicoes/2026-11-17-escada-da-ia/capa/pedido.txt` · sha256:f30f97a6a8ff · sujo
- `edicoes/2026-11-17-escada-da-ia/critica.json` · sha256:9f02c87c609e · sujo
- `edicoes/2026-11-17-escada-da-ia/roteiro.json` · sha256:5d1828ef7861 · sujo
- `edicoes/2026-11-17-fora-do-volante-v2/critica.json` · sha256:ed19b441fbbb · sujo
- `edicoes/2026-11-17-fora-do-volante-v2/roteiro.json` · sha256:f0ed97e509d1 · sujo
- `edicoes/2026-11-17-fora-do-volante/capa/abertura.codex.json` · sha256:a1ce50126487 · sujo
- `edicoes/2026-11-17-fora-do-volante/capa/abertura.png` · sha256:cb3be22ae1e7 · sujo
- `edicoes/2026-11-17-fora-do-volante/capa/codex.log` · sha256:ddf5cea1523b · sujo
- `edicoes/2026-11-17-fora-do-volante/capa/pedido.txt` · sha256:9318c52d2774 · sujo
- `edicoes/2026-11-17-fora-do-volante/critica.json` · sha256:ece8aae599c2 · sujo
- `edicoes/2026-11-17-fora-do-volante/roteiro.json` · sha256:7913c21ad41b · sujo
- `edicoes/2026-11-18-era-dos-conceitos/capa/abertura.codex.json` · sha256:2b1615934d7f · sujo
- `edicoes/2026-11-18-era-dos-conceitos/capa/abertura.png` · sha256:3589020035cf · sujo
- `edicoes/2026-11-18-era-dos-conceitos/capa/codex.log` · sha256:7af9f73762a8 · sujo
- `edicoes/2026-11-18-era-dos-conceitos/capa/pedido.txt` · sha256:1dee3d1bceec · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/capa/abertura.codex.json` · sha256:a088400edd82 · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/capa/abertura.png` · sha256:dd3702ad1c8b · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/capa/codex.log` · sha256:f2923b1663cf · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/capa/pedido.txt` · sha256:2c9e5194a324 · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/chamada-candidatas.md` · sha256:83abbd6218bf · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/critica-rodadas/roteiro-1.json` · sha256:1e45e64c87fe · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/critica.json` · sha256:2a6376eca125 · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/criticas.jsonl` · sha256:76bbd63453b0 · sujo
- `edicoes/2026-11-19-fim-do-capitalismo/roteiro.json` · sha256:be50ae16b9bb · sujo
- `edicoes/2026-11-22-compacta-400k/CONTINUAR.md` · sha256:f21c11979e6d · sujo
- `edicoes/2026-11-22-compacta-400k/CONTINUAR.resultado` · sha256:5c89529607ee · sujo
- `edicoes/2026-11-22-compacta-400k/capa/abertura.codex.json` · sha256:38b07918614a · sujo
- `edicoes/2026-11-22-compacta-400k/capa/abertura.png` · sha256:67ee6805bef9 · sujo
- `edicoes/2026-11-22-compacta-400k/capa/codex.log` · sha256:dd6d9496c7ac · sujo
- `edicoes/2026-11-22-compacta-400k/capa/pedido.txt` · sha256:04e227144744 · sujo
- `edicoes/2026-11-22-compacta-400k/chamada-candidatas.md` · sha256:39028174b78e · sujo
- `edicoes/2026-11-22-compacta-400k/critica-rodadas/roteiro-1.json` · sha256:13a6001e73af · sujo
- `edicoes/2026-11-22-compacta-400k/critica-rodadas/roteiro-2.json` · sha256:e36854fe7f63 · sujo
- `edicoes/2026-11-22-compacta-400k/critica.json` · sha256:1f3a1036e232 · sujo
- `edicoes/2026-11-22-compacta-400k/criticas.jsonl` · sha256:cfee9cb0df72 · sujo
- `edicoes/2026-11-22-compacta-400k/qa.md` · sha256:761f9d876f0f · sujo
- `edicoes/2026-11-22-compacta-400k/roteiro.json` · sha256:9732376bcb97 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/capa/abertura.codex.json` · sha256:e27373c4cb67 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/capa/abertura.png` · sha256:03b2bf558505 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/capa/codex.log` · sha256:19ac587373d1 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/capa/pedido.txt` · sha256:6c889eb56633 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/chamada-candidatas.md` · sha256:34e41d75923c · sujo
- `edicoes/2026-11-22-vende-empresa-ia/critica-rodadas/roteiro-1.json` · sha256:70499afad4b3 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/critica-rodadas/roteiro-2.json` · sha256:f78ec3d5c34e · sujo
- `edicoes/2026-11-22-vende-empresa-ia/critica.json` · sha256:73e8374c0af9 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/criticas.jsonl` · sha256:381003eef929 · sujo
- `edicoes/2026-11-22-vende-empresa-ia/roteiro.json` · sha256:f78ec3d5c34e · sujo
- `producao/pedidos-calculadora/fichas.log` · sha256:d20d2cde3487 · sujo
- `producao/pedidos-calculadora/lives1.log` · sha256:539289dc47d0 · sujo
- `producao/pedidos-calculadora/lives1.prompt` · sha256:d94d98705dd8 · sujo
- `producao/pedidos-calculadora/roda-fichas.sh` · sha256:1657d453ded8 · sujo

### Repo do trabalho: /home/nmaldaner/projetos/explicavideos
- commit: 53466f36ea02dfc7305c719a271efaffdef8c3da · branch: main
- arquivos sujos: 428 (lista cortada)
- impressão de todos os sujos: 6171796938216df4
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
