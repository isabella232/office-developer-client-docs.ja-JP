---
title: "'GoToRecord/レコードの移動' マクロ アクション"
TOCTitle: GoToRecord Macro Action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 702910c12f0954b8d5cf8c0c49395cb65b8c661d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879859"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="1cb2c-102">"GoToRecord/レコードの移動" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="1cb2c-102">GoToRecord Macro Action</span></span>


<span data-ttu-id="1cb2c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cb2c-104">**GoToRecord**アクションを使用するには、開いているテーブル、フォーム、またはクエリの結果セットで、指定されたレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="1cb2c-105">設定値</span><span class="sxs-lookup"><span data-stu-id="1cb2c-105">Setting</span></span>

<span data-ttu-id="1cb2c-106">" **GoToRecord/レコードの移動** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cb2c-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="1cb2c-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1cb2c-108">説明</span><span class="sxs-lookup"><span data-stu-id="1cb2c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cb2c-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="1cb2c-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb2c-p101">カレント レコードにするレコードが含まれているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb2c-113"><strong>オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="1cb2c-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb2c-114">現在のレコードにレコードを格納するオブジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-114">The name of the object that contains the record you want to make the current record.</span></span> <span data-ttu-id="1cb2c-115"><strong>オブジェクト名</strong>] ボックスでは、<strong>オブジェクトの型</strong>引数で指定した型の現在のデータベース内のすべてのオブジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-115">The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="1cb2c-116"><strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-116">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cb2c-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="1cb2c-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb2c-p103">カレント レコードにするレコードを指定します。[<strong>レコード</strong>] ボックスで、[<strong>前のレコード</strong>]、[<strong>次のレコード</strong>]、[<strong>先頭のレコード</strong>]、[<strong>最後のレコード</strong>]、[<strong>移動先指定</strong>]、[<strong>新しいレコード</strong>] のいずれかをクリックします。既定値は [<strong>次のレコード</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb2c-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="1cb2c-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb2c-122">整数型または整数値に評価される式です。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="1cb2c-123">式の前に等号 (=) (<strong>=</strong>)。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="1cb2c-124">この引数は、カレント レコードのレコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="1cb2c-125">2 つの方法では、<strong>この引数</strong>を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="1cb2c-126"><strong>Record</strong>引数は、<strong>次</strong>または<strong>前</strong>に、Microsoft Office Access 2007 は、前方または後方は、<strong>この引数</strong>で指定されたレコードの数を移動します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="1cb2c-127"><strong>レコード</strong>の引数が<strong>移動先</strong>にある場合は、<strong>オフセット</strong>の引数に等しい数のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-127">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="1cb2c-128">レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-128">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>

> [!NOTE]
> <P><span data-ttu-id="1cb2c-129"><STRONG></STRONG> <STRONG>最初</STRONG>、<STRONG>最後</STRONG>、または<STRONG>新規</STRONG>の設定を使用する場合<STRONG>、この引数</STRONG>は無視されます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-129">If you use the <STRONG>First</STRONG>, <STRONG>Last</STRONG>, or <STRONG>New</STRONG> setting for the <STRONG>Record</STRONG> argument, Access ignores the <STRONG>Offset</STRONG> argument.</span></span> <span data-ttu-id="1cb2c-130">大きすぎて<STRONG>オフセット</STRONG>の引数を入力する場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-130">If you enter an <STRONG>Offset</STRONG> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="1cb2c-131"><STRONG>オフセット</STRONG>の引数に負の値を入力できません。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-131">You can't enter negative numbers for the <STRONG>Offset</STRONG> argument.</span></span></P>


<p></p>
<ul>
<li><p><span data-ttu-id="1cb2c-132"><strong>Record</strong>引数は、<strong>次</strong>または<strong>前</strong>に、Microsoft Office Access 2007 は、前方または後方は、<strong>この引数</strong>で指定されたレコードの数を移動します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="1cb2c-133"><strong>レコード</strong>の引数が<strong>移動先</strong>にある場合は、<strong>オフセット</strong>の引数に等しい数のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-133">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="1cb2c-134">レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-134">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1cb2c-135">解説</span><span class="sxs-lookup"><span data-stu-id="1cb2c-135">Remarks</span></span>

<span data-ttu-id="1cb2c-136">レコードの特定のコントロールにフォーカスがある場合、このアクションを実行しても、新しいフォームの同じコントロールにフォーカスがとどまります。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="1cb2c-137">\*\*\*\* **新規**設定を使用すると、フォームまたはテーブルの末尾に空白のレコードに移動して新しいデータを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="1cb2c-138">このアクションでは、[**ホーム**] タブの [**検索**] ボタンの下の矢印をクリックし、[移動]**を**クリックすると似ています。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-138">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**.</span></span> <span data-ttu-id="1cb2c-139">**最初**、**最後**、**次\*\*\*\*前**、および、[**移動**] コマンドのサブコマンドを**新しいレコード**に、**最初**、**最後**、**次\*\*\*\*前**、選択したオブジェクトに同じ効果があります。\*\*\*\* **新規**設定します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-139">The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument.</span></span> <span data-ttu-id="1cb2c-140">ウィンドウの下部にあるナビゲーション ボタンを使用してレコードに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-140">You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="1cb2c-141">**GoToRecord**アクションを使用すると、**オブジェクト型**および**オブジェクト名**の引数を非表示のフォームを指定する場合、非表示のフォームの現在のレコードにレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="1cb2c-142">**GoToRecord**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**GoToRecord**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1cb2c-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

