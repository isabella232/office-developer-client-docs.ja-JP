---
title: "\"GoToPage/ページの移動\" マクロ アクション"
TOCTitle: GoToPage Macro Action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b183b7815769c1eed8c3ee0826167b93453ca19d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891311"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="a34fb-102">"GoToPage/ページの移動" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a34fb-102">GoToPage Macro Action</span></span>


<span data-ttu-id="a34fb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a34fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a34fb-104">**GoToPage**アクションを使用すると、アクティブ フォームの指定したページの先頭のコントロールにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a34fb-104">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page.</span></span> <span data-ttu-id="a34fb-105">このアクションは、関連のある情報を改ページで分割しているフォームを作成した場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-105">You can use this action if you have created a form with page breaks that contains groups of related information.</span></span> <span data-ttu-id="a34fb-106">たとえば、社員フォームの最初のページに個人情報、2 ページ目に会社情報、3 ページ目に売上情報があるとします。</span><span class="sxs-lookup"><span data-stu-id="a34fb-106">For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page.</span></span> <span data-ttu-id="a34fb-107">**GoToPage**アクションを使用すると、目的のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="a34fb-107">You can use the **GoToPage** action to move to the desired page.</span></span> <span data-ttu-id="a34fb-108">また、タブ コントロールを使用すると、1 つのフォーム上で複数のページに情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-108">You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="a34fb-109">設定値</span><span class="sxs-lookup"><span data-stu-id="a34fb-109">Setting</span></span>

<span data-ttu-id="a34fb-110">**GoToPage**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="a34fb-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a34fb-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a34fb-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a34fb-112">説明</span><span class="sxs-lookup"><span data-stu-id="a34fb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a34fb-113"><strong>ページ番号</strong></span><span class="sxs-lookup"><span data-stu-id="a34fb-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="a34fb-114">フォーカスを移動するページの数です。</span><span class="sxs-lookup"><span data-stu-id="a34fb-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="a34fb-115">マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの<strong>ページ番号</strong>ボックスにページ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="a34fb-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a34fb-116">この引数を指定しないと、フォーカスはカレント ページにとどまります。</span><span class="sxs-lookup"><span data-stu-id="a34fb-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="a34fb-117">表示するページの部分を表示するのには、<strong>右</strong>と<strong>下</strong>の引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a34fb-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="a34fb-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="a34fb-119">ページで、スポットの水平方向の位置は、ウィンドウの左端に表示するウィンドウの左端から計測されます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-119">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window.</span></span> <span data-ttu-id="a34fb-120"><strong></strong>引数を指定する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="a34fb-120">This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a34fb-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="a34fb-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="a34fb-122">ページ上の場所の垂直方向の位置は、ウィンドウの上端に表示するウィンドウの上端から測定されます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-122">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window.</span></span> <span data-ttu-id="a34fb-123"><strong>右</strong>の引数を指定する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="a34fb-123">This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="a34fb-124"><STRONG>右</STRONG>と<STRONG>下</STRONG>の引数は、インチまたはセンチメートル、Windows コントロール パネルの [地域の設定によって測定されます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-124">The <STRONG>Right</STRONG> and <STRONG>Down</STRONG> arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="a34fb-125">解説</span><span class="sxs-lookup"><span data-stu-id="a34fb-125">Remarks</span></span>

<span data-ttu-id="a34fb-126">ページで指定された最初のコントロール (フォームのタブ オーダーで定義されている) を選択するのには、このアクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-126">You can use this action to select the first control (as defined by the form's tab order) on the specified page.</span></span> <span data-ttu-id="a34fb-127">**フォーカスを移動**を使用すると、フォーム上の特定のコントロールに移動できます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-127">Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="a34fb-128">Access ウィンドウよりも大きいページでは、フォームの**右**と**下**の引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="a34fb-129">" **Page Number/ページ番号** " 引数を使用して目的のページに移動し、次に " **Right/右** " 引数と " **Down/下** " 引数を使ってページの必要な部分を表示します。</span><span class="sxs-lookup"><span data-stu-id="a34fb-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="a34fb-130">このとき、ウィンドウの左上隅から、引数で指定した間隔を置いた位置に、ページの左上隅が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a34fb-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="a34fb-131">**GoToPage**アクションは、次の場合に使用できません。</span><span class="sxs-lookup"><span data-stu-id="a34fb-131">You can't use the **GoToPage** action in the following cases:</span></span>

  - <span data-ttu-id="a34fb-132">非表示のフォームのページにフォーカスを移動する場合</span><span class="sxs-lookup"><span data-stu-id="a34fb-132">To move the focus to a page on a hidden form.</span></span>

  - <span data-ttu-id="a34fb-133">タブ コントロール内の別のページにフォーカスを移動する場合</span><span class="sxs-lookup"><span data-stu-id="a34fb-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="a34fb-134">Visual Basic for Applications (VBA) モジュールでは、 **GoToPage**アクションを実行するには、 **DoCmd**オブジェクトの**GoToPage**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a34fb-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

