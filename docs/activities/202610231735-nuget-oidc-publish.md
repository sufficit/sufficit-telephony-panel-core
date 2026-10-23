# Alinhamento da publicação NuGet

NUGET_USER=hugodeco confirmado em base e Blazor UI. Sonda base 40020366465
aprovada em 23/10/2026, demonstrando autenticação válida dessa conta.
Core tinha verify-auth via OIDC mas publicação com chave estática. Job publish
agora usa NuGet/login no SHA já usado por base, id-token:write e chave temporária.
YAML e configuração validados. Código do pacote inalterado. A autenticação do
core depende de policy correspondente ao repo 494192324/workflow publish.yml;
correção de workflow não comprova que a policy já esteja aceita.
