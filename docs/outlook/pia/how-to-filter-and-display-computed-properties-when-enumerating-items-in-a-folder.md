---
title: フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 946858221b649cd6189ddf44680b316554cab5de
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723076"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="1c013-102">フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="1c013-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="1c013-103">この例では、フォルダー内のアイテムの列挙時に、計算されたプロパティをフィルター処理して表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1c013-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="1c013-104">例</span><span class="sxs-lookup"><span data-stu-id="1c013-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1c013-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="1c013-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="1c013-p101">[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトからのアイテム データの集まりを表します。 [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) オブジェクトは、 **Table** 内のデータの行を表します。 [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) オブジェクトは、 **Table** のプロパティを表します。 **Columns** オブジェクトの [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) メソッドを使用すると、 **Table** オブジェクトに一部のプロパティを追加できます。 [Table](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) オブジェクトの **Restrict(String)** メソッドを使用すると、一部のプロパティをフィルター処理できます。ただし、 **Columns.Add** を使用して **Table** オブジェクトに追加したり、 **Restrict** メソッドを使用してフィルター処理したりできないプロパティもあります。以下の表は、各プロパティが、 **Columns.Add** メソッドまたは **Restrict** メソッド使用時に **Table** でサポートされるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1c013-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**. The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**. You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object. You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object. However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method. The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c013-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c013-113">Property</span></span></p></th>
<th><p><span data-ttu-id="1c013-114">Columns.Add での使用</span><span class="sxs-lookup"><span data-stu-id="1c013-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="1c013-115">Restrict での使用</span><span class="sxs-lookup"><span data-stu-id="1c013-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c013-116"><b> EntryID</b> などのバイナリ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1c013-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="1c013-117">組み込みまたは名前空間のプロパティを介してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1c013-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="1c013-p102">サポートされません。Outlook でエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c013-p102">Not supported. Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-120">本文のプロパティ ( <b>Body</b>、 <b>HTMLBody</b> など)、およびそれらのプロパティの名前空間表現 ( <b>PR_RTF_COMPRESSED</b> など)</span><span class="sxs-lookup"><span data-stu-id="1c013-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="1c013-121"><b>Body</b> プロパティは、値の先頭 255 バイトのみが <b>Table</b> オブジェクトに格納されるという制限付きで、サポートされます。</span><span class="sxs-lookup"><span data-stu-id="1c013-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="1c013-122">HTML または RTF 形式の本文のコンテンツを示すその他のプロパティはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c013-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="1c013-123"><b>Body</b> の先頭 255 バイトのみが返されることになるので、テキストまたは HTML でアイテムの本文全体のコンテンツを取得したい場合は、<b>GetItemFromID(文字列、オブジェクト)</b> メソッドでアイテムの <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">EntryID</a> を使用してアイテム オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="1c013-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="1c013-124"><b>Body</b> の完全な値をアイテム オブジェクトを使って取得します。</span><span class="sxs-lookup"><span data-stu-id="1c013-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="1c013-125">テキストで表される <b>Body</b> プロパティのみフィルターでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1c013-125">Only the <b>Body</b> property represented in text is supported in a filter.</span></span> <span data-ttu-id="1c013-126">したがって、DAV Searching and Locating (DASL) フィルターでは、このプロパティは <em>urn:schemas:http-mail:textdescription</em> として参照される必要があり、本文内の HTML タグはフィルター処理できません。</span><span class="sxs-lookup"><span data-stu-id="1c013-126">This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body.</span></span> <span data-ttu-id="1c013-127">パフォーマンスを向上させるには、本文内の文字列に一致するようにフィルター処理でコンテキスト インデクサー キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c013-127">To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c013-128">計算されたプロパティ ( <b>AutoResolvedWinner</b>、 <b>BodyFormat</b> など)</span><span class="sxs-lookup"><span data-stu-id="1c013-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="1c013-129">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c013-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="1c013-130">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c013-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-131">複数値プロパティ ( <b>Categories</b>、 <b>Children</b>、 <b>Companies</b>、 <b>VotingOptions</b> など)</span><span class="sxs-lookup"><span data-stu-id="1c013-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="1c013-132">サポートされています。</span><span class="sxs-lookup"><span data-stu-id="1c013-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="1c013-133">サポートされます。ただし、DASL クエリの作成には名前空間表現を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c013-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c013-134">オブジェクトを返すプロパティ ( <b>Attachments</b>、 <b>Parent</b>、 <b>Recipients</b>、 <b>RecurrencePattern</b>、 <b>UserProperties</b> など)</span><span class="sxs-lookup"><span data-stu-id="1c013-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="1c013-135">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c013-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="1c013-136">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c013-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c013-p105">以下の表は、 **Columns.Add** を使用して **Table** オブジェクトに追加できない既知のプロパティの一覧を示します。この一覧にあるプロパティを追加しようとすると、Outlook でエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1c013-p105">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**. If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c013-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="1c013-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="1c013-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="1c013-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="1c013-141">Class</span><span class="sxs-lookup"><span data-stu-id="1c013-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-142">Companies</span><span class="sxs-lookup"><span data-stu-id="1c013-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="1c013-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="1c013-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="1c013-144">DLName</span><span class="sxs-lookup"><span data-stu-id="1c013-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c013-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="1c013-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="1c013-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="1c013-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="1c013-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="1c013-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="1c013-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="1c013-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="1c013-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="1c013-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="1c013-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c013-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="1c013-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="1c013-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="1c013-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="1c013-153">Permission</span><span class="sxs-lookup"><span data-stu-id="1c013-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="1c013-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="1c013-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="1c013-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="1c013-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="1c013-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c013-157">Saved</span><span class="sxs-lookup"><span data-stu-id="1c013-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="1c013-158">Sent</span><span class="sxs-lookup"><span data-stu-id="1c013-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="1c013-159">Submitted</span><span class="sxs-lookup"><span data-stu-id="1c013-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c013-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="1c013-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="1c013-161">Unread</span><span class="sxs-lookup"><span data-stu-id="1c013-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="1c013-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="1c013-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c013-163">一部の計算済みのプロパティは、テーブルの列セットに追加することはできませんが、次のコード例はこの制限を回避して動作します。</span><span class="sxs-lookup"><span data-stu-id="1c013-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="1c013-164">**表**に表示されるアイテムを制限するために GetToDoItems は、DASL クエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c013-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="1c013-165">計算済みのプロパティが、名前空間を表現したものを持つ場合、その名前空間を表現したものは、計算済みのプロパティの指定された値の行に戻るため、**表**オブジェクトを表現する DASL クエリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c013-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="1c013-166">GetToDoItems は、[IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) プロパティが **true** と等しく、また [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\))、[TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\))、[TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\))、[TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)) のような特定のタスク プロパティに値を割り当てる受信トレイにアイテムを取得します。</span><span class="sxs-lookup"><span data-stu-id="1c013-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="1c013-167">最後に、これらのプロパティを、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1c013-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="1c013-168">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1c013-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1c013-169">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c013-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1c013-170">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1c013-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "https://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "https://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1c013-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c013-171">See also</span></span>

- [<span data-ttu-id="1c013-172">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="1c013-172">Search and filter</span></span>](search-and-filter.md)

