---
title: OpenReport マクロ アクション
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288351"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="b410e-102">OpenReport マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b410e-102">OpenReport macro action</span></span>

<span data-ttu-id="b410e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b410e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b410e-p101">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer. You can also restrict the records that are printed in the report.</span><span class="sxs-lookup"><span data-stu-id="b410e-p101">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer. You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="b410e-106">Setting</span><span class="sxs-lookup"><span data-stu-id="b410e-106">Setting</span></span>

<span data-ttu-id="b410e-107">"OpenReport/レポートを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b410e-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b410e-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b410e-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b410e-109">説明</span><span class="sxs-lookup"><span data-stu-id="b410e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b410e-110">レポート名</span><span class="sxs-lookup"><span data-stu-id="b410e-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="b410e-111">開くレポートの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b410e-111">The name of the report to open.</span></span> <span data-ttu-id="b410e-112">[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>レポート名</strong>] ボックスには、カレント データベース内のビューがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="b410e-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="b410e-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="b410e-113">This is a required argument.</span></span> <span data-ttu-id="b410e-114">ライブラリ データベースで OpenReport アクションが定義されているマクロを実行すると、この名前のレポートが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="b410e-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b410e-115">View</span><span class="sxs-lookup"><span data-stu-id="b410e-115">View</span></span></p></td>
<td><p><span data-ttu-id="b410e-p103">レポートを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで [ <strong>印刷</strong>] (レポートをすぐに印刷する場合)、[ <strong>デザイン</strong>]、または [ <strong>印刷プレビュー</strong>] をクリックします。既定値は [ <strong>印刷</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="b410e-p103">The view in which the report will open. Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box. The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b410e-119">Filter Name/フィルター名</span><span class="sxs-lookup"><span data-stu-id="b410e-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="b410e-p104">A filter that restricts the report's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b410e-p104">A filter that restricts the report's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b410e-123">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="b410e-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="b410e-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span><span class="sxs-lookup"><span data-stu-id="b410e-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="b410e-125">"filter Name/フィルター名" 引数を使用してフィルターを選択すると、この where 句がフィルターの結果に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b410e-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="b410e-126">レポートを開いて、フォームのコントロールの値で指定されたレコードにレコードを制限するには、次の式を使用します。</span><span class="sxs-lookup"><span data-stu-id="b410e-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="b410e-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="b410e-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="b410e-128">引数<em>fieldname</em>を、開いているレポートの基になるテーブルまたはクエリのフィールドの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="b410e-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="b410e-129"><em>formname</em>および<em>controlname on form</em>を、フォームの名前と、レポート内のレコードが一致するようにする値を含むフォームのコントロールに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="b410e-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="b410e-130"><b>注</b>: "Where Condition/Where 条件式" 引数の最大長は255文字です。</span><span class="sxs-lookup"><span data-stu-id="b410e-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="b410e-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span><span class="sxs-lookup"><span data-stu-id="b410e-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="b410e-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span><span class="sxs-lookup"><span data-stu-id="b410e-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b410e-133">Window Mode/ウィンドウ モード</span><span class="sxs-lookup"><span data-stu-id="b410e-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="b410e-134">レポートを開くときのモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="b410e-134">The mode in which the report will open.</span></span> <span data-ttu-id="b410e-135">[ <strong>ウィンドウ モード</strong>] ボックスで、[ <strong>標準</strong>]、[ <strong>非表示</strong>]、[ <strong>アイコン</strong>]、または [ <strong>ダイアログ</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b410e-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="b410e-136">既定値は [ <strong>標準</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="b410e-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="b410e-137"><b>注</b>: 一部のウィンドウモード引数の設定は、タブ付きドキュメントを使用している場合は適用されません。</span><span class="sxs-lookup"><span data-stu-id="b410e-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="b410e-138">ウィンドウを重ねて表示するように切り替えるには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b410e-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="b410e-139">[<strong>オプション</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b410e-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b410e-140">[ <strong>Access のオプション</strong>] ダイアログ ボックスの [ <strong>カレント データベース</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b410e-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b410e-141">[ <strong>アプリケーション オプション</strong>] の [ <strong>ドキュメント ウィンドウ オプション</strong>] で [ <strong>ウィンドウを重ねて表示する</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b410e-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b410e-142">[ <strong>OK</strong>] をクリックし、データベースを閉じて再度開きます。</span><span class="sxs-lookup"><span data-stu-id="b410e-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b410e-143">注釈</span><span class="sxs-lookup"><span data-stu-id="b410e-143">Remarks</span></span>

<span data-ttu-id="b410e-144">" **View/ビュー** " 引数で [ **印刷**] を選択すると、現在のプリンター設定を使用してすぐにレポートが印刷されますが、[ **印刷**] ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="b410e-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="b410e-145">また、" **OpenReport/レポートを開く** " アクションを使用すると、レポートを開いて設定した後に、 PrintOut アクションを使用してレポートを印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="b410e-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="b410e-146">たとえば、印刷前に、レポートを修正したり、" **PrintOut/印刷** " アクションを使用してプリンター設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b410e-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="b410e-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span><span class="sxs-lookup"><span data-stu-id="b410e-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="b410e-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span><span class="sxs-lookup"><span data-stu-id="b410e-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="b410e-149">複数のデータ セットに対して、類似したレポートを印刷するには、フィルターまたは WHERE 句を使用してレポートに印刷するレコードを制限します。</span><span class="sxs-lookup"><span data-stu-id="b410e-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="b410e-150">その後、マクロを編集して別のフィルターを適用するか、"Where Condition/Where 条件式" 引数を変更します。</span><span class="sxs-lookup"><span data-stu-id="b410e-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="b410e-p112">レポートをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、レポートをレポート ビューで開く "OpenReport/レポートを開く" アクションが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b410e-p112">You can drag a report from the Navigation Pane to a macro action row. This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="b410e-153">例</span><span class="sxs-lookup"><span data-stu-id="b410e-153">Example</span></span>

<span data-ttu-id="b410e-154">次の例では、 OpenReport アクションを使用して、レポートを開くときにフィルターを適用するパラメーターを渡す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b410e-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="b410e-155">**rptchapters**レポートには、 **cboAuthors**コンボボックスで選択されたアイテムを selectedauthor パラメーターに渡すことで、指定された作成者のレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b410e-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="b410e-156">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="b410e-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
