---
title: 受信者に送信されたタスク依頼アイテムを表示する
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 753de29eb19ec73ebb7cf1fb8e407d02e55c1b41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616335"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>受信者に送信されたタスク依頼アイテムを表示する

この例では、受信者の受信トレイにあるタスクの依頼のアイテムをすべて表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) オブジェクトは、タスクを別のユーザーに割り当てる依頼を表します。 **TaskRequestItem** は、受信者の受信トレイにアイテムを受信した時点で作成されます。 次のコード例の ShowTaskRequests では、受信者の受信トレイをフィルター処理して [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを作成し、[MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) プロパティの値が **IPM.TaskRequest** と等しい各アイテムの行を挿入します。 受信者の受信トレイ フォルダーの各タスクの件名が、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込まれます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

