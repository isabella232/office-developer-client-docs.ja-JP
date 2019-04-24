---
title: ローカル コンピューターでルールを実行する
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9840133b7cd70b72e0bedf57931dfa9e53c67b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320350"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="765af-102">ローカル コンピューターでルールを実行する</span><span class="sxs-lookup"><span data-stu-id="765af-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="765af-103">この例では、[RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) オブジェクトの [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) プロパティを使用して、ローカル コンピューターでルールを実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="765af-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="765af-104">例</span><span class="sxs-lookup"><span data-stu-id="765af-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="765af-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="765af-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="765af-p101">メールボックスが Exchange サーバーでホストされている場合、ルールは Exchange サーバーまたは Outlook クライアントで実行できます。サーバーでルールが実行される場合、Outlook が実行されていなくても、ルールの条件の評価とルールの処理の実行が可能になります。クライアントでルールが実行される場合、ルールの実行には Outlook が実行されていることが必要になります。[Rule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) オブジェクトの [IsLocalRule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) プロパティが **true** を返す場合には、ルールはクライアントで実行されます。</span><span class="sxs-lookup"><span data-stu-id="765af-p101">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client. If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed. If the rule is executed on the client, Outlook must be running for the rule to execute. If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="765af-110">既定でクライアントで実行されるルールの処理 (新着メール通知の表示など) については、 **OnLocalMachine** 条件が自動的に有効になり、クライアント側のみの [RuleAction](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) オブジェクトの **Enabled** プロパティが [true](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="765af-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="765af-111">一般にサーバーで実行されるルールについては、クライアント側のみの **RuleAction** オブジェクトの **Enabled** プロパティを設定して **OnLocalMachine** 条件を有効にします。</span><span class="sxs-lookup"><span data-stu-id="765af-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="765af-112">これによって、そのルールは強制的にクライアントでローカルに実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="765af-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="765af-113">ルールの **OnLocalMachine** 条件を有効にすると、他のコンピューターから同じルールが検査される場合に [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) 条件も有効になります。</span><span class="sxs-lookup"><span data-stu-id="765af-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="765af-114">[olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) 型のルール条件は、現在のコンピューター以外の特定のコンピューターでのみルールを実行できることを示し、プログラムからは有効と無効を設定できません。</span><span class="sxs-lookup"><span data-stu-id="765af-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="765af-115">たとえば、現在のコンピューターでルールを作成し、 **OnLocalMachine** ルール条件を有効にすると、そのルールはそのコンピューターのみで実行できます。</span><span class="sxs-lookup"><span data-stu-id="765af-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="765af-116">同じルールを他のコンピューターで実行すると、そのルールの **OnOtherMachine** ルール条件が有効であることが示されます。</span><span class="sxs-lookup"><span data-stu-id="765af-116">If the same rule is executed on another computer, the rule will show that the **OnOtherMachine** rule condition is enabled.</span></span>

<span data-ttu-id="765af-117">次のコード例の DemoOnMachineOnly では、ルールを作成し、**Enabled** プロパティを **true** に設定することによって、[OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) 条件と [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) 処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="765af-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="765af-118">次に **OnLocalMachine** 条件を有効にし、サーバー側ルールがローカルに実行されるようにして、ルールを保存します。</span><span class="sxs-lookup"><span data-stu-id="765af-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="765af-119">既定では、 **Forward** 処理および **OnlyToMe** 条件はサーバーで処理されます。</span><span class="sxs-lookup"><span data-stu-id="765af-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="765af-120">**OnLocalMachine** 条件を有効にすると、それらはクライアント側ルールとして処理されるようになります。</span><span class="sxs-lookup"><span data-stu-id="765af-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="765af-121">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="765af-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="765af-122">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="765af-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="765af-123">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="765af-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="765af-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="765af-124">See also</span></span>

- [<span data-ttu-id="765af-125">ルール</span><span class="sxs-lookup"><span data-stu-id="765af-125">Rules</span></span>](rules.md)

