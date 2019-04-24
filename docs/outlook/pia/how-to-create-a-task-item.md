---
title: 作業アイテムを作成する
TOCTitle: Create a task item
ms:assetid: d458dd31-2771-4a3c-a713-13c7e4e02a74
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184644(v=office.15)
ms:contentKeyID: 55119894
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4f9a8f156ec43f446f27c94b2cb061de181b7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349470"
---
# <a name="create-a-task-item"></a><span data-ttu-id="04f25-102">作業アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="04f25-102">Create a task item</span></span>

<span data-ttu-id="04f25-103">この例では、[MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) メソッドを使用してタスク アイテムを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="04f25-103">This example shows how to create a task item by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="04f25-104">例</span><span class="sxs-lookup"><span data-stu-id="04f25-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="04f25-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="04f25-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="04f25-106">次のコード例の CreateToDoItemExample は、アイテム上で **MarkAsTask** メソッドを呼び出してアイテムを保存することで、To Do アイテムを作成します。</span><span class="sxs-lookup"><span data-stu-id="04f25-106">In the following code example, CreateToDoItemExample creates a to-do item by calling the **MarkAsTask** method on the item and then saving the item.</span></span> <span data-ttu-id="04f25-107">このアイテムには、</span><span class="sxs-lookup"><span data-stu-id="04f25-107">The example marks the item for follow-up tomorrow and sets a reminder for tomorrow at 10:00 A.M.</span></span> <span data-ttu-id="04f25-108">[ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) プロパティと [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)) プロパティを使用して、翌日の処理対象を示すマークと翌日の午前 10 時のアラームが設定されます。</span><span class="sxs-lookup"><span data-stu-id="04f25-108">by using the [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) and [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)) properties.</span></span> <span data-ttu-id="04f25-109">その後、[Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) メソッドを使用してアイテムが保存されます。</span><span class="sxs-lookup"><span data-stu-id="04f25-109">The example then uses the [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) method to save the item.</span></span>

<span data-ttu-id="04f25-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="04f25-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="04f25-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04f25-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="04f25-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="04f25-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateToDoItemExample()
{
    // Date operations
    DateTime today = DateTime.Parse("10:00 AM");
    TimeSpan duration = TimeSpan.FromDays(1);
    DateTime tomorrow = today.Add(duration);
    Outlook.MailItem mail = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Find(
        "[MessageClass]='IPM.Note'") as Outlook.MailItem;
    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkTomorrow);
    mail.TaskStartDate = today;
    mail.ReminderSet = true;
    mail.ReminderTime = tomorrow;
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="04f25-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="04f25-113">See also</span></span>

- [<span data-ttu-id="04f25-114">タスク</span><span class="sxs-lookup"><span data-stu-id="04f25-114">Tasks</span></span>](tasks.md)

