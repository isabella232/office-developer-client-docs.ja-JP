---
title: AddMenu マクロ アクション
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280274"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="ca996-102">AddMenu マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ca996-102">AddMenu macro action</span></span>


<span data-ttu-id="ca996-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca996-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca996-104">This article describes the basic operation of the **AddMenu** macro action.</span><span class="sxs-lookup"><span data-stu-id="ca996-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="ca996-105">You can use the **AddMenu** action to create:</span><span class="sxs-lookup"><span data-stu-id="ca996-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="ca996-106">特定のフォームやレポートに対する、[ **アドイン**] タブのカスタム メニュー。</span><span class="sxs-lookup"><span data-stu-id="ca996-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="ca996-p101">フォーム、レポート、またはコントロールのカスタム ショートカット メニュー。フォーム、レポート、またはコントロールで、組み込みショートカット メニューの代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca996-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="ca996-p102">グローバル ショートカット メニュー。グローバル ショートカット メニューは、フォーム、 レポート、またはコントロールのカスタム ショートカット メニューを追加した場合を除き、テーブルやクエリ データシート内のフィールド、フォーム、およびレポートで、組み込みショートカット メニューの代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca996-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="ca996-111">Setting</span><span class="sxs-lookup"><span data-stu-id="ca996-111">Setting</span></span>

<span data-ttu-id="ca996-112">"AddMenu/メニューの追加" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ca996-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca996-113">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="ca996-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ca996-114">説明</span><span class="sxs-lookup"><span data-stu-id="ca996-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca996-115"><strong>Menu Name/メニュー名</strong></span><span class="sxs-lookup"><span data-stu-id="ca996-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ca996-116">メニューの名前&quot;(レポートコマンド&quot;や&quot;ツール&quot;など)。</span><span class="sxs-lookup"><span data-stu-id="ca996-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="ca996-117">キーボードを使用してメニューを選択できるようにアクセスキーを作成するには、アクセスキー<strong>&amp;</strong>として使用する文字の前にアンパサンド () を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca996-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="ca996-118">[<strong>アドイン</strong>] タブのメニュー名で、この文字に下線が付きます。</span><span class="sxs-lookup"><span data-stu-id="ca996-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca996-119"><strong>Menu Macro Name/メニュー マクロ名</strong></span><span class="sxs-lookup"><span data-stu-id="ca996-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ca996-120">メニュー コマンドのマクロを含むマクロ グループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca996-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="ca996-121">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="ca996-121">This is a required argument.</span></span></p>
<p><span data-ttu-id="ca996-122"><strong>注</strong>: ライブラリデータベースで " <strong>AddMenu/メニュー</strong>の作成" アクションが記述されたマクロを実行すると、Microsoft Office Access 2007 は、この名前のマクログループをカレントデータベースでのみ検索します。</span><span class="sxs-lookup"><span data-stu-id="ca996-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca996-123"><strong>Status Bar Text/ステータス バー テキスト</strong></span><span class="sxs-lookup"><span data-stu-id="ca996-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="ca996-124">メニュー選択時にステータス バーに表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="ca996-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="ca996-125">ショートカット メニューの場合、この引数は無視されます。</span><span class="sxs-lookup"><span data-stu-id="ca996-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca996-126">注釈</span><span class="sxs-lookup"><span data-stu-id="ca996-126">Remarks</span></span>

<span data-ttu-id="ca996-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span><span class="sxs-lookup"><span data-stu-id="ca996-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

