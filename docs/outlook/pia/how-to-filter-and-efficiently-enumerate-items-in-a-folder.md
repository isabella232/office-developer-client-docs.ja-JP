---
title: フォルダーのアイテムをフィルター処理して効率よく列挙する
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35215c24a9b953bf8406b268a6169abbd536202b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320308"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="bb400-102">フォルダーのアイテムをフィルター処理して効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="bb400-102">Filter and efficiently enumerate items in a folder</span></span>

<span data-ttu-id="bb400-103">この例では、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを使用して受信トレイ内の添付ファイルがあるアイテムをフィルター処理し、そのようなアイテムを効率よく列挙して、各アイテムの選択されたプロパティを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bb400-103">This example shows how to use the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to filter for items in the Inbox that have attachments, and efficiently enumerate such items, displaying selected properties for each item.</span></span>

## <a name="example"></a><span data-ttu-id="bb400-104">例</span><span class="sxs-lookup"><span data-stu-id="bb400-104">Example</span></span>

<span data-ttu-id="bb400-105">このコード サンプルでは、MAPI 名前空間でプロパティ **PR\_HASATTACH** を指定し、このプロパティを使用して受信トレイの [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドで初期フィルターを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb400-105">The code sample specifies the property **PR\_HASATTACH** with the MAPI namespace, and uses the property to create the initial filter in the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox.</span></span> <span data-ttu-id="bb400-106">アイテムの種類に対する **Table** オブジェクトには、そのアイテムの種類の特定のプロパティを表す既定の列があります。</span><span class="sxs-lookup"><span data-stu-id="bb400-106">A **Table** object for an item type has default columns representing certain properties of that item type.</span></span> <span data-ttu-id="bb400-107">列をカスタマイズするため、この例では最初にその [Table](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) の [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) コレクションで **RemoveAll** メソッドを呼び出してから、 [Columns](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) コレクションで **Add** メソッドを呼び出し、組み込みのプロパティ名と、現地時間で日時が表現された値を格納する **ReceivedTime** を使用して、 **EntryID**、 **Subject**、 **ReceivedTime** の各プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="bb400-107">To customize the columns, this example first calls the [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) method on the [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) collection of that **Table**, and then calls the [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method on the **Columns** collection to add the **EntryID**, **Subject**, and **ReceivedTime** properties using the built-in property names, with the **ReceivedTime** column storing values in local date-time representation.</span></span> 

<span data-ttu-id="bb400-108">次に、 **Columns.Add** を再び呼び出して **ReceiveTime** プロパティを追加し、この列が協定世界時 (UTC) の日時値として値を格納するように MAPI 名前空間を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb400-108">The example then calls **Columns.Add** one more time to add the **ReceiveTime** property specifying its MAPI namespace so that this column will store the value as a Universal Coordinated Time (UTC) date-time value.</span></span> <span data-ttu-id="bb400-109">最後に、テーブルの各アイテムを列挙し、テーブルの列として指定された 4 つの各プロパティの値を表示します。</span><span class="sxs-lookup"><span data-stu-id="bb400-109">Finally, the example enumerates each item in the Table, displaying the value of each of the four properties specified as the table columns.</span></span>

<span data-ttu-id="bb400-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb400-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bb400-111">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb400-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bb400-112">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bb400-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="bb400-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb400-113">See also</span></span>

- [<span data-ttu-id="bb400-114">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="bb400-114">Search and filter</span></span>](search-and-filter.md)

