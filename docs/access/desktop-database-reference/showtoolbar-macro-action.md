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
ms.localizationpriority: medium
ms.openlocfilehash: 17a88c2b05c6bb66ab0d5e10c38bf17f302f2da4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611505"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.

> [!NOTE]
> - The **ShowToolbar** action does not affect shortcut menus.
> - このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"ShowToolbar/ツールバーの表示" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Toolbar Name/ツール バー名</strong></p></td>
<td><p>表示と非表示を切り替える、[<strong>アドイン</strong>] タブ上のコマンド グループの名前を指定します。 [マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ツール バー名</strong>] ボックスには、このアクションの影響を受ける使用可能なグループがすべて表示されます。 この引数は省略できません。 ライブラリ データベースで "ShowToolbar/ツール バーの表示" アクションが定義されているマクロを実行すると、この名前のグループが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>グループを表示するかどうか、また、どのビューで表示または非表示にするかを指定します。 既定値は <strong>[はい]</strong> です (グループをすべての時間で表示します)。 [<strong>はい]</strong>を選択すると、グループをすべての<strong></strong>回で表示できます。適切なフォームまたはレポートがアクティブな場合にのみグループを表示するには[適切]、グループを非表示にする場合は<strong>[いいえ</strong>] を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

マクロでこのアクションと条件式を組み合わせて使用すると、特定の条件に応じてグループの表示と非表示を切り替えることができます。

If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.

The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.

To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.

