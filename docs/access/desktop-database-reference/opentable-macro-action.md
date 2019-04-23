---
title: OpenTable マクロ アクション
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288295"
---
# <a name="opentable-macro-action"></a>OpenTable マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.

## <a name="setting"></a>Setting

"OpenTable/テーブルを開く" アクションの引数は次のとおりです。

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
<td><p><strong>Table Name/テーブル名</strong></p></td>
<td><p>開くテーブル名を指定します。 [マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>テーブル名</strong>] ボックスには、カレント データベース内のテーブルがすべて表示されます。 この引数は省略できません。 ライブラリ データベースで "OpenTable/テーブルを開く" アクションが定義されているマクロを実行すると、この名前のテーブルが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>テーブルを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>テーブルを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているテーブルにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでテーブルをダブルクリックした場合や、ナビゲーション ウィンドウでテーブルを右クリックしてビューをクリックした場合と同じです。

> [!TIP]
> You can drag a table from the Navigation Pane to a macro action row. This automatically creates an **OpenTable** action that opens the table in Datasheet view.

To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.

