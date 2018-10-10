---
title: "\"OpenReport/レポートを開く\" マクロ アクション"
TOCTitle: OpenReport Macro Action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 06828474aee961dd6df02f29c7d046805a1c764c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477345"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="53a34-102">"OpenReport/レポートを開く" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="53a34-102">OpenReport Macro Action</span></span>

<span data-ttu-id="53a34-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="53a34-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="53a34-104">**OpenReport**アクションを使用するには、デザイン ビューまたは印刷プレビューでレポートを開くか、プリンターに直接レポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="53a34-104">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer.</span></span> <span data-ttu-id="53a34-105">また、レポートに印刷するレコードを制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="53a34-105">You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="53a34-106">設定値</span><span class="sxs-lookup"><span data-stu-id="53a34-106">Setting</span></span>

<span data-ttu-id="53a34-107">**OpenReport**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="53a34-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53a34-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="53a34-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="53a34-109">説明</span><span class="sxs-lookup"><span data-stu-id="53a34-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a34-110">Report Name/レポート名</span><span class="sxs-lookup"><span data-stu-id="53a34-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="53a34-p102">開くレポートの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>レポート名</strong>] ボックスには、カレント データベース内のビューがすべて表示されます。この引数は省略できません。ライブラリ データベースで OpenReport アクションが定義されているマクロを実行すると、この名前のレポートが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="53a34-p102">The name of the report to open. The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database. This is a required argument. If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a34-115">表示</span><span class="sxs-lookup"><span data-stu-id="53a34-115">View</span></span></p></td>
<td><p><span data-ttu-id="53a34-p103">レポートを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで [ <strong>印刷</strong>] (レポートをすぐに印刷する場合)、[ <strong>デザイン</strong>]、または [ <strong>印刷プレビュー</strong>] をクリックします。既定値は [ <strong>印刷</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="53a34-p103">The view in which the report will open. Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box. The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a34-119">Filter Name</span><span class="sxs-lookup"><span data-stu-id="53a34-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="53a34-120">レポートのレコードを制限するフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="53a34-120">A filter that restricts the report's records.</span></span> <span data-ttu-id="53a34-121">既存のクエリまたはクエリとして保存されているフィルターのいずれかの名前を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="53a34-121">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="53a34-122">ただし、クエリでは、開こうとしているか、<strong>含まれる</strong>プロパティを [<strong>はい]</strong>が設定されてレポートにすべてのフィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a34-122">However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a34-123">Where Condition</span><span class="sxs-lookup"><span data-stu-id="53a34-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="53a34-124">有効な SQL WHERE 句 (語を除く、)、またはレポートからレコードを選択するときに使用する式には、テーブルまたはクエリの基になります。</span><span class="sxs-lookup"><span data-stu-id="53a34-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="53a34-125">フィルター名の引数を指定してフィルターを選択する場合は、フィルターの結果に次の WHERE 句が適用されます。</span><span class="sxs-lookup"><span data-stu-id="53a34-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="53a34-126">レポートを開いて、フォームのコントロールの値を使ってレコードを制限するには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="53a34-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="53a34-127"><strong> 
<strong>[</strong><em>フィールド名</em>] = フォームです。[</strong><em>フォーム</em><strong>]![</strong><em>名フォームに置き換えます</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="53a34-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="53a34-128"><em>フィールド名</em>を基になるテーブルまたはクエリを開くには、レポートのフィールドの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="53a34-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="53a34-129"><em>フォーム名</em>と<em>名フォームに置き換えます</em>をフォームと一致するようにレポート内のレコードの値が含まれるフォーム上のコントロールの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="53a34-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="53a34-130"><b>注</b>: 条件式の最大長は 255 文字、です。</span><span class="sxs-lookup"><span data-stu-id="53a34-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="53a34-131">複雑な SQL WHERE 句よりも長い時間を入力する場合は、 <b>DoCmd</b>オブジェクトの<b>OpenReport</b>メソッドで Visual Basic for Applications (VBA) モジュールの代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="53a34-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="53a34-132">VBA では、SQL 句のステートメントの最大 32,768 文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="53a34-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a34-133">Window Mode</span><span class="sxs-lookup"><span data-stu-id="53a34-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="53a34-p108">レポートを開くときのモードを指定します。[ <strong>ウィンドウ モード</strong>] ボックスで、[ <strong>標準</strong>]、[ <strong>非表示</strong>]、[ <strong>アイコン</strong>]、または [ <strong>ダイアログ</strong>] をクリックします。既定値は [ <strong>標準</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="53a34-p108">The mode in which the report will open. Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box. The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="53a34-137"><b>注</b>: タブ付きドキュメントを使用すると、引数のいくつかのウィンドウ モードの設定は適用されません。</span><span class="sxs-lookup"><span data-stu-id="53a34-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="53a34-138">重ねて表示されるウィンドウに切り替えるには</span><span class="sxs-lookup"><span data-stu-id="53a34-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="53a34-139">[ <strong>オプション</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a34-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="53a34-140">[ <strong>Access のオプション</strong>] ダイアログ ボックスの [ <strong>カレント データベース</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a34-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="53a34-141">[ <strong>アプリケーション オプション</strong>] の [ <strong>ドキュメント ウィンドウ オプション</strong>] で [ <strong>ウィンドウを重ねて表示する</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53a34-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="53a34-142">[ <strong>OK</strong>] をクリックし、データベースを閉じて再度開きます。</span><span class="sxs-lookup"><span data-stu-id="53a34-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="53a34-143">備考</span><span class="sxs-lookup"><span data-stu-id="53a34-143">Remarks</span></span>

<span data-ttu-id="53a34-p110">" **View/ビュー** " 引数で [ **印刷**] を選択すると、現在のプリンター設定を使用してすぐにレポートが印刷されますが、[ **印刷**] ダイアログ ボックスは表示されません。また、" **OpenReport/レポートを開く** " アクションを使用すると、レポートを開いて設定した後に、 PrintOut アクションを使用してレポートを印刷することもできます。たとえば、印刷前に、レポートを修正したり、" **PrintOut/印刷** " アクションを使用してプリンター設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="53a34-p110">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box. You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it. For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="53a34-147">フィルターおよび WHERE 条件式を指定するレポートの**フィルター**のプロパティの設定になります。</span><span class="sxs-lookup"><span data-stu-id="53a34-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="53a34-148">**OpenReport**アクションは、ナビゲーション ウィンドウでレポートをダブルクリックすると、ナビゲーション ウィンドウでレポートを右クリックしてやビューまたは **[印刷**] コマンドを選択することに似ています。</span><span class="sxs-lookup"><span data-stu-id="53a34-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="53a34-149">複数のデータ セットに対して、類似したレポートを印刷するには、フィルターまたは WHERE 句を使用してレポートに印刷するレコードを制限します。</span><span class="sxs-lookup"><span data-stu-id="53a34-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="53a34-150">別のフィルターを適用または条件式を変更するマクロを編集します。</span><span class="sxs-lookup"><span data-stu-id="53a34-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="53a34-151">ナビゲーション ウィンドウからマクロのアクション行にレポートをドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="53a34-151">You can drag a report from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="53a34-152">これにより、レポート ビューでレポートを開く**OpenReport**アクションが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="53a34-152">This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="53a34-153">例</span><span class="sxs-lookup"><span data-stu-id="53a34-153">Example</span></span>

<span data-ttu-id="53a34-154">次の例では、 OpenReport アクションを使用して、レポートを開くときにフィルターを適用するパラメーターを渡す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="53a34-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="53a34-155">**RptChapters**レポートは、SelectedAuthor パラメーターを**cboAuthors**のコンボ ボックスで選択したアイテムを渡すことによって、指定した作成者のレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="53a34-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="53a34-156">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="53a34-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
