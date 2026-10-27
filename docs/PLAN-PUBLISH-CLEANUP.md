# Publicar Panel Core e limpar worktrees
1. CONCLUÍDO — Verificar política salva, adaptar publicação para OIDC e publicar pacote.
2. CONCLUÍDO — Remover as 11 worktrees integradas e limpas da migração.
3. PENDENTE (indexação pública do NuGet após upload aceito) — Confirmar pacote disponível no NuGet, registrar entrega e limpar worktree da publicação.
Não expor segredos. Usuário confirmou política salva e autorizou publicar.
Validação: verify-auth, workflow publish, download do nupkg e inspeção de assembly/targets.

Após confirmação de política salva: verify-auth 40015177055 falhou em 2026-10-23 19:55 UTC com HTTP401: nenhuma trust policy correspondente pertencente a hugodeco. Necessário confirmar usuário NuGet criador e vínculo exato repository/workflow. Publicação não executada sem autenticação.

Comparação: base autentica com hugodeco/OIDC; publicar core ainda usa chave estática. Alinhar job publish ao base e verificar novamente; preservar diagnóstico de policy separadamente.

Teste explícito do usuário sufficit: verify-auth 40020605616 falhou; NUGET_USER restaurado para hugodeco. Repo owner sufficit ID66928451 e repo ID494192324 confirmados. Workflow publish já corrigido para OIDC no commit f8cf2b8; run40020446014 compilou/empacotou, mas login hugodeco recebeu401. Nova worktree do ajuste removida.

Política corrigida: verify-auth 40020871312 aprovado com hugodeco. Retomada execução publish 40020446014 após comprovação de autenticação.

Publicação aceita: run40020446014 attempt2 success; HTTP201, versão1.26.1023.2040, commitf8cf2b8. Verificando download/indexação.

Registro de entrega gravado em docs/activities/202610231741-nuget-published.md. Último download público ainda404; não reenviar pacote já aceito. Limpeza desta tarefa concluída.
