---
title: 受信者に送信されたタスク依頼アイテムを表示する
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726051"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a><span data-ttu-id="b3088-102">受信者に送信されたタスク依頼アイテムを表示する</span><span class="sxs-lookup"><span data-stu-id="b3088-102">Display the task request items sent to a recipient</span></span>

<span data-ttu-id="b3088-103">この例では、受信者の受信トレイにあるタスクの依頼のアイテムをすべて表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b3088-103">This example shows how to display all of the task request items that are in a recipient's Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="b3088-104">例</span><span class="sxs-lookup"><span data-stu-id="b3088-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b3088-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="b3088-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="b3088-106">[TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) オブジェクトは、タスクを別のユーザーに割り当てる依頼を表します。</span><span class="sxs-lookup"><span data-stu-id="b3088-106">A [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) object represents a request to assign a task to another user.</span></span> <span data-ttu-id="b3088-107">**TaskRequestItem** は、受信者の受信トレイにアイテムを受信した時点で作成されます。</span><span class="sxs-lookup"><span data-stu-id="b3088-107">The **TaskRequestItem** is created when the item is received in the recipient's Inbox.</span></span> <span data-ttu-id="b3088-108">次のコード例の ShowTaskRequests では、受信者の受信トレイをフィルター処理して [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを作成し、[MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) プロパティの値が **IPM.TaskRequest** と等しい各アイテムの行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="b3088-108">In the following code example, ShowTaskRequests filters through a recipient’s Inbox, creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and inserts a row for each item for which the value of the [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) property equals **IPM.TaskRequest**.</span></span> <span data-ttu-id="b3088-109">受信者の受信トレイ フォルダーの各タスクの件名が、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="b3088-109">The subject of each task in the recipient’s Inbox folder is then written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="b3088-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3088-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b3088-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3088-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b3088-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b3088-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b3088-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3088-113">See also</span></span>

- [<span data-ttu-id="b3088-114">タスク</span><span class="sxs-lookup"><span data-stu-id="b3088-114">Tasks</span></span>](tasks.md)

