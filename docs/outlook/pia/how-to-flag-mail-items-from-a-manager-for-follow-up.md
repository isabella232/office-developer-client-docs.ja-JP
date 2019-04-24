---
title: 上司からのメール アイテムにフラグを設定する
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa3cf00a116b51f88f47ef48eab566155626dbbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320245"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>上司からのメール アイテムにフラグを設定する

この例では、ユーザーの上司から受信した電子メール アイテムにフラグを設定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

Microsoft Outlook には、フラグを設定するシステムがあり、メール アイテム、連絡先アイテムなどの Outlook アイテムに、処理対象であることを示すフラグを設定できます。Outlook アイテムにフラグを設定すると、その Outlook アイテムに関する情報と、必要な処理に関するその他の情報が、Outlook ユーザー インターフェイスの **To Do バー**とカレンダー ナビゲーション モジュールに表示されます。 **To Do バー**は、Outlook エクスプローラー ウィンドウの一般的な構成では、縦型の作業ウィンドウとして表示されます。To Do バーには、カレンダー ナビゲーター コントロール、今後の予定、およびフラグ設定済みアイテムが表示されます。 **To Do バー** 自体は拡張可能ではなく、 **To Do バー**の構成オプションを設定できるのは Outlook ユーザー インターフェイスからのみです。アイテムにフラグを設定すると、タスクおよび To Do アイテムを整理して優先順位付けできます。

次のコード サンプルでは、アイテムのグループに指定の処理期間をマークします。 この例では、現在のユーザーの受信トレイ内にあるアイテムから、そのユーザーの上司から受信したアイテムをすべて取得します。DAV Searching and Locating (DASL) クエリを使用し、差出人が上司の名前の、"IPM.NOTE" という種類のメッセージをフィルター処理します。 次に、[Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) プロパティの [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) 値に基づいて、すべてのアイテムにフラグを設定します。 [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) メソッドを使用して、重要度「高」のすべてのアイテムに今日の処理対象のフラグを設定し、重要度「中」のすべてのアイテムに今週の処理対象のフラグを設定します。


> [!NOTE]
> **Importance** プロパティと **MarkAsTask** メソッドは、**Item** オブジェクトのメンバーです。


Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "https://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
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
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [タスク](tasks.md)

