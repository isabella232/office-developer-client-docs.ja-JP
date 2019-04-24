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
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306476"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="938fc-102">ShowToolbar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="938fc-102">ShowToolbar macro action</span></span>

<span data-ttu-id="938fc-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="938fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="938fc-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span><span class="sxs-lookup"><span data-stu-id="938fc-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="938fc-105">The **ShowToolbar** action does not affect shortcut menus.</span><span class="sxs-lookup"><span data-stu-id="938fc-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="938fc-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="938fc-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="938fc-107">設定値</span><span class="sxs-lookup"><span data-stu-id="938fc-107">Setting</span></span>

<span data-ttu-id="938fc-108">"ShowToolbar/ツールバーの表示" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="938fc-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938fc-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="938fc-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="938fc-110">説明</span><span class="sxs-lookup"><span data-stu-id="938fc-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938fc-111"><strong>Toolbar Name/ツール バー名</strong></span><span class="sxs-lookup"><span data-stu-id="938fc-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="938fc-112">表示と非表示を切り替える、[<strong>アドイン</strong>] タブ上のコマンド グループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="938fc-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="938fc-113">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ツール バー名</strong>] ボックスには、このアクションの影響を受ける使用可能なグループがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="938fc-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="938fc-114">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="938fc-114">This is a required argument.</span></span> <span data-ttu-id="938fc-115">ライブラリ データベースで "ShowToolbar/ツール バーの表示" アクションが定義されているマクロを実行すると、この名前のグループが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="938fc-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938fc-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="938fc-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="938fc-117">グループを表示するかどうか、また、どのビューで表示または非表示にするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="938fc-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="938fc-118">既定では、 <strong>[はい]</strong> (グループを常に表示) にします。</span><span class="sxs-lookup"><span data-stu-id="938fc-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="938fc-119">グループを常に表示する場合は [はい]、 <strong></strong>適切なフォームまたはレポートがアクティブな場合にのみグループを表示する場合は [いいえ<strong>]</strong>を選択し、常にグループを非表示にする場合は [<strong>いいえ</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="938fc-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="938fc-120">注釈</span><span class="sxs-lookup"><span data-stu-id="938fc-120">Remarks</span></span>

<span data-ttu-id="938fc-121">マクロでこのアクションと条件式を組み合わせて使用すると、特定の条件に応じてグループの表示と非表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="938fc-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="938fc-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span><span class="sxs-lookup"><span data-stu-id="938fc-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="938fc-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span><span class="sxs-lookup"><span data-stu-id="938fc-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="938fc-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="938fc-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

