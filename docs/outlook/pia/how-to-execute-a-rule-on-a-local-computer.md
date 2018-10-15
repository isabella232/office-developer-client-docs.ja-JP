---
title: ローカル コンピューターでルールを実行する
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405841"
---
# <a name="execute-a-rule-on-a-local-computer"></a>ローカル コンピューターでルールを実行する

この例では、[RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) オブジェクトの [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) プロパティを使用して、ローカル コンピューターでルールを実行する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

メールボックスが Exchange サーバーでホストされている場合、ルールは Exchange サーバーまたは Outlook クライアントで実行できます。サーバーでルールが実行される場合、Outlook が実行されていなくても、ルールの条件の評価とルールの処理の実行が可能になります。クライアントでルールが実行される場合、ルールの実行には Outlook が実行されていることが必要になります。[Rule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) オブジェクトの [IsLocalRule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) プロパティが **true** を返す場合には、ルールはクライアントで実行されます。

既定でクライアントで実行されるルールの処理 (新着メール通知の表示など) については、 **OnLocalMachine** 条件が自動的に有効になり、クライアント側のみの [RuleAction](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) オブジェクトの **Enabled** プロパティが [true](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) に設定されます。 一般にサーバーで実行されるルールについては、クライアント側のみの **RuleAction** オブジェクトの **Enabled** プロパティを設定して **OnLocalMachine** 条件を有効にします。 これによって、そのルールは強制的にクライアントでローカルに実行されるようになります。 

ルールの **OnLocalMachine** 条件を有効にすると、他のコンピューターから同じルールが検査される場合に [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) 条件も有効になります。 [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) 型のルール条件は、現在のコンピューター以外の特定のコンピューターでのみルールを実行できることを示し、プログラムからは有効と無効を設定できません。 たとえば、現在のコンピューターでルールを作成し、 **OnLocalMachine** ルール条件を有効にすると、そのルールはそのコンピューターのみで実行できます。 同じルールを他のコンピューターで実行すると、そのルールの **OnOtherMachine** ルール条件が有効であることが示されます。

次のコード例の DemoOnMachineOnly では、ルールを作成し、**Enabled** プロパティを **true** に設定することによって、[OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) 条件と [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) 処理を有効にします。 次に **OnLocalMachine** 条件を有効にし、サーバー側ルールがローカルに実行されるようにして、ルールを保存します。 既定では、 **Forward** 処理および **OnlyToMe** 条件はサーバーで処理されます。 **OnLocalMachine** 条件を有効にすると、それらはクライアント側ルールとして処理されるようになります。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a>関連項目

- [ルール](rules.md)

