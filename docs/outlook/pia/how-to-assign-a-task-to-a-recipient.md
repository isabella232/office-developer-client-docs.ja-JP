---
title: 受信者にタスクを割り当てる
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54259b00fb3eb67c86985758bb86f5ab7ba120eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359738"
---
# <a name="assign-a-task-to-a-recipient"></a><span data-ttu-id="ecc76-102">受信者にタスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="ecc76-102">Assign a task to a recipient</span></span>

<span data-ttu-id="ecc76-103">この例では、タスクを作成して受信者に割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ecc76-103">This example shows how to create a task and assign it to a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="ecc76-104">例</span><span class="sxs-lookup"><span data-stu-id="ecc76-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ecc76-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="ecc76-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="ecc76-106">次のコード例の AssignTaskExample は、[TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを作成し、[Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\))、[StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\))、および [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)) プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecc76-106">In the following code example, AssignTaskExample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and specifies values for the [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)), and [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)) properties.</span></span> <span data-ttu-id="ecc76-107">[Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) メソッドを使用して、このタスクが割り当てられたタスクであることを指定します。</span><span class="sxs-lookup"><span data-stu-id="ecc76-107">The [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) method specifies that the task is an assigned task.</span></span> <span data-ttu-id="ecc76-108">[Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) メソッドを使用して [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを **TaskItem** に追加した後、[Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) メソッドでタスクを受信者に送信します。</span><span class="sxs-lookup"><span data-stu-id="ecc76-108">After a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object is added to the **TaskItem** by using the [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method, the [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) method sends the task to the recipient.</span></span>

<span data-ttu-id="ecc76-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecc76-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ecc76-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecc76-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ecc76-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ecc76-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AssignTaskExample()
{
    Outlook.TaskItem task = Application.CreateItem(
        Outlook.OlItemType.olTaskItem) as Outlook.TaskItem;
    task.Subject = "Tax Preparation";
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM");
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM");
    Outlook.RecurrencePattern pattern =
        task.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly;
    pattern.PatternStartDate = DateTime.Parse("4/1/2007");
    pattern.NoEndDate = true;
    task.ReminderSet = true;
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM");
    task.Assign();
    task.Recipients.Add("accountant@example.com");
    task.Recipients.ResolveAll();
    task.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="ecc76-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecc76-112">See also</span></span>

- [<span data-ttu-id="ecc76-113">タスク</span><span class="sxs-lookup"><span data-stu-id="ecc76-113">Tasks</span></span>](tasks.md)

