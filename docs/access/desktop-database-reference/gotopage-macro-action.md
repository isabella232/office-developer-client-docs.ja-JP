---
title: GoToPage マクロ アクション
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292161"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="31854-102">GoToPage マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="31854-102">GoToPage macro action</span></span>

<span data-ttu-id="31854-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="31854-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31854-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span><span class="sxs-lookup"><span data-stu-id="31854-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="31854-109">Setting</span><span class="sxs-lookup"><span data-stu-id="31854-109">Setting</span></span>

<span data-ttu-id="31854-110">"GoToPage/ページの移動" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="31854-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31854-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="31854-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="31854-112">説明</span><span class="sxs-lookup"><span data-stu-id="31854-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31854-113"><strong>Page Number/ページ番号</strong></span><span class="sxs-lookup"><span data-stu-id="31854-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="31854-114">フォーカスを移動するページの番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="31854-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="31854-115">[マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ページ</strong>番号] ボックスにページ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="31854-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="31854-116">この引数を指定しないと、フォーカスはカレント ページにとどまります。</span><span class="sxs-lookup"><span data-stu-id="31854-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="31854-117"><strong>右</strong>および<strong>下</strong>の引数を使用して、表示するページの一部を表示できます。</span><span class="sxs-lookup"><span data-stu-id="31854-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31854-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="31854-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="31854-p103">ページの左端を表示する水平方向の位置を、そのページを表示するウィンドウの左端からの距離で指定します。"Down/下" 引数を指定する場合は、この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="31854-p103">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window. This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31854-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="31854-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="31854-p104">ページの上端を表示する垂直方向の位置を、そのページを表示するウィンドウの上端からの距離で指定します。"Right/右" 引数を指定する場合は、この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="31854-p104">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window. This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="31854-124">"Right/右" 引数と "Down/下" 引数は、インチまたは cm 単位で指定します。どちらの単位を使用するかは、Windows コントロール パネルの地域の設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="31854-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="31854-125">注釈</span><span class="sxs-lookup"><span data-stu-id="31854-125">Remarks</span></span>

<span data-ttu-id="31854-p105">このアクションを使用すると、指定ページの最初のコントロール (フォームのタブ オーダーで定義されたコントロール) を選択できます。フォーム上の特定のコントロールに移動するには、"GoToControl/コントロールの移動" アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="31854-p105">You can use this action to select the first control (as defined by the form's tab order) on the specified page. Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="31854-128">Access ウィンドウよりも大きいページを持つフォームの場合は、引数**Right**および**Down**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="31854-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="31854-129">" **Page Number/ページ番号** " 引数を使用して目的のページに移動し、次に " **Right/右** " 引数と " **Down/下** " 引数を使ってページの必要な部分を表示します。</span><span class="sxs-lookup"><span data-stu-id="31854-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="31854-130">このとき、ウィンドウの左上隅から、引数で指定した間隔を置いた位置に、ページの左上隅が表示されます。</span><span class="sxs-lookup"><span data-stu-id="31854-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="31854-131">You can't use the **GoToPage** action in the following cases:</span><span class="sxs-lookup"><span data-stu-id="31854-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="31854-132">非表示のフォームのページにフォーカスを移動する場合</span><span class="sxs-lookup"><span data-stu-id="31854-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="31854-133">タブ コントロール内の別のページにフォーカスを移動する場合</span><span class="sxs-lookup"><span data-stu-id="31854-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="31854-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="31854-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

