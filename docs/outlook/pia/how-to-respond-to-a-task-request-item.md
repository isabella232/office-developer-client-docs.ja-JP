---
title: タスク依頼アイテムに返信する
TOCTitle: Respond to a task request item
ms:assetid: 573c98ef-4d15-4fd1-bccd-25a22c9a63f0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184608(v=office.15)
ms:contentKeyID: 55119896
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9aa6416680bbf2443506415b5fa871d30fe5f32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357394"
---
# <a name="respond-to-a-task-request-item"></a>タスク依頼アイテムに返信する

以下の例では、タスク依頼アイテムの取得および返信を行う方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード サンプルでは、AcceptTaskRequest は [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) オブジェクトの [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) メソッドを使用して [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを取得します。 次に、パラメーターを [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)) に設定した [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)) メソッドを呼び出して、タスクの依頼を承諾します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AcceptTaskRequest()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).
        Items.Restrict(filter);
    if (items.Count > 0)
    {
        Outlook.TaskRequestItem taskRequest =
            (Outlook.TaskRequestItem)items[1];
        Outlook.TaskItem task =
            taskRequest.GetAssociatedTask(false);
        Outlook.TaskItem taskResponse = task.Respond(
            Outlook.OlTaskResponse.olTaskAccept, true, false);
        taskResponse.Send();
    }
}
```

## <a name="see-also"></a>関連項目

- [タスク](tasks.md)

