# Publicação e limpeza

Publicação permanece bloqueada. A chave do workflow de publicação recebeu HTTP403
na execução 40002569961. Testada alternativa OIDC pelo verify-auth existente:
execução 40005481450 falhou com HTTP401, sem trust policy correspondente para
hugodeco. Não foi repetida publicação com a mesma credencial inválida.
Cofres pessoal e compartilhado global acessíveis não possuem entrada NuGet.
Necessário autorizar chave para Sufficit.Telephony.Panel.Core ou configurar policy
para sufficit/sufficit-telephony-panel-core, workflow publish.yml, creator hugodeco.

Removidas sem force as 11 worktrees desta migração, após verificar árvore limpa,
HEAD ancestral de origin/main e ausência de processo com cwd dentro da worktree.
Ausência confirmada no disco e no git worktree list. Worktrees de outras tarefas
preservadas. Branches preservados; não houve alteração nas fontes/pacotes.

- /mnt/sufficit/sufficit-efdata/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-standard/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-statistics/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-ami-events/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-ari/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-telephony-panel/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-endpoints/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-web/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-project-management/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-services-openclaw/.worktrees/panel-core-main
- /mnt/sufficit/sufficit-telephony-panel-core/.worktrees/panel-core-merge-record
