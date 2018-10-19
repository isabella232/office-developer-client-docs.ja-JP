---
title: 受信者に送信されたタスク依頼アイテムを表示する
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f26e8d1402b75272e79c6244b7bd2875d783c1f1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406639"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>受信者に送信されたタスク依頼アイテムを表示する

この例では、受信者の受信トレイにあるタスクの依頼のアイテムをすべて表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) オブジェクトは、タスクを別のユーザーに割り当てる依頼を表します。 **TaskRequestItem** は、受信者の受信トレイにアイテムを受信した時点で作成されます。 次のコード例の ShowTaskRequests では、受信者の受信トレイをフィルター処理して [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを作成し、[MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) プロパティの値が **IPM.TaskRequest** と等しい各アイテムの行を挿入します。 受信者の受信トレイ フォルダーの各タスクの件名が、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込まれます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [タスク](tasks.md)

