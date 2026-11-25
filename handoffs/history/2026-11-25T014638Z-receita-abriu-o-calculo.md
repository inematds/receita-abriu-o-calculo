# Handoff — 2026-11-24 — guia: exemplo de janeiro + bloco preço e contador com imagem

## Projeto e escopo
~/projetos/receita-abriu-o-calculo (guia PT/EN/ES em guia/). O Nei pediu um exemplo de janeiro com uma nota de mercado real dele (121 itens) rodada no programa da Receita, e depois os blocos "o que muda no preço" e "para o contador", com uma imagem de impacto. Medições no repo ~/projetos/calculadora-da-reforma (kit/MEDICOES.md, kit/exemplos/).

## Objetivo atual
Os blocos #janeiro e #preco estão no ar nos 3 idiomas. Pronto = guia ao vivo com id="preco" em PT/EN/ES e as imagens respondendo 200.

## Estado aceito
- [confirmed] Seção #janeiro (nota real, CBS R$ 89,14 com 8,8% e R$ 114,30 com 11,3%) — evidência: commit bc4edb9
- [confirmed] Seção #preco (linha do tempo do preço, margem sobre custo sem imposto, 3 armadilhas, Simples) com imagem `kit/preco-contador.html` → guia/assets/preco-contador*.jpg — evidência: commit 7fcccd6
- [confirmed] O Pages passou a sair do branch main (/, legacy), e o workflow "Deploy static site to Pages" foi desligado — evidência: commit e417254 (FALHAS.md) e `gh workflow list --all` → disabled_manually

## Proposto / tentado, não confirmado
- nenhum

## Decisões
- A imagem é HTML renderizado pelo chrome-headless-shell (números exatos), não o Codex — motivo: os números vêm da medição.
- O Pages sai do branch porque o Actions falhou 5× com "Fetching artifact metadata failed".

## Não fazer (restrições e travas)
- Nunca dizer que 8,8% ou 11,3% é a alíquota de 2027 — fonte: guia/index.html #janeiro
- Nunca publicar o CPF, a chave de acesso, o QR, o operador ou o CNPJ da nota; as fotos originais ficam fora do repo — dito pelo usuário em 24/11, só nesta conversa
- Não dizer "custa a mais"; a CBS substitui o PIS e a Cofins — fonte: guia/index.html #janeiro
- Tradução só pelo inema-traduz; o autor dos commits é inematds — fonte: ~/.claude/CLAUDE.md

## Arquivos alterados
- `guia/index.html`, `guia/en/index.html`, `guia/es/index.html` — seções #janeiro e #preco + nav
- `kit/nota-janeiro.html`, `kit/preco-contador.html` — fontes das imagens (?lang=, ?v=1)
- `guia/assets/` — nota-hoje, nota-janeiro*, preco-contador* (jpg)
- `FALHAS.md` — 3 linhas de deploy
- Fora do projeto: ~/projetos/calculadora-da-reforma/kit/MEDICOES.md e kit/exemplos/supermercado-janeiro-* (commit 69644df)

## Memória e regras duráveis tocadas
- nenhuma (só FALHAS.md do projeto)

## Verificação
- Rodado: curl no guia PT/EN/ES → id="preco" 1/1/1; assets preco-contador*.jpg → 200
- Rodado: Pages build legacy → built
- Não rodado: revisor independente nos blocos novos — não pedido

## Estado em execução
- Processos em segundo plano: nenhum (motores da Receita derrubados)
- Servidores / portas: nenhum
- Worktrees / branches abertos: nenhum

## Perguntas abertas e adiados
- Aberta: reels/vídeo com a nota (R$ 89,14 ou R$ 114,30)? — sem resposta do Nei

## Pela metade
- nada

## Próxima ação exata
Esperar o Nei. Se ele pedir os reels ou o vídeo, usar as imagens de guia/assets como base; a publicação segue as regras do canal.

## Mapa de retomada
- `guia/index.html` — seções #janeiro e #preco
- `kit/preco-contador.html` — fonte da imagem nova
- `FALHAS.md` — por que o Pages sai do branch

## Perguntas-teste
1. Qual é a tarefa atual e o critério de pronto? → blocos #janeiro e #preco no ar em PT/EN/ES — fonte: commit 7fcccd6 — chave: `preco`
2. Qual foi a última decisão e por quê? → o Pages passou a sair do branch main, porque o Actions falhava — fonte: FALHAS.md — chave: `branch`
3. O que não pode mudar? → não chamar 8,8%/11,3% de alíquota de 2027 — fonte: guia/index.html — chave: `alíquota`
4. O que está pela metade? → nada — fonte: commit e417254 — chave: `nada`
5. Qual é a próxima ação, por quê, e ela precisa de aprovação? → esperar a resposta sobre os reels; precisa do Nei — fonte: só nesta conversa — chave: `reels`

## Checagem de compartilhamento
- Sem segredos nem dados pessoais: sim (os dados da nota foram omitidos)


<!-- handoff-estado:inicio -->
## Estado gravado pelo script (não editar)

Gravado por handoff-grava.py no momento do handoff. `--conferir` compara com o projeto agora.

- commit: e417254c772eeea71d1a0e63c5f5caf990f7e0ce · branch: main
- arquivos sujos fora de handoffs/: 0
- `kit/preco-contador.html` · sha256:904bdbbb5324 · citado
- `guia/index.html` · sha256:8e609d3c7199 · citado
- `guia/en/index.html` · sha256:0bba7c78b231 · citado
- `guia/es/index.html` · sha256:22ebba729805 · citado
- `kit/nota-janeiro.html` · sha256:8194f4af56e9 · citado
- `FALHAS.md` · sha256:88a010ddafae · citado
<!-- handoff-estado:fim -->
