---
title: 先月に変更された受信トレイアイテムをフィルター処理して表示する
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 952d28cc64ffa3638f8147b665e88a372dc81848
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406877"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="f83bd-102">先月に変更された受信トレイアイテムをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="f83bd-102">Filter and display Inbox items modified in the last month</span></span>

<span data-ttu-id="f83bd-103">この例では、先月に変更された受信トレイアイテムをフィルター処理して表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="f83bd-104">例</span><span class="sxs-lookup"><span data-stu-id="f83bd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f83bd-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="f83bd-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="f83bd-106">DAV Search and Locating (DASL) は、Outlook における Microsoft Exchange の DASL 実装に基づくクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="f83bd-106">DAV Searching and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="f83bd-107">[表](https://msdn.microsoft.com/library/bb652856\(v=office.15\))オブジェクトに示されるように、フォルダーのデータ内のプロパティに基づくアイテム レベルの検索結果などを戻すのに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f83bd-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="f83bd-108">DASL フィルターは、等号 (=) 演算子による文字列の比較 (同値、接頭辞、語句、部分文字列の一致) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f83bd-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal ( ) operator.</span></span> <span data-ttu-id="f83bd-109">DASL クエリを使用して、日付と時刻の比較とフィルター処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f83bd-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="f83bd-p102">DASL クエリによる **DateTime** 比較は常に協定世界時 (UTC) で行われるので、クエリを正しく動作させるためには現地時刻を UTC に変換する必要があります。さらに、 **DateTime** 値を文字列表現に変換する必要もあります。DASL フィルターでは文字列による比較が行われるからです。 **DateTime** の変換には次の 2 つの方法があります。1 つは [Row](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) オブジェクトの [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) メソッドによる変換で、もう 1 つは Outlook の **DateTime** マクロによる変換です。</span><span class="sxs-lookup"><span data-stu-id="f83bd-p102">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly. You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons. You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="f83bd-113">次のコードは、 **LocalTimeToUTC** メソッドを使用して **LastModificationTime** プロパティ (すべての **Item** オブジェクトにある既定の列) の値を UTC に変換する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83bd-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="f83bd-114">次の表は、 **DateTime** プロパティの値と UTC の相対日時を比較して文字列をフィルター処理するための **DateTime** マクロです。</span><span class="sxs-lookup"><span data-stu-id="f83bd-114">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC.</span></span> <span data-ttu-id="f83bd-115">SchemaName のプロパティの値は、名前空間で参照される有効な **DateTime** プロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-115">The  SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f83bd-116">マクロ</span><span class="sxs-lookup"><span data-stu-id="f83bd-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="f83bd-117">構文</span><span class="sxs-lookup"><span data-stu-id="f83bd-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="f83bd-118">説明</span><span class="sxs-lookup"><span data-stu-id="f83bd-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-119">today</span><span class="sxs-lookup"><span data-stu-id="f83bd-119">today</span></span></p></td>
<td><p><span data-ttu-id="f83bd-120">%today(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-121">抽出対象を SchemaName プロパティの値が今日と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-121">Restricts for items with a SchemaName property value equal to today.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f83bd-122">tomorrow</span><span class="sxs-lookup"><span data-stu-id="f83bd-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="f83bd-123">%tomorrow(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-124">抽出対象を SchemaName プロパティの値が明日と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-124">Restricts for items with a SchemaName property value equal to tomorrow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-125">yesterday</span><span class="sxs-lookup"><span data-stu-id="f83bd-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="f83bd-126">%yesterday(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-127">抽出対象を SchemaName プロパティの値が昨日と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-127">Restricts for items with a SchemaName property value equal to yesterday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f83bd-128">next7days</span><span class="sxs-lookup"><span data-stu-id="f83bd-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="f83bd-129">%next7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-130">抽出対象をSchemaName プロパティの値の範囲が次の 7 日間と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-131">last7days</span><span class="sxs-lookup"><span data-stu-id="f83bd-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="f83bd-132">%last7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-133">抽出対象をSchemaName プロパティの値の範囲が今日までの7 日間と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f83bd-134">nextweek</span><span class="sxs-lookup"><span data-stu-id="f83bd-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="f83bd-135">%nextweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-136">抽出対象を SchemaName プロパティ値の範囲が来週と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-137">thisweek</span><span class="sxs-lookup"><span data-stu-id="f83bd-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="f83bd-138">%thisweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-139">抽出対象を SchemaName プロパティ値の範囲が今週と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f83bd-140">lastweek</span><span class="sxs-lookup"><span data-stu-id="f83bd-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="f83bd-141">%lastweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-142">抽出対象を SchemaName プロパティ値の範囲が先週と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-143">nextmonth</span><span class="sxs-lookup"><span data-stu-id="f83bd-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="f83bd-144">%nextmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-145">抽出対象を SchemaName プロパティ値の範囲が来月と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f83bd-146">thismonth</span><span class="sxs-lookup"><span data-stu-id="f83bd-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="f83bd-147">%thismonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-148">抽出対象を SchemaName プロパティ値の範囲が今月と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-148">Restricts for items with SchemaName property values in a   range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f83bd-149">lastmonth</span><span class="sxs-lookup"><span data-stu-id="f83bd-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="f83bd-150">%lastmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="f83bd-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="f83bd-151">抽出対象を SchemaName プロパティ値の範囲が先月と等しいアイテムに制限します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f83bd-152">次の例では、DemoDASLDateMacro が **lastmonthDateTime**マクロを使用する DASL クエリを作成し、先月変更されたユーザーの受信トレイ内のアイテムをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-152">In the following example,   creates a DASL query that uses the lastmonth DateTime macro to filter for items in the user's Inbox that were modified in the last month.</span></span> <span data-ttu-id="f83bd-153">次に、作成、**表**オブジェクトをフィルターと共に作成、列挙し、制限された**テーブル**オブジェクトの行を表示します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="f83bd-154">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83bd-154">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f83bd-155">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83bd-155">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f83bd-156">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83bd-156">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f83bd-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="f83bd-157">See also</span></span>

- [<span data-ttu-id="f83bd-158">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="f83bd-158">Search and Filter</span></span>](search-and-filter.md)

