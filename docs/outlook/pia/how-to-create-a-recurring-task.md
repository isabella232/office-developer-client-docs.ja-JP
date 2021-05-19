---
title: 定期タスクを作成する
TOCTitle: Create a recurring task
ms:assetid: bbca8527-79af-4c00-aae7-a1fd381e707c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623455(v=office.15)
ms:contentKeyID: 55119932
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fd2df68ef866008799a7206e7ae041e5bfd82a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349526"
---
# <a name="create-a-recurring-task"></a><span data-ttu-id="f1965-102">定期タスクを作成する</span><span class="sxs-lookup"><span data-stu-id="f1965-102">Create a recurring task</span></span>

<span data-ttu-id="f1965-103">この例では、定期的なタスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="f1965-103">This example creates a recurrent task.</span></span>

## <a name="example"></a><span data-ttu-id="f1965-104">例</span><span class="sxs-lookup"><span data-stu-id="f1965-104">Example</span></span>

<span data-ttu-id="f1965-105">次のコード サンプルでは、[TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを作成し、**TaskItem** の [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) メソッドを使用して、タスクを定期的なタスクにします。</span><span class="sxs-lookup"><span data-stu-id="f1965-105">This code sample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and uses the [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) method of the **TaskItem** to make the task a recurrent task.</span></span>

<span data-ttu-id="f1965-106">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1965-106">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f1965-107">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1965-107">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f1965-108">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f1965-108">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateRecurringTask()
    Dim task As Outlook.TaskItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olTaskItem), Outlook.TaskItem)
    task.Subject = "Tax Preparation"
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM")
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM")
    Dim pattern As Outlook.RecurrencePattern = _
        task.GetRecurrencePattern()
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly
    pattern.PatternStartDate = DateTime.Parse("4/1/2007")
    pattern.NoEndDate = True
    task.ReminderSet = True
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM")
    task.Save()
End Sub
```


```csharp
private void CreateRecurringTask()
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
    task.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="f1965-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1965-109">See also</span></span>

- [<span data-ttu-id="f1965-110">タスク</span><span class="sxs-lookup"><span data-stu-id="f1965-110">Tasks</span></span>](tasks.md)

