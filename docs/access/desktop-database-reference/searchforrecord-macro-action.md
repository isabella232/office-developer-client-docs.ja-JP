---
title: SearchForRecord マクロ アクション
TOCTitle: SearchForRecord Macro Action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 21efa96338363646be826248e6c9ca0b951496c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476617"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="186c9-102">SearchForRecord マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="186c9-102">SearchForRecord Macro Action</span></span>


<span data-ttu-id="186c9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="186c9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="186c9-104">**SearchForRecord** アクションは、テーブル、クエリ、フォーム、またはレポート内の特定のレコードを検索するために使用します。</span><span class="sxs-lookup"><span data-stu-id="186c9-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="186c9-105">設定</span><span class="sxs-lookup"><span data-stu-id="186c9-105">Setting</span></span>

<span data-ttu-id="186c9-106">**SearchForRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="186c9-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="186c9-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="186c9-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="186c9-108">説明</span><span class="sxs-lookup"><span data-stu-id="186c9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="186c9-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-p101">検索先のデータベース オブジェクトの種類を入力または選択します。[ <strong>テーブル</strong> ]、[ <strong>クエリ</strong> ]、[ <strong>フォーム</strong> ]、[ <strong>レポート</strong> ] のいずれかを選択できます。  </span><span class="sxs-lookup"><span data-stu-id="186c9-p101">Enter or select the type of database object that you are searching in. You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186c9-112"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-p102">検索対象のレコードが含まれている特定のオブジェクトを入力または選択します。ドロップダウン リストには、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のデータベース オブジェクトがすべて表示されます。  </span><span class="sxs-lookup"><span data-stu-id="186c9-p102">Enter or select the specific object that contains the record to search for. The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="186c9-115"><strong>レコード/Record</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-116">検索の開始点と方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="186c9-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="186c9-117">設定</span><span class="sxs-lookup"><span data-stu-id="186c9-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="186c9-118">説明</span><span class="sxs-lookup"><span data-stu-id="186c9-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="186c9-119"><strong>Previous/前のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-120">カレント レコードから前方へ検索します。</span><span class="sxs-lookup"><span data-stu-id="186c9-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186c9-121"><strong>Next/次のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-122">カレント レコードから後方へ検索します。</span><span class="sxs-lookup"><span data-stu-id="186c9-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="186c9-123"><strong>First/先頭のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-p103">最初のレコードから後方へ検索します。この引数の既定値です。</span><span class="sxs-lookup"><span data-stu-id="186c9-p103">Search forward from the first record. This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186c9-126"><strong>Last/最後のレコード</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-127">最後のレコードから前方へ検索します。</span><span class="sxs-lookup"><span data-stu-id="186c9-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186c9-128"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-129">SQL の WHERE 句、のみなしの word と同じ構文を使用して検索の条件を入力してください&quot;、&quot;。</span><span class="sxs-lookup"><span data-stu-id="186c9-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="186c9-130">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="186c9-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="186c9-131">フォームのテキスト ボックスにある値を含む条件を作成するには、条件の最初の部分と、検索対象の値を含むテキスト ボックスの名前を連結する式を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="186c9-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="186c9-132">たとえば、次の条件では、"説明" フィールドで frmCategories というフォーム上の txtDescription というテキスト ボックスに含まれる値を検索します。</span><span class="sxs-lookup"><span data-stu-id="186c9-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="186c9-133">等号 (=) に注意してください (<strong>=</strong>) の式、およびテキスト ボックス参照の両側に単一引用符 (<strong>'</strong>) の先頭にします。</span><span class="sxs-lookup"><span data-stu-id="186c9-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="186c9-134">解説</span><span class="sxs-lookup"><span data-stu-id="186c9-134">Remarks</span></span>

