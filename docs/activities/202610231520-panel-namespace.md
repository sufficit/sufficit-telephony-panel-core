# Correção do namespace padrão

Namespace e RootNamespace corrigidos para Sufficit.Telephony.Panel conforme
pedido do mantenedor. Projeto, assembly e PackageId permanecem
Sufficit.Telephony.Panel.Core. Atualizadas 49 fontes/imports/referências
qualificadas do core, painel, streaming, base, EFData, Standard, EndPoints e Client.
README ajustado. Classes e contratos JSON preservados.

Validação: pack Release nos três targets aprovado; 1204 checks do painel
aprovados; build EndPoints (33 projetos) e Client (9 projetos) sem erros.
Builds apresentam avisos existentes de dependências/código.
Busca nas fontes ativas não encontrou namespace Sufficit.Telephony.Panel.Core.
Pacote local: /tmp/panel-namespace-pack. Sem commit/push, publicação NuGet ou deploy.
