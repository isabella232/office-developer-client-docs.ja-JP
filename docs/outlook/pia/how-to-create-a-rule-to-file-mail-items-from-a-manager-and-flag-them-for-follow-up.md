---
title: 上司からのメール アイテムを分類して確認のフラグを設定する
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dba46c851050c3f948ec829ae2340e0492ca135f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360404"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="0da27-102">上司からのメール アイテムを分類して確認のフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="0da27-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="0da27-103">この例では、ユーザーの上司からのメール アイテムを分類して確認のフラグを設定するための仕分けルールを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0da27-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="0da27-104">例</span><span class="sxs-lookup"><span data-stu-id="0da27-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0da27-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="0da27-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0da27-p101">Outlook の仕分けルールは、アカウントとルールの種類に応じて、サーバー側とクライアント側のどちらかで処理できます。さまざまな方法で仕分けルールを実装して、メールボックスのアイテムを整理するための組織独自の設定を適用できます。たとえば、未読メールを整理するサブフォルダー階層を作成し、対象の領域ごとにメールを読むことができます。メッセージの差出人に応じたサブフォルダー階層を作成することもできます。また、メールを分類し、検索フォルダーを使用して分類項目ごとにメールを集約することもできます。</span><span class="sxs-lookup"><span data-stu-id="0da27-p101">Outlook rules can operate either server-side or client-side, depending on the type of account and rule. There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox. For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area. Or, you can create a subfolder hierarchy that corresponds to the sender of the message. You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="0da27-111">Outlook のルールを表す [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトを含む **Rule** オブジェクト モデルでは、特定の組織編成の適用、ソリューションに固有の特定のルールの作成、および特定のルールがユーザーのグループに配置されていることの確認のためのルールを、プログラムを使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="0da27-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="0da27-112">**Rule** オブジェクト モデルを使用することで、プログラムを使用してルールの追加、編集、および削除を行えます。</span><span class="sxs-lookup"><span data-stu-id="0da27-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="0da27-113">[Rule](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) コレクションと **Rule** オブジェクトを使用することで、セッションで定義されたルールへのアクセス、追加、および削除も行えます。</span><span class="sxs-lookup"><span data-stu-id="0da27-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="0da27-114">**Rule** オブジェクトには、ルールが送信ルールなのか受信ルールなのかを示す [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0da27-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="0da27-115">ルールが作成されると **RuleType** プロパティが指定され、ルールを削除するか、または別の **RuleType** プロパティを使用してルールを再作成する場合を除いて、変更できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0da27-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="0da27-116">[RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) オブジェクトと [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) オブジェクト、それらのコレクション オブジェクト、および派生のアクション オブジェクトと条件オブジェクトは、ルール のアクションと条件の編集でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0da27-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="0da27-p104">**Rules** のオブジェクト モデルは、Outlook のユーザー インターフェイスの仕分けルールと通知ウィザードで作成できるすべての仕分けルールをサポートしているわけではありませんが、使用頻度の高い仕分けルールのアクションと条件の多くをサポートしています。仕分けルールと通知ウィザードで作成され、メッセージ (メール アイテム、会議出席依頼、タスクの依頼、ドキュメント、配信済みメッセージ、開封済みメッセージ、投票結果、および不在通知を含む) に適用される仕分けルールもプログラムで作成できます。</span><span class="sxs-lookup"><span data-stu-id="0da27-p104">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions. Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="0da27-119">現在のユーザーのメールボックスが Exchange サーバーでホストされている場合、ルールは Exchange サーバー上または Outlook クライアント上で実行できます。</span><span class="sxs-lookup"><span data-stu-id="0da27-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user’s mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="0da27-120">[Rule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) オブジェクトの **IsLocalRule** プロパティが **true** を返す場合、仕分けルールはクライアントで実行され、その際に Outlook が実行中であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="0da27-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="0da27-121">仕分けルールがサーバー上で実行される場合、仕分けルールの条件の評価および仕分けルールのアクションの実行の際に Outlook が実行中である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0da27-121">If the rule executes on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="0da27-p106">[!メモ] 仕分けルールの例外条件を表す個別のコレクションはありません。仕分けルールの例外条件を表す [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) コレクションを取得するには、 **Rule** オブジェクトの [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0da27-p106">There is no separate collection that represents rule exception conditions. Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="0da27-124">Outlook オブジェクト モデルを使用して仕分けルールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0da27-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="0da27-p107">既定の **Store** オブジェクトの [GetRules()](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) メソッドを呼び出して、 [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [DefaultStore](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) プロパティから [Rules](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) コレクションを取得します。ユーザーがオフラインの場合や Exchange サーバーに接続していない場合を考慮するために、 **try…catch** ブロックを使用します。これにより、Outlook でのエラーの発生を防ぎます。</span><span class="sxs-lookup"><span data-stu-id="0da27-p107">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object. Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server. This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="0da27-128">インスタンス変数を作成するには **Rules** オブジェクトで [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) メソッドを呼び出し、または、**Rule** オブジェクトを作成するには Name と [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="0da27-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="0da27-p108">[RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) コレクションおよび [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) コレクションを使用して、 **Rule** オブジェクトに対してアクション、条件、および例外を有効にします。 **RuleConditions** コレクションで有効にし、 [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) プロパティで返される条件は、仕分けルールの例外条件として処理され、組み込みのカスタム アクションまたは条件をこのコレクションに追加することはできない点に注意します。</span><span class="sxs-lookup"><span data-stu-id="0da27-p108">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object. Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="0da27-p109">仕分けルールのアクション、条件、または例外で、有効にするものについて、[Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) プロパティを **true** に設定します。 [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) プロパティなど、アクションまたは条件によっては、 **Rule** オブジェクトをエラーなしで保存するために、そのアクションまたは条件に対して追加のプロパティを設定することが必要なものがあります。</span><span class="sxs-lookup"><span data-stu-id="0da27-p109">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational. Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="0da27-p110">最後に、 [Rules](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) コレクションの **Save(Object)** メソッドを呼び出して、作成または変更した仕分けルールを保存します。例外を処理するために、 **Save** メソッドは **try…catch** ブロックで囲みます。</span><span class="sxs-lookup"><span data-stu-id="0da27-p110">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules. Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="0da27-135">次のコード例では、CreateManagerRule は前述の手順を実装します。</span><span class="sxs-lookup"><span data-stu-id="0da27-135">In the following code example, CreateManagerRule implements the steps previously described.</span></span> <span data-ttu-id="0da27-136">最初に、CreateManagerRule は [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) プロパティが、現在のユーザーが Exchange ユーザーであることを示す [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを表しているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0da27-136">CreateManagerRule first verifies whether the [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) property represents an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="0da27-137">現在のユーザーが Exchange ユーザーである場合、CreateManagerRule は現在のユーザーの上司を取得するために、**NameSpace** オブジェクトの **CurrentUser** プロパティの **ExchangeUser** オブジェクト上の [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0da27-137">If the current user is an Exchange user, CreateManagerRule gets the current user’s manager by calling the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method on the **ExchangeUser** object of the **CurrentUser** property of the **NameSpace** object.</span></span> <span data-ttu-id="0da27-138">次の条件を使用して受信メッセージを受信トレイのサブフォルダーに移動する受信ルールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0da27-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="0da27-139">メッセージの送信元がユーザーの上司であること。</span><span class="sxs-lookup"><span data-stu-id="0da27-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="0da27-140">受信者がメッセージの [**宛先:**] 行にあること。</span><span class="sxs-lookup"><span data-stu-id="0da27-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="0da27-141">メッセージが会議出席依頼または会議の更新情報でないこと。</span><span class="sxs-lookup"><span data-stu-id="0da27-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="0da27-p112">最後に、メッセージに対し、今日の処理対象のフラグを設定します。CreateManagerRule では、ユーザーがオフラインの場合または Exchange キャッシュ モードで切断されている場合など、例外が発生する可能性がある条件のエラー処理も適切に行っています。 </span><span class="sxs-lookup"><span data-stu-id="0da27-p112">Finally, the message is flagged for follow-up today. CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="0da27-144">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0da27-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0da27-145">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0da27-145">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0da27-146">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0da27-146">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0da27-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="0da27-147">See also</span></span>

- [<span data-ttu-id="0da27-148">ルール</span><span class="sxs-lookup"><span data-stu-id="0da27-148">Rules</span></span>](rules.md)

