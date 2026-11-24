# Handoff — 2026-11-24 — receita-abriu-o-calculo: exemplo de janeiro com nota de supermercado real

## Projeto e escopo
~/projetos/receita-abriu-o-calculo (guia PT/EN/ES) e ~/projetos/calculadora-da-reforma (kit). Pedido do Nei 24/11: "baixe estas imagens e quero que aplique exemplo de como será em janeiro" (4 fotos de uma NFC-e real dele, 06/11/2026, supermercado de Canela/RS, 121 itens, R$ 1.512,15).

## Objetivo atual
Seção #janeiro no guia, feita e no ar. Depois disso o Nei só fez perguntas: (1) quando vem o custo a mais e se o comerciante põe margem; (2) se para o contador é fácil ou trabalhoso. As duas foram respondidas no chat, e para cada uma ofereci um bloco novo no guia, sem resposta dele ainda.

## Estado aceito
- [confirmed] Seção #janeiro + link no menu nas 3 páginas, imagens nota-janeiro(-vertical)(-en|-es).jpg e nota-hoje.jpg — evidência: commit bc4edb9; conferido no ar (id="janeiro" e 89,14 nas 3 línguas, assets 200)
- [confirmed] Medição no kit — evidência: calculadora-da-reforma commit 69644df (MEDICOES.md + kit/exemplos/*supermercado*)
- [confirmed] Números (motor regime regular 1.7.2, 15/01/2027, Canela 4304408, 121 itens CALCULO_SIMULADO): cesta 396,04→0; red. 60% 173,74→6,13/7,87; cheia 942,37→83,01/106,43; CBS total 89,14 (8,8%) / 114,30 (11,3%); IBS 0,70
- [confirmed] FALHAS.md: Pages falhou 3× ("Fetching artifact metadata failed"), 4ª execução passou

## Proposto / tentado, não confirmado
- [unverified] Bloco "O que fica mais caro e o que não muda" (cesta igual, óleo de soja passa a ter CBS, margem sobre imposto) — só oferecido
- [unverified] Bloco "Para o contador: o que dá trabalho" (classificação de produtos com as 3 armadilhas da nota, transição 2027–2032, opção do Simples, preço) — só oferecido
- [unverified] Reels/vídeo com essa nota — só oferecido

## Decisões
- Classificação do INEMA conferida no texto dos anexos da base do motor; milho/ervilha em conserva e batata palha = alíquota cheia (Anexo VII item 16 exige sem sal); pão de alho e gelatina = cheia (Anexo I só pão francês/fórmula infantil); frango NCM 02071411/02071412 (02071400 não existe em 2027).
- Foto publicada só com o trecho dos itens (sem cabeçalho da loja, CPF, QR, chave); originais não vão ao repo.
- Imagem feita de `kit/nota-janeiro.html` por screenshot (chrome-headless-shell do ms-playwright 1254), nunca por gerador.

## Não fazer (restrições e travas)
- Não chamar 89,14/114,30 de "custo a mais": a CBS substitui PIS/Cofins já embutidos — fonte: FATOS.md do explicavideos
- Nunca dizer que a alíquota é 8,8% ou 11,3% — fonte: FATOS.md
- Não publicar CPF, nome da loja ou CNPJ da nota do Nei — fonte: decisão desta sessão
- Sem logo da Receita em imagem gerada — fonte: CLAUDE.md do projeto

## Arquivos alterados
- `guia/index.html`, `guia/en/index.html`, `guia/es/index.html`, guia/assets/nota-*.jpg, `kit/nota-janeiro.html`, `FALHAS.md`
- Fora: ~/projetos/calculadora-da-reforma/kit/MEDICOES.md e kit/exemplos/ (operacao/resposta-supermercado-janeiro-*, supermercado-janeiro-itens.py, supermercado-janeiro-roda.py)

## Memória e regras duráveis tocadas
- nenhuma

## Verificação
- Rodado: soma das 121 linhas = 1.512,15; motor 121/121 CALCULO_SIMULADO nas duas alíquotas; conteúdo no ar conferido nas 3 línguas
- Não rodado: revisor independente da seção nova

## Estado em execução
- Nenhum processo; motores desligados.

## Perguntas abertas e adiados
- Nei: fazer os blocos "o que fica mais caro" e/ou "para o contador" no guia? Fazer reels/vídeo com a nota?

## Pela metade
- nada

## Próxima ação exata
Esperar a resposta do Nei aos blocos oferecidos; para refazer a conta: subir os motores com kit/scripts/subir-calculadoras.sh da calculadora (JAVA_HOME=~/.local/jdk25/jdk-25.0.5.1+2, portas 8180/8182/8190) e rodar kit/exemplos/supermercado-janeiro-roda.py.

## Mapa de retomada
- ~/projetos/calculadora-da-reforma/kit/MEDICOES.md — números e armadilhas
- `guia/index.html` (#janeiro) — seção publicada
- `kit/nota-janeiro.html` — fonte da imagem

## Perguntas-teste
1. Tarefa atual? → exemplo de janeiro com nota real — fonte: commit bc4edb9 — chave: `janeiro`
2. Última decisão? → conservas com sal na alíquota cheia — fonte: MEDICOES.md — chave: `sem sal`
3. O que não pode mudar? → não chamar a CBS de custo a mais — fonte: FATOS.md — chave: `no lugar do PIS`
4. Pela metade? → nada; blocos oferecidos aguardam o Nei — fonte: este handoff — chave: `contador`
5. Próxima ação? → esperar resposta do Nei — fonte: este handoff — chave: `Sua resposta`

## Checagem de compartilhamento
- Sem segredos, tokens ou dados pessoais: sim


<!-- handoff-estado:inicio -->
## Estado gravado pelo script (não editar)

Gravado por handoff-grava.py no momento do handoff. `--conferir` compara com o projeto agora.

- commit: 88db15c92b34f183d94d49c40a234b53105890da · branch: main
- arquivos sujos fora de handoffs/: 0
- `kit/nota-janeiro.html` · sha256:8194f4af56e9 · citado
- `guia/index.html` · sha256:5c65deaf762d · citado
- `guia/en/index.html` · sha256:18c1057ff6fe · citado
- `guia/es/index.html` · sha256:9b70e3da7e06 · citado
- `FALHAS.md` · sha256:824bfe7dd99c · citado

### Repo do trabalho: /home/nmaldaner/projetos/calculadora-da-reforma
- commit: 69644df0ca8181a3d8f3108fba842672d4b728f9 · branch: main
- arquivos sujos: 0
- impressão de todos os sujos: e3b0c44298fc1c14
<!-- handoff-estado:fim -->
