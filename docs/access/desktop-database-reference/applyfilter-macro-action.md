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
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296998"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="f9b99-102">ApplyFilter マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="f9b99-102">ApplyFilter macro action</span></span>

<span data-ttu-id="f9b99-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9b99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9b99-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span><span class="sxs-lookup"><span data-stu-id="f9b99-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="f9b99-p102">[!メモ] このアクションは、サーバー フィルターを使用する場合のみ、SQL WHERE 句を適用するために使用します。サーバー フィルターは、保存されているプロシージャのレコード ソースには適用できません。</span><span class="sxs-lookup"><span data-stu-id="f9b99-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="f9b99-108">Setting</span><span class="sxs-lookup"><span data-stu-id="f9b99-108">Setting</span></span>

<span data-ttu-id="f9b99-109">"ApplyFilter/フィルターの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f9b99-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9b99-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="f9b99-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f9b99-111">説明</span><span class="sxs-lookup"><span data-stu-id="f9b99-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9b99-112">Filter Name/フィルター名</span><span class="sxs-lookup"><span data-stu-id="f9b99-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="f9b99-p103">テーブル、フォーム、またはレポートのレコードの制限または並べ替えを行うフィルターまたはクエリの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションの [ <strong>フィルター名</strong>] ボックスに、既存のクエリ、またはクエリとして保存されているフィルターの名前を入力できます。  </span><span class="sxs-lookup"><span data-stu-id="f9b99-p103">The name of a filter or query that restricts or sorts the records of the table, form, or report. You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="f9b99-115"><strong>注</strong>: このアクションを使用してサーバーフィルターを適用する場合は、"filter Name/フィルター名" 引数を空白にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b99-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9b99-116">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="f9b99-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="f9b99-117">テーブル、フォーム、またはレポートのレコードを制限するための有効な SQL WHERE 句 (WHERE という単語は除く) または式を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9b99-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="f9b99-118"><b>注</b>: Where Condition/Where 条件式引数式では、通常、フォームまたはレポートの基になるテーブルまたはクエリのフィールド名が式の左側に格納されます。</span><span class="sxs-lookup"><span data-stu-id="f9b99-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="f9b99-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span><span class="sxs-lookup"><span data-stu-id="f9b99-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="f9b99-120">このコントロール名は、完全な名前で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b99-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="f9b99-121">たとえば、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="f9b99-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="f9b99-122"><strong>フォーム</strong><em>formname</em>!<em>controlname</em>フィールド名は二重引用符で囲む必要があり、リテラル文字列は一重引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b99-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="f9b99-123">引数 Where Condition の最大長は255文字です。</span><span class="sxs-lookup"><span data-stu-id="f9b99-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="f9b99-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span><span class="sxs-lookup"><span data-stu-id="f9b99-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="f9b99-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span><span class="sxs-lookup"><span data-stu-id="f9b99-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f9b99-126">適切なデータを提供するフィルターが既に定義されている場合は、"filter Name/フィルター名" 引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9b99-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="f9b99-127">制限条件を直接入力する場合は、"Where Condition/Where 条件式" 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9b99-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="f9b99-128">両方の引数を指定すると、Microsoft Office Access 2007 では、WHERE 句がフィルターの結果に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f9b99-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="f9b99-129">2 つの引数のうち少なくとも 1 つは指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b99-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b99-130">注釈</span><span class="sxs-lookup"><span data-stu-id="f9b99-130">Remarks</span></span>

<span data-ttu-id="f9b99-131">フィルターまたはクエリは、フォーム ビューまたはデータシート ビューで開いているフォームに適用できます。</span><span class="sxs-lookup"><span data-stu-id="f9b99-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="f9b99-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span><span class="sxs-lookup"><span data-stu-id="f9b99-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="f9b99-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span><span class="sxs-lookup"><span data-stu-id="f9b99-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="f9b99-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span><span class="sxs-lookup"><span data-stu-id="f9b99-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="f9b99-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span><span class="sxs-lookup"><span data-stu-id="f9b99-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="f9b99-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span><span class="sxs-lookup"><span data-stu-id="f9b99-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="f9b99-142">例</span><span class="sxs-lookup"><span data-stu-id="f9b99-142">Example</span></span>

<span data-ttu-id="f9b99-143">次の例では、ApplyFilter アクションを使用し、frmFoods フォームを開くときにフィルターを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f9b99-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="f9b99-144">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="f9b99-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



