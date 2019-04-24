---
title: フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acb6f6807f956ee6d468d3fcefc2cdd27732ab9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320322"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する

この例では、フォルダー内のアイテムの列挙時に、複数値プロパティをフィルター処理して表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトのアイテム データのセットを表します。バイナリ、日付、または複数値のプロパティが **Table** オブジェクトに最初に追加されると、そのプロパティの参照方法によってプロパティの型と書式が変わります。組み込みの名前による参照では、名前空間による参照の場合とは異なる列値が返されることがあるので、明示的な組み込みの名前 (ある場合) と名前空間 (明示的な組み込みの名前の有無とは無関係) のどちらでプロパティを参照するか確認する必要があります。以下の表は、プロパティの元の型別に、プロパティ値表現 (型および書式) の相違を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>型</p></th>
<th><p>指定したプロパティで組み込みの名前を使用した場合の戻り値の型</p></th>
<th><p>指定したプロパティで名前空間を使用した場合の戻り値の型</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>バイナリ <b>(PT_BINARY)</b></p></td>
<td><p>文字列</p></td>
<td><p>バイト配列</p></td>
</tr>
<tr class="even">
<td><p>日付 <b>(PT_SYSTIME)</b></p></td>
<td><p>ローカル <b>DateTime</b></p></td>
<td><p>UTC <b>DateTime</b></p></td>
</tr>
<tr class="odd">
<td><p><b>Categories</b> プロパティなどの複数値 (キーワード型ともいいます) <b>(PT_MV_STRING8)</b></p></td>
<td><p>コンマで区切られた値が含まれる文字列</p></td>
<td><p>キーワードごとに 1 つの要素が含まれる 1 次元配列</p></td>
</tr>
</tbody>
</table>


次のコード例は、MAPI 文字列名前空間のプロパティを **Table** オブジェクトに追加する方法、および [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) オブジェクトに返される値が複数値プロパティでどのように変化するかを示します。 TableMultiValuedProperties プロシージャでは、[Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) プロパティが null 参照ではない行について **Table** オブジェクトをフィルター処理します。 **Categories** プロパティは MAPI 文字列名前空間を使用するプロパティで表されます。 分類項目が含まれるアイテムを処理する DAV Searching and Locating (DASL) フィルターを作成します (実際のフィルターは、null 参照ではない分類項目を返します)。 次に、型指定子 0000001f と categoriesProperty 定数を連結して、**Table** オブジェクトに **Categories** 列を追加します。 最後に、**Categories** プロパティを表す **Column** オブジェクトに 1 次元文字列配列が含まれます。この配列の各要素は、アイテムに割り当てられた分類項目を表します。 アイテムの **Categories** プロパティと **Subject** プロパティの両方を、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "https://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

