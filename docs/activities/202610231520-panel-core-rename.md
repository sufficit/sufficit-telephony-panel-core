# Renomeação de Panel Core

Pedido: renomear projeto/repositório e namespaces para corresponder a sufficit-telephony-panel-core.

## Entrega

Repositório GitHub renomeado para https://github.com/sufficit/sufficit-telephony-panel-core;
origin e diretório local atualizados. Projeto, assembly e pacote agora
Sufficit.Telephony.Panel.Core; namespace corrigido conforme pedido para
Sufficit.Telephony.Panel. Atualizados consumidores base, standard, client,
endpoints, EFData, streaming, painel, referências do Blazor, solução Web,
workflows ARI/AMI/Blazor/Web e inventários de workspace.

As nove fontes do core diferem do HEAD anterior somente no namespace.
Classes, enums, JSON e chave de configuração foram preservados.
README corrigido para os tipos existentes e caminho do README no pack corrigido
para funcionar em filesystem sensível a maiúsculas. Removida a regra legada de
.gitignore que ocultava o arquivo csproj renomeado.

## Validação

- Core: build netstandard2.0, net7.0 e net10.0; pack Release com três DLLs.
- Painel: 1204 checks aprovados (`dotnet run --project tests/Panel.Tests.csproj`).
- Standard: dois EventsPanelRuntimeFacadeTests aprovados (persistência/leitura).
- EndPoints: build 33 projetos, zero erros, 285 avisos.
- Client: build 9 projetos, zero erros, 21 avisos.
- Blazor Server: build 20 projetos, zero erros, 24 avisos.
- Busca nos arquivos ativos dos consumidores não encontrou namespace/core antigo;
  referências aos componentes UI arquivados e documentos históricos preservadas.
- Alterações preexistentes de outras tarefas preservadas; nenhum deploy executado.

## Limites de publicação

Fontes alteradas nos checkouts locais, sem commit/push desta migração.
Pacote gerado em /tmp/panel-core-pack, ainda não publicado no NuGet.
O rename do GitHub foi confirmado pela API. Publicar o pacote novo antes de builds
que usem fallback NuGet; recompilar consumidores coordenadamente, pois assembly
 e namespace novos quebram compatibilidade binária. Os builds possuem avisos de
pacotes/deprecações, inclusive advisories; as versões não foram alteradas nesta tarefa.
Worktrees históricos e repositórios arquivados não foram migrados.
