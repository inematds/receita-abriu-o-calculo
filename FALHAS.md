# FALHAS — receita-abriu-o-calculo

| data | o que quebrou | menor correção | prompt \| infra |
|---|---|---|---|
| 2026-11-24 | exemplo de janeiro: deploy do Pages falhou 3× seguidas (push, rerun e workflow_dispatch) com "Fetching artifact metadata failed", só neste repo (o calculadora-da-reforma, mesmo workflow, passou no mesmo minuto) | esperar e disparar de novo; se continuar, trocar o Pages para "deploy from branch" (main, /) | infra |
| 2026-11-24 | deploy do Pages falhou de novo ("Fetching artifact metadata failed"), já com upload-pages-artifact v4: instabilidade do GitHub | `gh run rerun <id>` uma vez; conferir o conteúdo no ar, não só o 200 | infra |
| 2026-11-24 | 1º deploy do Pages falhou ("No artifacts named github-pages") porque o push rodou o workflow antes de ligar o Pages (build_type=workflow) | ligar o Pages (gh api .../pages -f build_type=workflow) ANTES do 1º push, ou rodar o workflow de novo | infra |