- <span data-ttu-id="186c9-135">複数のレコードが **Where Condition/Where 条件式** 引数の条件と一致した場合は、次の要因によって、検出されるレコードが決まります。</span><span class="sxs-lookup"><span data-stu-id="186c9-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="186c9-136">**Record/レコード引数の設定: \*\*\*\*Record/レコード**引数の詳細については、「設定値」セクションの表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="186c9-136">**The Record argument setting**See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="186c9-137">**レコードの並べ替え順序: **たとえば、**Record/レコード**引数が [**先頭のレコード**] に設定されている場合、レコードの並べ替え順序を変更すると、検出されるレコードが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="186c9-137">**The sort order of the records**For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="186c9-p106">**Object Name/オブジェクト名** 引数で指定されたオブジェクトは、このアクションが実行される前に開いておく必要があります。開かれていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="186c9-p106">The object specified in the **Object Name** argument must be open before this action is run. Otherwise, an error occurs.</span></span>

- <span data-ttu-id="186c9-140">**Where Condition/Where 条件式** 引数の条件と一致するレコードがなくても、エラーは発生せず、フォーカスはカレント レコードに置かれたままになります。</span><span class="sxs-lookup"><span data-stu-id="186c9-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="186c9-p107">前のレコードまたは次のレコードを検索する場合、データの先頭または末尾まで検索すると、そこで終了します。条件に一致するレコードがなくても、エラーは発生せず、フォーカスはカレント レコードに置かれたままになります。条件と一致するレコードが見つかったことを確認するには、次のアクションの条件を入力し、その条件を **Where Condition/Where 条件式** 引数の条件と同じにします。</span><span class="sxs-lookup"><span data-stu-id="186c9-p107">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data. If there are no further records that match the criteria, no error occurs and the focus remains on the current record. To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="186c9-144">VBA モジュールで **SearchForRecord** アクションを実行するには、 **DoCmd** オブジェクトの **SearchForRecord** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="186c9-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="186c9-p108">**SearchForRecord** アクションは、 **[FindRecord](findrecord-macro-action.md)** アクションと似ていますが、 **SearchForRecord** アクションの検索機能の方が強力です。 **FindRecord** アクションは、主に文字列の検索に使用され、その機能は [ **検索**] ダイアログ ボックスの機能と同じです。 **SearchForRecord** アクションでは、フィルターまたは SQL クエリのように機能する条件が使用されます。次の一覧は、 **SearchForRecord** アクションで実行できるいくつかの操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="186c9-p108">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features. The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box. The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query. The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="186c9-149">**Where Condition/Where 条件式** 引数では、次に示すような複雑な条件を使用できます。</span><span class="sxs-lookup"><span data-stu-id="186c9-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="186c9-p109">フォームまたはレポートのレコード ソース内にあってもフォームまたはレポートには表示されないフィールドを参照できます。前の例では、フォームまたはレポートに Description も CategoryID も表示されない場合でも、条件は機能します。</span><span class="sxs-lookup"><span data-stu-id="186c9-p109">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report. In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="186c9-p110">**\<** 、 **\>** 、 **AND** 、 **OR** 、 **BETWEEN** などの論理演算子を使用できます。 **FindRecord** アクションでは、検索対象の文字列と完全に一致する文字列、検索対象の文字列で始まる文字列、検索対象の文字列を含む文字列のみが検索されます。</span><span class="sxs-lookup"><span data-stu-id="186c9-p110">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**. The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="186c9-154">例</span><span class="sxs-lookup"><span data-stu-id="186c9-154">Example</span></span>

<span data-ttu-id="186c9-p111">次のマクロは、まず **OpenTable** アクションを使用して [商品区分] テーブルを開きます。次に、 **SearchForRecord** アクションを使用して、テーブル内で [説明] フィールドが "飲料" である最初のレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="186c9-p111">The following macro first opens the Categories table by using the **OpenTable** action. The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="186c9-157">アクション</span><span class="sxs-lookup"><span data-stu-id="186c9-157">Action</span></span></p></th>
<th><p><span data-ttu-id="186c9-158">引数</span><span class="sxs-lookup"><span data-stu-id="186c9-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="186c9-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-160"><strong>テーブル名</strong>: カテゴリの<strong>表示</strong>: <strong>DatasheetData モード</strong>:<strong>編集</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="186c9-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="186c9-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="186c9-162"><strong>オブジェクトの種類</strong>:<strong>大域オフセットテーブルオブジェクトファイル名前</strong>: カテゴリ<strong>レコード</strong>: <strong>FirstWhere の状態</strong>: 説明 =&quot;飲料&quot;</span><span class="sxs-lookup"><span data-stu-id="186c9-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

