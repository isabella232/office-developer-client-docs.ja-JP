---
title: フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 228dd7799a2bc0acf41696cc98ae574670c5ea9b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406086"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する

この例では、フォルダー内のアイテムの列挙時に、計算されたプロパティをフィルター処理して表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトからのアイテム データの集まりを表します。 [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) オブジェクトは、 **Table** 内のデータの行を表します。 [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) オブジェクトは、 **Table** のプロパティを表します。 **Columns** オブジェクトの [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) メソッドを使用すると、 **Table** オブジェクトに一部のプロパティを追加できます。 [Table](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) オブジェクトの **Restrict(String)** メソッドを使用すると、一部のプロパティをフィルター処理できます。ただし、 **Columns.Add** を使用して **Table** オブジェクトに追加したり、 **Restrict** メソッドを使用してフィルター処理したりできないプロパティもあります。以下の表は、各プロパティが、 **Columns.Add** メソッドまたは **Restrict** メソッド使用時に **Table** でサポートされるかどうかを示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ</p></th>
<th><p>Columns.Add での使用</p></th>
<th><p>Restrict での使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><b> EntryID</b> などのバイナリ プロパティ。</p></td>
<td><p>組み込みまたは名前空間のプロパティを介してサポートされます。</p></td>
<td><p>サポートされません。Outlook でエラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p>本文のプロパティ ( <b>Body</b>、 <b>HTMLBody</b> など)、およびそれらのプロパティの名前空間表現 ( <b>PR_RTF_COMPRESSED</b> など)</p></td>
<td><p><b>Body</b> プロパティは、値の先頭 255 バイトのみが <b>Table</b> オブジェクトに格納されるという制限付きで、サポートされます。 HTML または RTF 形式の本文のコンテンツを示すその他のプロパティはサポートされていません。 <b>Body</b> の先頭 255 バイトのみが返されることになるので、テキストまたは HTML でアイテムの本文全体のコンテンツを取得したい場合は、<b>GetItemFromID(文字列、オブジェクト)</b> メソッドでアイテムの <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">EntryID</a> を使用してアイテム オブジェクトを取得します。 <b>Body</b> の完全な値をアイテム オブジェクトを使って取得します。</p></td>
<td><p>テキストで表される <b>Body</b> プロパティのみフィルターでサポートされています。 したがって、DAV Searching and Locating (DASL) フィルターでは、このプロパティは <em>urn:schemas:http-mail:textdescription</em> として参照される必要があり、本文内の HTML タグはフィルター処理できません。 パフォーマンスを向上させるには、本文内の文字列に一致するようにフィルター処理でコンテキスト インデクサー キーワードを使用します。</p></td>
</tr>
<tr class="odd">
<td><p>計算されたプロパティ ( <b>AutoResolvedWinner</b>、 <b>BodyFormat</b> など)</p></td>
<td><p>サポートされていません。</p></td>
<td><p>サポートされていません。</p></td>
</tr>
<tr class="even">
<td><p>複数値プロパティ ( <b>Categories</b>、 <b>Children</b>、 <b>Companies</b>、 <b>VotingOptions</b> など)</p></td>
<td><p>サポートされています。</p></td>
<td><p>サポートされます。ただし、DASL クエリの作成には名前空間表現を使用する必要があります。</p></td>
</tr>
<tr class="odd">
<td><p>オブジェクトを返すプロパティ ( <b>Attachments</b>、 <b>Parent</b>、 <b>Recipients</b>、 <b>RecurrencePattern</b>、 <b>UserProperties</b> など)</p></td>
<td><p>サポートされていません。</p></td>
<td><p>サポートされていません。</p></td>
</tr>
</tbody>
</table>


以下の表は、 **Columns.Add** を使用して **Table** オブジェクトに追加できない既知のプロパティの一覧を示します。この一覧にあるプロパティを追加しようとすると、Outlook でエラーが発生します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Class</p></td>
</tr>
<tr class="even">
<td><p>Companies</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Permission</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Sent</p></td>
<td><p>Submitted</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>Unread</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


一部の計算済みのプロパティは、テーブルの列セットに追加することはできませんが、次のコード例はこの制限を回避して動作します。 **表**に表示されるアイテムを制限するために GetToDoItems は、DASL クエリを使用します。 計算済みのプロパティが、名前空間を表現したものを持つ場合、その名前空間を表現したものは、計算済みのプロパティの指定された値の行に戻るため、**表**オブジェクトを表現する DASL クエリを作成するために使用されます。 GetToDoItems は、[IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) プロパティが **true** と等しく、また [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\))、[TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\))、[TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\))、[TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)) のような特定のタスク プロパティに値を割り当てる受信トレイにアイテムを取得します。 最後に、これらのプロパティを、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

