# Integração da migração Panel Core na main

Autorização explícita do mantenedor: "merge na main".
Namespace final Sufficit.Telephony.Panel; projeto/pacote Sufficit.Telephony.Panel.Core.
Core (4cc5621), base (e77bcd0), client (8fca0c8) e Blazor (d4d52384) já estavam
integrados na main remota por outra entrega ao iniciar esta etapa.

## Commits publicados e verificados na main remota

- sufficit-efdata: `6d31b8acc67caf34e500b765527a6ad7637c4b37`
- sufficit-standard: `f89ee45c0e1521702b004f0bd106da60ccb0a65b`
- sufficit-statistics: `5c0ee48a9279f9f9740029df85d320c2db27175b`
- sufficit-ami-events: `0d134ab9ea8e07f13f98d215769eca486de1d8d6`
- sufficit-ari: `47a78de7396e69d12e25c9d507af271ab9e45a53`
- sufficit-telephony-panel: `f296271f49846a6044acc72d2b46088bf724e17e`
- sufficit-endpoints: `4b4729f8ed38f9f8dcd4a350be53918797da4454`
- sufficit-web: `0fb65b75a915f16c329ffb11db1750c040036444`
- sufficit-project-management: `13fcc9e67bba72d133f06ab24634392ea546ef05`
- sufficit-services-openclaw: `15c3a91bc5e5c46ea5131d2ab77b764a7ff69ffa`

## Preservação e validação

Commits isolados em worktrees internos a partir de origin/main; apenas diffs
verificados da migração foram incluídos. Nenhum force-push. Checkouts main foram
sincronizados preservando alterações alheias. Branches de correção das notificações
ARI/AMI permanecem intactos; seus commits funcionais não fizeram parte deste merge.
Validação anterior: 1204 checks do painel, builds core/EndPoints/Client e testes
de persistência aprovados. CI dos novos pushes estava em execução na conferência;
não equivale a sucesso de CI ou deploy. Dez SHAs de main remota confirmados.

## Bloqueio de publicação NuGet

O core já integrado compilou no GitHub, mas o workflow 40002569961 falhou ao
publicar Sufficit.Telephony.Panel.Core: HTTP 403, API key inválida/expirada ou sem
permissão para o novo pacote. É necessário corrigir a credencial/escopo no NuGet
antes de builds que dependam exclusivamente do pacote. Não foi repetida a execução
sem corrigir a causa e não foi afirmada publicação/deploy de produção.
