---
title: フォルダーのアイテムをフィルター処理して効率よく列挙する
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01f0019d0f038cd1e9ea8fee7c85d0d2f18c4b47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405673"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a>フォルダーのアイテムをフィルター処理して効率よく列挙する

この例では、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを使用して受信トレイ内の添付ファイルがあるアイテムをフィルター処理し、そのようなアイテムを効率よく列挙して、各アイテムの選択されたプロパティを表示する方法を示します。

## <a name="example"></a>例

このコード サンプルでは、MAPI 名前空間でプロパティ **PR\_HASATTACH** を指定し、このプロパティを使用して受信トレイの [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドで初期フィルターを作成します。 アイテムの種類に対する **Table** オブジェクトには、そのアイテムの種類の特定のプロパティを表す既定の列があります。 列をカスタマイズするため、この例では最初にその [Table](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) の [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) コレクションで **RemoveAll** メソッドを呼び出してから、 [Columns](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) コレクションで **Add** メソッドを呼び出し、組み込みのプロパティ名と、現地時間で日時が表現された値を格納する **ReceivedTime** を使用して、 **EntryID**、 **Subject**、 **ReceivedTime** の各プロパティを追加します。 

次に、 **Columns.Add** を再び呼び出して **ReceiveTime** プロパティを追加し、この列が協定世界時 (UTC) の日時値として値を格納するように MAPI 名前空間を指定します。 最後に、テーブルの各アイテムを列挙し、テーブルの列として指定された 4 つの各プロパティの値を表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

