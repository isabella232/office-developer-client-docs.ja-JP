---
title: RunMenuCommand マクロ アクション
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f01fc72a620e5c08a6f98b4b69a8eb8da7b98bbb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925675"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="a3348-102">RunMenuCommand マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a3348-102">RunMenuCommand macro action</span></span>


<span data-ttu-id="a3348-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a3348-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3348-104">**RunMenuCommand**アクションを使用すると、組み込みの Access コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a3348-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="a3348-105">設定値</span><span class="sxs-lookup"><span data-stu-id="a3348-105">Setting</span></span>

<span data-ttu-id="a3348-106">**RunMenuCommand**アクションには、次のアクションの引数があります。</span><span class="sxs-lookup"><span data-stu-id="a3348-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3348-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a3348-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a3348-108">説明</span><span class="sxs-lookup"><span data-stu-id="a3348-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3348-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="a3348-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="a3348-p101">実行するコマンドの名前を指定します。[<strong>コマンド</strong>] ボックスには、Access の使用可能な組み込みのコマンドが五十音順で表示されます。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="a3348-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3348-113">解説</span><span class="sxs-lookup"><span data-stu-id="a3348-113">Remarks</span></span>

<span data-ttu-id="a3348-114">**RunMenuCommand**アクションを使用すると、カスタム メニュー バー、グローバル メニュー バー、カスタム ショートカット メニューまたはグローバル ショートカット メニューから、Access コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a3348-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="a3348-115">マクロ内で条件付き書式**RunMenuCommand**アクションを使用するには一定の条件に従ってコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a3348-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a3348-116">[<STRONG>ファイル</STRONG>] タブをクリックし、[<STRONG>最近使用した</STRONG>最近使用したデータベースを示しています。</span><span class="sxs-lookup"><span data-stu-id="a3348-116">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases.</span></span> <span data-ttu-id="a3348-117"><STRONG>開く</STRONG>をクリックする代わりにこれらのデータベースのいずれかをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="a3348-117">You can click one of these databases instead of clicking <STRONG>Open</STRONG>.</span></span> <span data-ttu-id="a3348-118">データベースのこれらの項目は、<STRONG>コマンド</STRONG>の引数のドロップダウン リスト ボックスに表示されないし、 <STRONG>RunMenuCommand</STRONG>アクションを使用してマクロ内で使用できません。</span><span class="sxs-lookup"><span data-stu-id="a3348-118">These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="a3348-119">以前のバージョンの Access から Access データベースを変換するときにいくつかのコマンドが利用できなくです。</span><span class="sxs-lookup"><span data-stu-id="a3348-119">When you convert an Access database from a previous version of Access, some commands may no longer be available.</span></span> <span data-ttu-id="a3348-120">コマンドでは、可能性がありますが名前が変更されて、別のメニューに移動または、Access で使用可能な不要になった場合があります。</span><span class="sxs-lookup"><span data-stu-id="a3348-120">A command may have been renamed, moved to a different menu, or may no longer be available in Access.</span></span> <span data-ttu-id="a3348-121">**RunMenuCommand**アクションには、このようなコマンドの動作を**DoMenuItem**を変換できません。</span><span class="sxs-lookup"><span data-stu-id="a3348-121">The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions.</span></span> <span data-ttu-id="a3348-122">マクロを開くと、このようなコマンドの**コマンド**の引数が空で、 **RunMenuCommand**アクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3348-122">When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands.</span></span> <span data-ttu-id="a3348-123">マクロを編集、有効なコマンド引数を入力し、または**RunMenuCommand**アクションを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3348-123">You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="a3348-124">**RunMenuCommand**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **Application**オブジェクトの**RunCommand**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3348-124">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object.</span></span> <span data-ttu-id="a3348-125">(これは、 **DoCmd**オブジェクトの**RunCommand**メソッドと同等) です。</span><span class="sxs-lookup"><span data-stu-id="a3348-125">(This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

