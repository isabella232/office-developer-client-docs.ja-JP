---
title: ApplyFilter マクロ アクション
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f6f0511a1358e8d9b0d0ee820e83cf59d2400345
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025968"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="9e5d2-102">ApplyFilter マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="9e5d2-102">ApplyFilter macro action</span></span>

<span data-ttu-id="9e5d2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e5d2-104">**ApplyFilter**アクションを使用すると、テーブル、フォーム、または、テーブル内のレコードまたはレコードは、基になるテーブルまたはクエリ、フォームまたはレポートの制限または並べ替えをレポートに、フィルター、クエリ、または、SQL WHERE 句を適用します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-104">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report.</span></span> <span data-ttu-id="9e5d2-105">レポート、レポートの **"開く時"** イベント プロパティで指定されたマクロでのみこの操作を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-105">For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="9e5d2-p102">[!メモ] このアクションは、サーバー フィルターを使用する場合のみ、SQL WHERE 句を適用するために使用します。サーバー フィルターは、保存されているプロシージャのレコード ソースには適用できません。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="9e5d2-108">設定値</span><span class="sxs-lookup"><span data-stu-id="9e5d2-108">Setting</span></span>

<span data-ttu-id="9e5d2-109">**データシート**には、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e5d2-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="9e5d2-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9e5d2-111">説明</span><span class="sxs-lookup"><span data-stu-id="9e5d2-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e5d2-112">Filter Name</span><span class="sxs-lookup"><span data-stu-id="9e5d2-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="9e5d2-p103">テーブル、フォーム、またはレポートのレコードの制限または並べ替えを行うフィルターまたはクエリの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションの [ <strong>フィルター名</strong>] ボックスに、既存のクエリ、またはクエリとして保存されているフィルターの名前を入力できます。  </span><span class="sxs-lookup"><span data-stu-id="9e5d2-p103">The name of a filter or query that restricts or sorts the records of the table, form, or report. You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="9e5d2-115"><strong>注</strong>: サーバー フィルターを適用するのにはこのアクションを使用する場合、[フィルター名] 引数が空白する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e5d2-116">Where Condition</span><span class="sxs-lookup"><span data-stu-id="9e5d2-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="9e5d2-117">テーブル、フォーム、またはレポートのレコードを制限するための有効な SQL WHERE 句 (WHERE という単語は除く) または式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="9e5d2-118"><b>注</b>: で、ある条件の引数の式、式の左側にあるには通常、フォームまたはレポートの基になるテーブルまたはクエリのフィールド名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="9e5d2-119">通常、式の右側にあるには、制限するか、レコードを並べ替えるには、このフィールドに適用する条件が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="9e5d2-120">などの条件と一致する最初のフォーム内のレコードが必要な値を格納する別のフォーム上のコントロールの名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="9e5d2-121">コントロールの名前は、たとえば、完全修飾にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="9e5d2-122"><strong>フォーム</strong>です。<em>フォーム名</em>です。<em>controlname</em>フィールド名を二重引用符で囲む必要があり、文字列リテラルは単一引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="9e5d2-123">条件式の最大長は、255 文字です。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="9e5d2-124">長い SQL WHERE 句を入力する場合はで Visual Basic for Applications (VBA) モジュールの<strong>DoCmd</strong>オブジェクトの<strong>ApplyFilter</strong>メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="9e5d2-125">VBA では、SQL 句のステートメントの最大 32,768 文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9e5d2-126">適切なデータを提供するフィルターが既に定義されている場合は、フィルター名の引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="9e5d2-127">制限条件を直接入力するのに条件式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="9e5d2-128">両方の引数を指定すると、Microsoft Office Access 2007 では、WHERE 句がフィルターの結果に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="9e5d2-129">2 つの引数のうち少なくとも 1 つは指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5d2-130">解説</span><span class="sxs-lookup"><span data-stu-id="9e5d2-130">Remarks</span></span>

<span data-ttu-id="9e5d2-131">フィルターまたはクエリは、フォーム ビューまたはデータシート ビューで開いているフォームに適用できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="9e5d2-132">フィルターおよび WHERE 条件式を指定するフォームまたはレポートの**フィルター**または**フォーム**のプロパティの設定になります。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="9e5d2-133">テーブルおよびフォームでは、この操作は、[**レコード**] メニューの **[フィルター/並べ替えの実行**または**サーバー フィルターの適用**] をクリックすると同様です。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-133">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu.</span></span> <span data-ttu-id="9e5d2-134">メニュー コマンドは、 **ApplyFilter**アクションには、指定したフィルターまたはクエリが適用されますが、テーブルまたはフォームに最も新しく作成されたフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-134">The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="9e5d2-135">、Access データベースの [**レコード**] メニューの [**フィルター** ] をポイントし、[フィルター/並べ替えの編集ウィンドウに表示フィルターの条件、 **ApplyFilter**アクションを実行した後、 **[フィルター/並べ替えの編集**] をクリックしてオンにした場合にこのアクションです。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="9e5d2-136">フィルターを削除し、Office Access 2007 データベース内のすべてのテーブルまたはフォームのレコードを表示、[**レコード**] メニューには、**解除**、または、[**フィルター/並べ替えの解除**] コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-136">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu.</span></span> <span data-ttu-id="9e5d2-137">Access プロジェクト (.adp) でフィルターを削除するにフォーム サーバー フィルター ウィンドウに戻るとすべてのフィルター条件を削除して、ツールバーの [**レコード**] メニューの [**サーバー フィルターの適用**] をクリックしてしたり、**フォーム サーバー フィルター**のプロパティを設定**False** (0)。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-137">To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="9e5d2-138">テーブルまたはフォームを保存すると、アクセス、そのオブジェクトに現在定義されているすべてのフィルターは保存されることはありませんフィルター自動的に次回オブジェクトを開いたときに自動的に、保存前にオブジェクトに適用した並べ替えに適用されます)。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-138">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved).</span></span> <span data-ttu-id="9e5d2-139">フォームを最初に開いたときに自動的にフィルターを適用するには、**データシート**または**Open**イベントが発生する**DoCmd**オブジェクトの**ApplyFilter**メソッドを含むイベント プロシージャが含まれているマクロを指定します。フォームのプロパティの設定します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-139">If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form.</span></span> <span data-ttu-id="9e5d2-140">**OpenForm**または**OpenReport**アクション、または、対応するメソッドを使用してフィルターを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-140">You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods.</span></span> <span data-ttu-id="9e5d2-141">テーブルを最初に開いたときに自動的にフィルターを適用するには、**データシート**の直後、 **OpenTable**アクションを含むマクロを使用してテーブルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-141">To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="9e5d2-142">使用例</span><span class="sxs-lookup"><span data-stu-id="9e5d2-142">Example</span></span>

<span data-ttu-id="9e5d2-143">次の例では、 ApplyFilter アクションを使用し、frmFoods フォームを開くときにフィルターを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="9e5d2-144">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="9e5d2-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



