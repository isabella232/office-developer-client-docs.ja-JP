---
title: SetMenuItem マクロ アクション
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308681"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="a2bb0-102">SetMenuItem マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a2bb0-102">SetMenuItem macro action</span></span>

<span data-ttu-id="a2bb0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2bb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2bb0-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span><span class="sxs-lookup"><span data-stu-id="a2bb0-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="a2bb0-p101">The **SetMenuItem** action works only with custom and global menus created by using menu macros. The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span><span class="sxs-lookup"><span data-stu-id="a2bb0-p101">The **SetMenuItem** action works only with custom and global menus created by using menu macros. The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="a2bb0-109">Setting</span><span class="sxs-lookup"><span data-stu-id="a2bb0-109">Setting</span></span>

<span data-ttu-id="a2bb0-110">"SetMenuItem/メニューの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2bb0-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a2bb0-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a2bb0-112">説明</span><span class="sxs-lookup"><span data-stu-id="a2bb0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2bb0-113"><strong>Menu Index/メニュー インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="a2bb0-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a2bb0-114">状態を設定するコマンドを含むメニューのインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="a2bb0-115">ユーザー設定またはグローバルメニューの目的のメニューのインデックスとして、0から始まる整数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="a2bb0-116">[マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションで、 <strong>[メニューインデックス</strong>] ボックスにインデックス値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a2bb0-117">インデックスは、ユーザー設定またはグローバルメニューのメニューマクロにおけるメニューの位置を基準にしたものです (メニューマクロのこのメニューの " <strong>AddMenu</strong> /メニューの設定" アクションの0からカウント)。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="a2bb0-118">メニューの表示は、メニューマクロで条件式を使用してユーザー設定メニュー項目を表示または非表示にできるため、多少異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="a2bb0-119">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-119">This is a required argument.</span></span> <span data-ttu-id="a2bb0-120">この引数でメニューを選択し、"Command Index/コマンド インデックス" 引数と "Subcommand Index/サブコマンド インデックス" 引数を空白にすると、メニュー名自体を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="a2bb0-121">ただし、メニュー名のチェックマークを付けたり外したりすることはできません (Access では、メニュー名の "Flag/フラグ" 引数の [チェックマーク表示] と [チェックマーク非表示] の設定は無視されます)。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2bb0-122"><strong>Command Index/コマンド インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="a2bb0-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a2bb0-p103">状態を設定するコマンドのインデックスを指定します。"Menu Index/メニュー インデックス" 引数で選択したメニューの該当コマンドのインデックスとして 0 以上の整数値を入力します。インデックスは、ユーザー設定のメニューやグローバル メニューで選択したメニューを定義するマクロ グループにおけるコマンドの位置 (マクロ グループ内でのコマンドのマクロを示す 0 から数えた位置) を基準としています。メニューのマクロ グループで条件式を使用するとユーザー設定のメニュー コマンドの表示と非表示を切り替えることができるため、メニューの表示は多少異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-p103">The index of the command for which you want to set the state. Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument. The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0). The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2bb0-127"><strong>Subcommand Index/サブコマンド インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="a2bb0-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a2bb0-p104">状態を設定するサブコマンドのインデックスを指定します。これが適用されるのは、目的のコマンドにサブメニューが含まれる場合のみです。"Command Index/コマンド インデックス" 引数で選択したサブメニューの該当サブコマンドのインデックスとして 0 以上の整数値を入力します。インデックスは、ユーザー設定のメニューやグローバル メニューで選択したサブメニューを定義するマクロ グループにおけるサブコマンドの位置 (マクロ グループ内でのサブコマンドのマクロを示す 0 から数えた位置) を基準としています。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-p104">The index of the subcommand for which you want to set the state. This applies only if the desired command has a submenu. Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument. The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2bb0-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="a2bb0-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="a2bb0-p105">コマンドまたはサブコマンドに設定する状態を指定します。コマンドを無効にして淡色表示にする場合は [<strong>淡色表示</strong>]、コマンドを有効にする場合は [<strong>通常表示</strong>]、コマンドの横にチェックマークを付けて選択つまり設定されていることを示す場合は [<strong>チェックマーク表示</strong>]、チェックマークを外す場合は [<strong>チェックマーク非表示</strong>] をクリックします。既定値は [<strong>通常表示</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a2bb0-136">注釈</span><span class="sxs-lookup"><span data-stu-id="a2bb0-136">Remarks</span></span>

<span data-ttu-id="a2bb0-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span><span class="sxs-lookup"><span data-stu-id="a2bb0-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="a2bb0-139">このアクションを使用すると、メニュー コマンドおよびサブコマンドの状態は設定できますが、サブコマンドのサブコマンドの状態は設定できません。</span><span class="sxs-lookup"><span data-stu-id="a2bb0-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="a2bb0-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="a2bb0-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

