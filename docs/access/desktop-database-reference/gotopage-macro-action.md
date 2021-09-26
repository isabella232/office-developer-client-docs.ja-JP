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
ms.localizationpriority: medium
ms.openlocfilehash: 9e4d7acd7c0f07f4d18a0a997c999cb877dbcb45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626499"
---
# <a name="gotopage-macro-action"></a>GoToPage マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.

## <a name="setting"></a>設定

"GoToPage/ページの移動" アクションの引数は次のとおりです。

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
<td><p><strong>Page Number/ページ番号</strong></p></td>
<td><p>フォーカスを移動するページの数。 [マクロ ビルダー] ウィンドウの [<strong>アクション引数</strong>] セクションの [ページ番号] ボックスにページ番号を入力します。 <strong></strong> この引数を指定しないと、フォーカスはカレント ページにとどまります。 Right 引数と <strong>Down</strong> 引数 <strong>を</strong> 使用して、表示するページの一部を表示できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>ページの左端を表示する水平方向の位置を、そのページを表示するウィンドウの左端からの距離で指定します。"Down/下" 引数を指定する場合は、この引数は省略できません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>ページの上端を表示する垂直方向の位置を、そのページを表示するウィンドウの上端からの距離で指定します。"Right/右" 引数を指定する場合は、この引数は省略できません。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> "Right/右" 引数と "Down/下" 引数は、インチまたは cm 単位で指定します。どちらの単位を使用するかは、Windows コントロール パネルの地域の設定によって決まります。

## <a name="remarks"></a>注釈

このアクションを使用すると、指定ページの最初のコントロール (フォームのタブ オーダーで定義されたコントロール) を選択できます。フォーム上の特定のコントロールに移動するには、"GoToControl/コントロールの移動" アクションを使用します。

Access ウィンドウより大 **きいページを** 持つフォームには **、Right** 引数と Down 引数を使用できます。 " **Page Number/ページ番号** " 引数を使用して目的のページに移動し、次に " **Right/右** " 引数と " **Down/下** " 引数を使ってページの必要な部分を表示します。 このとき、ウィンドウの左上隅から、引数で指定した間隔を置いた位置に、ページの左上隅が表示されます。

You can't use the **GoToPage** action in the following cases:

- 非表示のフォームのページにフォーカスを移動する場合

- タブ コントロール内の別のページにフォーカスを移動する場合

To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.

