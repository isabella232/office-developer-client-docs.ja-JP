---
title: GoToRecord マクロ アクション
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292140"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="97fc2-102">GoToRecord マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="97fc2-102">GoToRecord macro action</span></span>


<span data-ttu-id="97fc2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="97fc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97fc2-104">"GoToRecord/レコードの移動" アクションを使用すると、開いているテーブル、フォーム、またはクエリの結果セットで、指定したレコードをカレント レコードにすることができます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="97fc2-105">Setting</span><span class="sxs-lookup"><span data-stu-id="97fc2-105">Setting</span></span>

<span data-ttu-id="97fc2-106">"**GoToRecord/レコードの移動**" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="97fc2-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97fc2-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="97fc2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="97fc2-108">説明</span><span class="sxs-lookup"><span data-stu-id="97fc2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97fc2-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="97fc2-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="97fc2-p101">カレント レコードにするレコードが含まれているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97fc2-113"><strong>オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="97fc2-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="97fc2-p102">カレント レコードにするレコードが含まれているオブジェクトの名前を指定します。[オブジェクト名] ボックスには、カレント データベースに含まれる、"Object Type/オブジェクトの種類" 引数で指定した種類のオブジェクトがすべて表示されます。"Object Type/オブジェクトの種類" 引数を指定しない場合は、この引数も指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="97fc2-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97fc2-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="97fc2-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="97fc2-p103">カレント レコードにするレコードを指定します。[<strong>レコード</strong>] ボックスで、[<strong>前のレコード</strong>]、[<strong>次のレコード</strong>]、[<strong>先頭のレコード</strong>]、[<strong>最後のレコード</strong>]、[<strong>移動先指定</strong>]、[<strong>新しいレコード</strong>] のいずれかをクリックします。既定値は [<strong>次のレコード</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="97fc2-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97fc2-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="97fc2-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="97fc2-122">整数値、または結果が整数値となる式を指定します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="97fc2-123">式の前には等号 (<strong>=</strong>) を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fc2-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="97fc2-124">この引数では、カレント レコードにするレコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="97fc2-125">この引数の使用方法は 2 とおりあります。</span><span class="sxs-lookup"><span data-stu-id="97fc2-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="97fc2-126"><strong>Record</strong>引数が Previous また<strong></strong>は<strong>Previous</strong>に指定されている場合、Microsoft Office Access 2007 は、 <strong>Offset</strong>引数で指定したレコード数を前方または後方に移動します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="97fc2-127"><strong>record</strong>引数に<strong>Go を</strong>指定すると、引数<strong>Offset</strong>と等しい数のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-127">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="97fc2-128">レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-128">The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="97fc2-129"><strong>注</strong>: <strong>Record</strong>引数の<strong>最初</strong>、<strong>最後</strong>、または<strong>新しい</strong>設定を使用すると、引数<strong>Offset</strong>は無視されます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="97fc2-130">引数<strong>Offset</strong>に大きすぎる値を入力すると、エラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="97fc2-131"><strong>Offset</strong>引数に負の数を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="97fc2-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="97fc2-132"><strong>Record</strong>引数が Previous また<strong></strong>は<strong>Previous</strong>に指定されている場合、Microsoft Office Access 2007 は、 <strong>Offset</strong>引数で指定したレコード数を前方または後方に移動します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="97fc2-133"><strong>record</strong>引数に<strong>Go を</strong>指定すると、引数<strong>Offset</strong>と等しい数のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="97fc2-133">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="97fc2-134">レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="97fc2-134">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="97fc2-135">注釈</span><span class="sxs-lookup"><span data-stu-id="97fc2-135">Remarks</span></span>

<span data-ttu-id="97fc2-136">レコードの特定のコントロールにフォーカスがある場合、このアクションを実行しても、新しいフォームの同じコントロールにフォーカスがとどまります。</span><span class="sxs-lookup"><span data-stu-id="97fc2-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="97fc2-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span><span class="sxs-lookup"><span data-stu-id="97fc2-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="97fc2-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span><span class="sxs-lookup"><span data-stu-id="97fc2-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="97fc2-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span><span class="sxs-lookup"><span data-stu-id="97fc2-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="97fc2-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="97fc2-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

