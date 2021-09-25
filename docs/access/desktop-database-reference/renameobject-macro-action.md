---
title: RenameObject マクロ アクション
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: bafbde738154993f3fea0c4f2537a9807009b966
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617455"
---
# <a name="renameobject-macro-action"></a>RenameObject マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **RenameObject** action to rename a specified database object.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。

## <a name="setting"></a>Setting

"RenameObject/オブジェクト名の変更" アクションの引数は次のとおりです。

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
<td><p><strong>New Name/新しい名前</strong></p></td>
<td><p>データベース オブジェクトに付ける新しい名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>新しい名前</strong>] ボックスにオブジェクト名を入力します。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクトの種類</strong></p></td>
<td><p>名前を変更するオブジェクトの種類を指定します。[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトの名前を変更する場合は、この引数を指定しません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Old Name/古い名前</strong></p></td>
<td><p>名前を変更するオブジェクトの名前。 [ <strong>古い名前]</strong> ボックスには、引数 Object Type で選択された型のデータベース内のすべてのオブジェクト <strong>が表示</strong> されます。 If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</p><p><strong>注</strong>: ライブラリ データベースで Rename<STRONG></STRONG>アクションを含むマクロを実行すると、まずライブラリ データベースでこの名前のオブジェクトが検索され、次に現在のデータベースで検索されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

データベース オブジェクトの新しい名前は、Access のオブジェクトの名前付け規則に従う必要があります。

開いているオブジェクトの名前は変更できません。

If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.

You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.

This action differs from the **CopyObject** action, which creates a copy of the object under a new name.

To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.

