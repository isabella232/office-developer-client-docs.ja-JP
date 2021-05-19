---
title: 上司からのメール アイテムにフラグを設定する
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 06e6bdd91198cabeff689681f2999d6fd2cb725a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542591"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a><span data-ttu-id="a32ce-102">上司からのメール アイテムにフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="a32ce-102">Flag mail items from a manager for follow-up</span></span>

<span data-ttu-id="a32ce-103">この例では、ユーザーの上司から受信した電子メール アイテムにフラグを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a32ce-103">This example shows how to flag email items that were received from the user’s manager for follow-up.</span></span>

## <a name="example"></a><span data-ttu-id="a32ce-104">例</span><span class="sxs-lookup"><span data-stu-id="a32ce-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a32ce-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="a32ce-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a32ce-p101">Microsoft Outlook には、フラグを設定するシステムがあり、メール アイテム、連絡先アイテムなどの Outlook アイテムに、処理対象であることを示すフラグを設定できます。Outlook アイテムにフラグを設定すると、その Outlook アイテムに関する情報と、必要な処理に関するその他の情報が、Outlook ユーザー インターフェイスの **To Do バー** とカレンダー ナビゲーション モジュールに表示されます。 **To Do バー** は、Outlook エクスプローラー ウィンドウの一般的な構成では、縦型の作業ウィンドウとして表示されます。To Do バーには、カレンダー ナビゲーター コントロール、今後の予定、およびフラグ設定済みアイテムが表示されます。 **To Do バー** 自体は拡張可能ではなく、 **To Do バー** の構成オプションを設定できるのは Outlook ユーザー インターフェイスからのみです。アイテムにフラグを設定すると、タスクおよび To Do アイテムを整理して優先順位付けできます。</span><span class="sxs-lookup"><span data-stu-id="a32ce-p101">Microsoft Outlook provides a task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up. When you flag an Outlook item for follow-up, information about that Outlook item, along with other task-based information, is displayed on the **To-Do Bar** and Calendar navigation module in the Outlook user interface. The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window. It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up. The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface. Flagging items allows to you organize and prioritize tasks and to-do items.</span></span>

<span data-ttu-id="a32ce-112">次のコード サンプルでは、アイテムのグループに指定の処理期間をマークします。</span><span class="sxs-lookup"><span data-stu-id="a32ce-112">The following code example marks a group of items for a specified follow-up interval.</span></span> <span data-ttu-id="a32ce-113">この例では、現在のユーザーの受信トレイ内にあるアイテムから、そのユーザーの上司から受信したアイテムをすべて取得します。DAV Searching and Locating (DASL) クエリを使用し、差出人が上司の名前の、"IPM.NOTE" という種類のメッセージをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="a32ce-113">The example gets all items in the current user’s Inbox that are from the current user’s manager by using a DAV Searching and Locating (DASL) query to filter for messages of type “IPM.NOTE” with the manager’s name as the sender.</span></span> <span data-ttu-id="a32ce-114">次に、[Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) プロパティの [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) 値に基づいて、すべてのアイテムにフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a32ce-114">It then flags all items according to the [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) value of the [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) property.</span></span> <span data-ttu-id="a32ce-115">[MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) メソッドを使用して、重要度「高」のすべてのアイテムに今日の処理対象のフラグを設定し、重要度「中」のすべてのアイテムに今週の処理対象のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a32ce-115">All high-importance items are flagged for follow-up today and all normal-importance items are flagged for follow-up this week by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>


> [!NOTE]
> <span data-ttu-id="a32ce-116">**Importance** プロパティと **MarkAsTask** メソッドは、**Item** オブジェクトのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="a32ce-116">The **Importance** property and the **MarkAsTask** method are **Item** object members.</span></span>


<span data-ttu-id="a32ce-117">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a32ce-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a32ce-118">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a32ce-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a32ce-119">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a32ce-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "http://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
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

## <a name="see-also"></a><span data-ttu-id="a32ce-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a32ce-120">See also</span></span>

- [<span data-ttu-id="a32ce-121">タスク</span><span class="sxs-lookup"><span data-stu-id="a32ce-121">Tasks</span></span>](tasks.md)

