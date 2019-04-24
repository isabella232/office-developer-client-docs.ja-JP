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
# <a name="create-a-recurring-task"></a>定期タスクを作成する

この例では、定期的なタスクを作成します。

## <a name="example"></a>例

次のコード サンプルでは、[TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを作成し、**TaskItem** の [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) メソッドを使用して、タスクを定期的なタスクにします。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [タスク](tasks.md)

