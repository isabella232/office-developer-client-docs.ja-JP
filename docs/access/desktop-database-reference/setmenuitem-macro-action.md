---
title: "'SetMenuItem/メニューの設定' マクロ アクション"
TOCTitle: SetMenuItem Macro Action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d6b5a91e9aa2f0c729a7fce221c859eb0cecc290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476742"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="4418d-102">"SetMenuItem/メニューの設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="4418d-102">SetMenuItem Macro Action</span></span>


<span data-ttu-id="4418d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4418d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4418d-104">**SetMenuItem**アクションを使用すると、[**アドイン**] タブで、カスタムまたはグローバル メニューのメニュー項目の (有効または無効になっている、選択または選択されていない場合) の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="4418d-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4418d-105"><STRONG>SetMenuItem</STRONG>アクションは、メニュー マクロで作成されたユーザー設定とグローバルのメニューでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="4418d-105">The <STRONG>SetMenuItem</STRONG> action works only with custom and global menus created by using menu macros.</span></span> <span data-ttu-id="4418d-106"><STRONG>SetMenuItem</STRONG>アクションは、以前のバージョンとの互換性のための Microsoft Access に含まれます。</span><span class="sxs-lookup"><span data-stu-id="4418d-106">The <STRONG>SetMenuItem</STRONG> action is included in Microsoft Access only for compatibility with previous versions.</span></span> <span data-ttu-id="4418d-107">コマンド バーの機能は動作しません。</span><span class="sxs-lookup"><span data-stu-id="4418d-107">It does not work with the command bar functionality.</span></span> <span data-ttu-id="4418d-108">ただしを無効にするまたは有効にする選択するか、ショートカット メニュー上の項目の選択を解除するのには、Visual Basic for Applications (VBA) モジュールのプロパティを<STRONG>有効に</STRONG>し、<STRONG>状態</STRONG>またはユーザー設定やグローバル メニューを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4418d-108">However, you can use the <STRONG>Enabled</STRONG> and <STRONG>State</STRONG> properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span></P>



## <a name="setting"></a><span data-ttu-id="4418d-109">設定値</span><span class="sxs-lookup"><span data-stu-id="4418d-109">Setting</span></span>

<span data-ttu-id="4418d-110">**SetMenuItem**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="4418d-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4418d-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="4418d-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4418d-112">説明</span><span class="sxs-lookup"><span data-stu-id="4418d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4418d-113"><strong>Menu Index/メニュー インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="4418d-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4418d-114">状態を設定するコマンドを含むメニューのインデックス。</span><span class="sxs-lookup"><span data-stu-id="4418d-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="4418d-115">カスタム メニューまたはグローバル メニューのメニューのインデックスを表す 0 から始まる整数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4418d-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="4418d-116">マクロ ビルダー] ウィンドウの<strong>メニューの [インデックス</strong>] ボックス [<strong>アクションの引数</strong>] セクションで、インデックスの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4418d-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="4418d-117">インデックスは、メニュー マクロに、カスタム メニューまたはグローバル メニュー (このメニューの<strong>メニューの追加</strong>アクション] メニューの 0 から数えた位置) のメニューの位置を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="4418d-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="4418d-118">メニュー マクロで条件式を使用するにはカスタム メニュー項目を表示または非表示にするため、メニューの表示が若干異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4418d-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="4418d-119">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="4418d-119">This is a required argument.</span></span> <span data-ttu-id="4418d-120">場合はこの引数でメニューを選択し、<strong>インデックスのコマンド</strong>や<strong>サブコマンドのインデックス</strong>の引数を空白のままにするを有効にしたり、メニュー名自体を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="4418d-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="4418d-121">ただし、選択または (アクセスを無視する] メニューの [名前の<strong>フラグ</strong>引数の設定<strong>を確認</strong>し<strong>をオフにします</strong>)] メニューの [名前の選択を解除することはできません。</span><span class="sxs-lookup"><span data-stu-id="4418d-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4418d-122"><strong>Command Index/コマンド インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="4418d-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4418d-123">状態を設定するコマンドのインデックス。</span><span class="sxs-lookup"><span data-stu-id="4418d-123">The index of the command for which you want to set the state.</span></span> <span data-ttu-id="4418d-124"><strong>メニュー インデックス</strong>の引数で選択したメニューで目的のコマンドのインデックスを表す 0 から始まる整数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4418d-124">Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument.</span></span> <span data-ttu-id="4418d-125">インデックスは、カスタム メニューまたはグローバル メニュー (0 から数えて、マクロ グループ内のこのコマンドのマクロの位置) を選択したメニューを定義するマクロ グループにおける対象コマンドの位置を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="4418d-125">The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0).</span></span> <span data-ttu-id="4418d-126">メニューのマクロ グループで条件式を使用するにはカスタム メニュー コマンドを表示または非表示にするため、メニューの表示が若干異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4418d-126">The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4418d-127"><strong>Subcommand Index/サブコマンド インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="4418d-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4418d-128">状態を設定するサブコマンドのインデックス。</span><span class="sxs-lookup"><span data-stu-id="4418d-128">The index of the subcommand for which you want to set the state.</span></span> <span data-ttu-id="4418d-129">これは、目的のコマンドにサブメニューがある場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4418d-129">This applies only if the desired command has a submenu.</span></span> <span data-ttu-id="4418d-130"><strong>コマンド インデックス</strong>引数で選択したサブメニューのサブコマンドのインデックスを表す 0 から始まる整数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4418d-130">Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument.</span></span> <span data-ttu-id="4418d-131">インデックスは、カスタム メニューまたはグローバル メニュー (0 から数えて、マクロ グループ内のこのサブコマンドのマクロの位置) を選択したサブメニューを定義するマクロ グループにおける対象サブコマンドの位置を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="4418d-131">The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4418d-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="4418d-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="4418d-p105">コマンドまたはサブコマンドに設定する状態を指定します。コマンドを無効にして淡色表示にする場合は [<strong>淡色表示</strong>]、コマンドを有効にする場合は [<strong>通常表示</strong>]、コマンドの横にチェックマークを付けて選択つまり設定されていることを示す場合は [<strong>チェックマーク表示</strong>]、チェックマークを外す場合は [<strong>チェックマーク非表示</strong>] をクリックします。既定値は [<strong>通常表示</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="4418d-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4418d-136">解説</span><span class="sxs-lookup"><span data-stu-id="4418d-136">Remarks</span></span>

<span data-ttu-id="4418d-137">**SetMenuItem**アクションは、カスタム メニューまたはグローバル メニューに対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="4418d-137">The **SetMenuItem** action works only on a custom or global menu.</span></span> <span data-ttu-id="4418d-138">作業中のウィンドウは、カスタム メニューまたはグローバル メニューを持たない場合は、 **SetMenuItem**アクションを含むマクロを実行すると実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4418d-138">If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="4418d-139">このアクションを使用すると、メニュー コマンドおよびサブコマンドの状態は設定できますが、サブコマンドのサブコマンドの状態は設定できません。</span><span class="sxs-lookup"><span data-stu-id="4418d-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="4418d-140">**SetMenuItem**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**SetMenuItem**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4418d-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

