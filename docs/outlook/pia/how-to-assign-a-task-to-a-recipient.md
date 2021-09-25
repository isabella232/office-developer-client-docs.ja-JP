---
title: 受信者にタスクを割り当てる
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ba189b90468fdf967f4849cf0b1304afde0948f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616384"
---
# <a name="assign-a-task-to-a-recipient"></a>受信者にタスクを割り当てる

この例では、タスクを作成して受信者に割り当てる方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


次のコード例の AssignTaskExample は、[TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを作成し、[Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\))、[StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\))、および [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)) プロパティの値を指定します。 [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) メソッドを使用して、このタスクが割り当てられたタスクであることを指定します。 [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) メソッドを使用して [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを **TaskItem** に追加した後、[Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) メソッドでタスクを受信者に送信します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [タスク](tasks.md)

