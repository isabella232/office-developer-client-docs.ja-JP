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
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>上司からのメール アイテムを分類して確認のフラグを設定する

この例では、ユーザーの上司からのメール アイテムを分類して確認のフラグを設定するための仕分けルールを設定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Outlook の仕分けルールは、アカウントとルールの種類に応じて、サーバー側とクライアント側のどちらかで処理できます。さまざまな方法で仕分けルールを実装して、メールボックスのアイテムを整理するための組織独自の設定を適用できます。たとえば、未読メールを整理するサブフォルダー階層を作成し、対象の領域ごとにメールを読むことができます。メッセージの差出人に応じたサブフォルダー階層を作成することもできます。また、メールを分類し、検索フォルダーを使用して分類項目ごとにメールを集約することもできます。

Outlook のルールを表す [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) オブジェクトを含む **Rule** オブジェクト モデルでは、特定の組織編成の適用、ソリューションに固有の特定のルールの作成、および特定のルールがユーザーのグループに配置されていることの確認のためのルールを、プログラムを使用して作成できます。 **Rule** オブジェクト モデルを使用することで、プログラムを使用してルールの追加、編集、および削除を行えます。 [Rule](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) コレクションと **Rule** オブジェクトを使用することで、セッションで定義されたルールへのアクセス、追加、および削除も行えます。 

**Rule** オブジェクトには、ルールが送信ルールなのか受信ルールなのかを示す [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) プロパティが含まれます。 ルールが作成されると **RuleType** プロパティが指定され、ルールを削除するか、または別の **RuleType** プロパティを使用してルールを再作成する場合を除いて、変更できなくなります。 [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) オブジェクトと [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) オブジェクト、それらのコレクション オブジェクト、および派生のアクション オブジェクトと条件オブジェクトは、ルール のアクションと条件の編集でも使用されます。

**Rules** のオブジェクト モデルは、Outlook のユーザー インターフェイスの仕分けルールと通知ウィザードで作成できるすべての仕分けルールをサポートしているわけではありませんが、使用頻度の高い仕分けルールのアクションと条件の多くをサポートしています。仕分けルールと通知ウィザードで作成され、メッセージ (メール アイテム、会議出席依頼、タスクの依頼、ドキュメント、配信済みメッセージ、開封済みメッセージ、投票結果、および不在通知を含む) に適用される仕分けルールもプログラムで作成できます。

現在のユーザーのメールボックスが Exchange サーバーでホストされている場合、ルールは Exchange サーバー上または Outlook クライアント上で実行できます。 [Rule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) オブジェクトの **IsLocalRule** プロパティが **true** を返す場合、仕分けルールはクライアントで実行され、その際に Outlook が実行中であることが必要です。 仕分けルールがサーバー上で実行される場合、仕分けルールの条件の評価および仕分けルールのアクションの実行の際に Outlook が実行中である必要はありません。

> [!NOTE]
> [!メモ] 仕分けルールの例外条件を表す個別のコレクションはありません。仕分けルールの例外条件を表す [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) コレクションを取得するには、 **Rule** オブジェクトの [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) プロパティを使用します。

Outlook オブジェクト モデルを使用して仕分けルールを作成するには、次の手順に従います。

1.  既定の **Store** オブジェクトの [GetRules()](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) メソッドを呼び出して、 [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [DefaultStore](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) プロパティから [Rules](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) コレクションを取得します。ユーザーがオフラインの場合や Exchange サーバーに接続していない場合を考慮するために、 **try…catch** ブロックを使用します。これにより、Outlook でのエラーの発生を防ぎます。

2.  インスタンス変数を作成するには **Rules** オブジェクトで [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) メソッドを呼び出し、または、**Rule** オブジェクトを作成するには Name と [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) パラメーターを指定します。

3.  [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) コレクションおよび [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) コレクションを使用して、 **Rule** オブジェクトに対してアクション、条件、および例外を有効にします。 **RuleConditions** コレクションで有効にし、 [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) プロパティで返される条件は、仕分けルールの例外条件として処理され、組み込みのカスタム アクションまたは条件をこのコレクションに追加することはできない点に注意します。

4.  仕分けルールのアクション、条件、または例外で、有効にするものについて、[Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) プロパティを **true** に設定します。 [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) プロパティなど、アクションまたは条件によっては、 **Rule** オブジェクトをエラーなしで保存するために、そのアクションまたは条件に対して追加のプロパティを設定することが必要なものがあります。

5.  最後に、 [Rules](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) コレクションの **Save(Object)** メソッドを呼び出して、作成または変更した仕分けルールを保存します。例外を処理するために、 **Save** メソッドは **try…catch** ブロックで囲みます。

次のコード例では、CreateManagerRule は前述の手順を実装します。 最初に、CreateManagerRule は [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) プロパティが、現在のユーザーが Exchange ユーザーであることを示す [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを表しているかどうかを確認します。 現在のユーザーが Exchange ユーザーである場合、CreateManagerRule は現在のユーザーの上司を取得するために、**NameSpace** オブジェクトの **CurrentUser** プロパティの **ExchangeUser** オブジェクト上の [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを呼び出します。 次の条件を使用して受信メッセージを受信トレイのサブフォルダーに移動する受信ルールが作成されます。

- メッセージの送信元がユーザーの上司であること。

- 受信者がメッセージの [**宛先:**] 行にあること。

- メッセージが会議出席依頼または会議の更新情報でないこと。

最後に、メッセージに対し、今日の処理対象のフラグを設定します。CreateManagerRule では、ユーザーがオフラインの場合または Exchange キャッシュ モードで切断されている場合など、例外が発生する可能性がある条件のエラー処理も適切に行っています。 

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [ルール](rules.md)

