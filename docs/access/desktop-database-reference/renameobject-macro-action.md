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
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698387"
---
# <a name="renameobject-macro-action"></a>RenameObject マクロ アクション

**適用されます**Access 2013、Office 2013。

**RenameObject**アクションを使用するには、指定されたデータベース オブジェクトの名前を変更します。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。

## <a name="setting"></a>設定値

**RenameObject**アクションには、次の引数があります。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>名前を変更するオブジェクトの種類を指定します。[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトの名前を変更する場合は、この引数を指定しません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Old Name/古い名前</strong></p></td>
<td><p>名前を変更するオブジェクトの名前。 <strong>古い名前</strong>] ボックスでは、<strong>オブジェクトの種類</strong>の引数で選択した種類のデータベース内のすべてのオブジェクトを示しています。 <strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</p><p><strong>注</strong>: 場合は、ライブラリ データベースで<STRONG>名前を変更</STRONG>アクションを含むマクロを実行すると、最初の検索にライブラリ データベースで、し、[現在のデータベース内にこの名前のオブジェクト。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

データベース オブジェクトの新しい名前は、Access のオブジェクトの名前付け規則に従う必要があります。

開いているオブジェクトの名前は変更できません。

**オブジェクトの種類**と、**古い名前**の引数を空白のままにする場合は、ナビゲーション ウィンドウで選択したオブジェクトが変更されます。 ナビゲーション ウィンドウでオブジェクトを選択するには、 **[はい]** に設定**をナビゲーション ウィンドウ**に引数を指定して**SelectObject**アクションを使用できます。

ナビゲーション ウィンドウで右クリックし、**名前の変更**をクリックすると新しい名前を入力して、オブジェクトを変更することもできます。 **RenameObject**アクションでは、ナビゲーション ウィンドウでオブジェクトを最初に選択する必要はありませんし、新しい名前を入力するマクロを停止する必要はありません。

このアクションは、 **CopyObject**アクションの新しい名前の下にあるオブジェクトのコピーが作成されるとは異なります。

Visual Basic for Applications (VBA) モジュールに**RenameObject**アクションを実行するには、 **DoCmd**オブジェクトの**Rename**メソッドを使用します。

