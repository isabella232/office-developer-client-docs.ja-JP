---
title: ShowToolbar マクロ アクション
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed69a84f9b1774b7c33711a0bb8e80da54e656cc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997931"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="cfa4b-102">ShowToolbar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="cfa4b-102">ShowToolbar macro action</span></span>

<span data-ttu-id="cfa4b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfa4b-104">**[アドイン**] タブのコマンドのグループを表示または非表示に**切り替えます**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="cfa4b-105">**ShowToolbar**アクションは、ショートカット メニューには影響しません。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="cfa4b-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="cfa4b-107">設定値</span><span class="sxs-lookup"><span data-stu-id="cfa4b-107">Setting</span></span>

<span data-ttu-id="cfa4b-108">**ShowToolbar**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfa4b-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="cfa4b-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cfa4b-110">説明</span><span class="sxs-lookup"><span data-stu-id="cfa4b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfa4b-111"><strong>Toolbar Name/ツール バー名</strong></span><span class="sxs-lookup"><span data-stu-id="cfa4b-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cfa4b-112"><strong>[アドイン</strong>] タブ上のコマンド グループの名前を表示または非表示にします。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="cfa4b-113">マクロ ビルダー] ウィンドウの [<strong>ツールバー名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、この操作によって影響を受けることができますすべての利用可能なグループを示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="cfa4b-114">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-114">This is a required argument.</span></span> <span data-ttu-id="cfa4b-115">ライブラリ データベースで<strong>ShowToolbar</strong>アクションを含むマクロを実行する場合は、まずライブラリ データベースで、[し、[現在のデータベース内にこの名前のグループの検索されます。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfa4b-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="cfa4b-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="cfa4b-117">表示または非表示] グループにあるかどうか、およびどのビューで表示または非表示にするを指定します。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="cfa4b-118">既定値は<strong>[はい]</strong> (常にグループを表示するです)。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="cfa4b-119">時間、<strong>適切な場所</strong>に適切なフォームまたはレポートがアクティブなときにのみ、グループを表示] または [<strong>いいえ</strong>常にグループを非表示にするすべてのグループを表示するには、 <strong>[はい]</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cfa4b-120">解説</span><span class="sxs-lookup"><span data-stu-id="cfa4b-120">Remarks</span></span>

<span data-ttu-id="cfa4b-121">マクロでこのアクションと条件式を組み合わせて使用すると、特定の条件に応じてグループの表示と非表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="cfa4b-122">1 つのフォームまたはレポート上の特定のグループを表示する場合は、グループを表示する**ShowToolbar**のアクションを含むマクロの名前に、フォームまたはレポートの**OnActivate**プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-122">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group.</span></span> <span data-ttu-id="cfa4b-123">グループを非表示にする**ShowToolbar**のアクションを含むマクロの名前に、フォームまたはレポートの**OnDeactivate**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-123">Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="cfa4b-124">組み込みのツールバーでは利用できない**できるようにする組み込みのツールバーを表示**] オプションを設定する場合または**False** (0) で、Visual Basic for Applications (VBA) のモジュールに**できない**プロパティを設定する場合にこのアクションを使用して非表示**False** **SetOption**メソッドを使用して VBA にします。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="cfa4b-125">VBA モジュールで**ShowToolbar**アクションを実行するには、 **DoCmd**オブジェクトの**ShowToolbar**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa4b-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

