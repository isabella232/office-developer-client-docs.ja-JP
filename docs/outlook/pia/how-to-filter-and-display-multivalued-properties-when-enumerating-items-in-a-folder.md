---
title: フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: bb1abdeb97e15225e77f9e04a4c34e91e70a533a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407458"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="7b286-102">フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="7b286-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="7b286-103">この例では、フォルダー内のアイテムの列挙時に、複数値プロパティをフィルター処理して表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7b286-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="7b286-104">例</span><span class="sxs-lookup"><span data-stu-id="7b286-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7b286-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="7b286-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="7b286-p101">[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトのアイテム データのセットを表します。バイナリ、日付、または複数値のプロパティが **Table** オブジェクトに最初に追加されると、そのプロパティの参照方法によってプロパティの型と書式が変わります。組み込みの名前による参照では、名前空間による参照の場合とは異なる列値が返されることがあるので、明示的な組み込みの名前 (ある場合) と名前空間 (明示的な組み込みの名前の有無とは無関係) のどちらでプロパティを参照するか確認する必要があります。以下の表は、プロパティの元の型別に、プロパティ値表現 (型および書式) の相違を示します。</span><span class="sxs-lookup"><span data-stu-id="7b286-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format. Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name). The following table shows the difference in the property value representation (in terms of type and format) per original property type.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b286-110">型</span><span class="sxs-lookup"><span data-stu-id="7b286-110">Type</span></span></p></th>
<th><p><span data-ttu-id="7b286-111">指定したプロパティで組み込みの名前を使用した場合の戻り値の型</span><span class="sxs-lookup"><span data-stu-id="7b286-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="7b286-112">指定したプロパティで名前空間を使用した場合の戻り値の型</span><span class="sxs-lookup"><span data-stu-id="7b286-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b286-113">バイナリ <b>(PT_BINARY)</b></span><span class="sxs-lookup"><span data-stu-id="7b286-113">Binary (<b>PT_BINARY</b>)</span></span></p></td>
<td><p><span data-ttu-id="7b286-114">文字列</span><span class="sxs-lookup"><span data-stu-id="7b286-114">String</span></span></p></td>
<td><p><span data-ttu-id="7b286-115">バイト配列</span><span class="sxs-lookup"><span data-stu-id="7b286-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b286-116">日付 <b>(PT_SYSTIME)</b></span><span class="sxs-lookup"><span data-stu-id="7b286-116">Date (<b>PT_SYSTIME</b>)</span></span></p></td>
<td><p><span data-ttu-id="7b286-117">ローカル <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="7b286-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="7b286-118">UTC <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="7b286-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b286-119"><b>Categories</b> プロパティなどの複数値 (キーワード型ともいいます) <b>(PT_MV_STRING8)</b></span><span class="sxs-lookup"><span data-stu-id="7b286-119">Multivalued (also known as keyword type) such as <b>Categories</b> property (<b>PT_MV_STRING8</b>)</span></span></p></td>
<td><p><span data-ttu-id="7b286-120">コンマで区切られた値が含まれる文字列</span><span class="sxs-lookup"><span data-stu-id="7b286-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="7b286-121">キーワードごとに 1 つの要素が含まれる 1 次元配列</span><span class="sxs-lookup"><span data-stu-id="7b286-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7b286-122">次のコード例は、MAPI 文字列名前空間のプロパティを **Table** オブジェクトに追加する方法、および [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) オブジェクトに返される値が複数値プロパティでどのように変化するかを示します。</span><span class="sxs-lookup"><span data-stu-id="7b286-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="7b286-123">TableMultiValuedProperties プロシージャでは、[Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) プロパティが null 参照ではない行について **Table** オブジェクトをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7b286-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="7b286-124">**Categories** プロパティは MAPI 文字列名前空間を使用するプロパティで表されます。</span><span class="sxs-lookup"><span data-stu-id="7b286-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="7b286-125">分類項目が含まれるアイテムを処理する DAV Searching and Locating (DASL) フィルターを作成します (実際のフィルターは、null 参照ではない分類項目を返します)。</span><span class="sxs-lookup"><span data-stu-id="7b286-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="7b286-126">次に、型指定子 0000001f と categoriesProperty 定数を連結して、**Table** オブジェクトに **Categories** 列を追加します。</span><span class="sxs-lookup"><span data-stu-id="7b286-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="7b286-127">最後に、**Categories** プロパティを表す **Column** オブジェクトに 1 次元文字列配列が含まれます。この配列の各要素は、アイテムに割り当てられた分類項目を表します。</span><span class="sxs-lookup"><span data-stu-id="7b286-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="7b286-128">アイテムの **Categories** プロパティと **Subject** プロパティの両方を、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="7b286-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="7b286-129">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b286-129">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="7b286-130">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b286-130">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="7b286-131">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7b286-131">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="7b286-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b286-132">See also</span></span>

- [<span data-ttu-id="7b286-133">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="7b286-133">Search and Filter</span></span>](search-and-filter.md)

