---
title: "'AddMenu/メニューの追加' マクロ アクション"
TOCTitle: AddMenu Macro Action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 984b10638ab7f01aeb4dc9656bc70aa1e44d56a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478514"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="fa05f-102">"AddMenu/メニューの追加" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fa05f-102">AddMenu Macro Action</span></span>


<span data-ttu-id="fa05f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa05f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fa05f-104">**Addmenu マクロ**の基本的な操作をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fa05f-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="fa05f-105">作成するのには、**メニューの追加**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="fa05f-106">特定のフォームやレポートに対する、[ **アドイン**] タブのカスタム メニュー。</span><span class="sxs-lookup"><span data-stu-id="fa05f-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="fa05f-p101">フォーム、レポート、またはコントロールのカスタム ショートカット メニュー。フォーム、レポート、またはコントロールで、組み込みショートカット メニューの代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="fa05f-p102">グローバル ショートカット メニュー。グローバル ショートカット メニューは、フォーム、 レポート、またはコントロールのカスタム ショートカット メニューを追加した場合を除き、テーブルやクエリ データシート内のフィールド、フォーム、およびレポートで、組み込みショートカット メニューの代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="fa05f-111">設定値</span><span class="sxs-lookup"><span data-stu-id="fa05f-111">Setting</span></span>

<span data-ttu-id="fa05f-112">**メニューの追加**アクションでは、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="fa05f-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa05f-113">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="fa05f-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fa05f-114">説明</span><span class="sxs-lookup"><span data-stu-id="fa05f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa05f-115"><strong>Menu Name/メニュー名</strong></span><span class="sxs-lookup"><span data-stu-id="fa05f-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fa05f-116">たとえば、メニューの名前&quot;レポート コマンド&quot;または&quot;ツール&quot;。</span><span class="sxs-lookup"><span data-stu-id="fa05f-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="fa05f-117">メニューを選択するキーボードを使用できるようにアクセス キーを作成するのには、アンパサンドを入力します (<strong>&amp;</strong>)、アクセス キーに文字の前にします。</span><span class="sxs-lookup"><span data-stu-id="fa05f-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="fa05f-118"><strong>[アドイン</strong>] タブのメニュー名で、この文字が下線付きで表示します。</span><span class="sxs-lookup"><span data-stu-id="fa05f-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa05f-119"><strong>Menu Macro Name/メニュー マクロ名</strong></span><span class="sxs-lookup"><span data-stu-id="fa05f-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fa05f-p104">メニュー コマンドのマクロを含むマクロ グループの名前を指定します。この引数は省略できません。 

</span><span class="sxs-lookup"><span data-stu-id="fa05f-p104">The name of the macro group that contains the macros for the menu's commands. This is a required argument.</span></span></p>

> [!NOTE]
> <span data-ttu-id="fa05f-122">ライブラリ データベースでは、**メニューの追加**アクションを含むマクロを実行すると、現在のデータベースだけでは、この名前のマクロ グループの Microsoft Office Access 2007 が検索されます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-122">If you run a macro containing the **AddMenu** action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa05f-123"><strong>Status Bar Text/ステータス バー テキスト</strong></span><span class="sxs-lookup"><span data-stu-id="fa05f-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="fa05f-p105">メニュー選択時にステータス バーに表示されるテキストを指定します。ショートカット メニューの場合、この引数は無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-p105">The text to display in the status bar when the menu is selected. This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fa05f-126">解説</span><span class="sxs-lookup"><span data-stu-id="fa05f-126">Remarks</span></span>

<span data-ttu-id="fa05f-127">Visual Basic for Applications (VBA) モジュールの**メニューの追加**アクションを実行するには、 **DoCmd**オブジェクトの**AddMenu**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa05f-127">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object.</span></span> <span data-ttu-id="fa05f-128">**[アドイン**] タブにカスタム メニューを作成するか、カスタム ショートカット メニューをフォーム、レポート、またはコントロールにアタッチするのには、VBA では、 **MenuBar**プロパティまたは**ShortcutMenuBar**プロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-128">You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control.</span></span> <span data-ttu-id="fa05f-129">グローバル ショートカット メニューを作成する**アプリケーション**オブジェクトの**ShortcutMenuBar**プロパティを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fa05f-129">You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

