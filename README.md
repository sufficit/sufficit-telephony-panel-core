# Sufficit.Telephony.Panel.Core

Contratos compartilhados pelo painel de telefonia e seus serviços consumidores.

- Repositório: `sufficit-telephony-panel-core`.
- Projeto, assembly e pacote: `Sufficit.Telephony.Panel.Core`.
- Namespace: `Sufficit.Telephony.Panel`.
- Targets: `netstandard2.0`, `net7.0`, `net10.0`.

Contém os modelos `EventsPanelCardInfo`, `EventsPanelCardKind`, opções e interfaces
compartilhadas. Os nomes das classes, propriedades JSON, valores do enum e a chave
de configuração `Sufficit:Telephony:EventsPanel` foram preservados na renomeação.

```csharp
using Sufficit.Telephony.Panel;

var card = new EventsPanelCardInfo { Label = "Atendimento", Kind = EventsPanelCardKind.QUEUE };
```

## Migração

Atualizar referências de projeto/pacote e imports para o novo nome e recompilar
os consumidores em conjunto. A alteração de assembly e namespace quebra a
compatibilidade binária com consumidores compilados contra o pacote antigo.
O novo pacote precisa ser publicado antes de builds que dependam do NuGet.

## Desenvolvimento

Worktrees devem ficar em `.worktrees/` dentro do próprio repositório.

```sh
dotnet build src/Sufficit.Telephony.Panel.Core.csproj
dotnet pack src/Sufficit.Telephony.Panel.Core.csproj -c Release
```

Licença: [MIT](license).
