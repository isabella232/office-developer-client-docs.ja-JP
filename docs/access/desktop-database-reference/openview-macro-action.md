---
title: OpenView マクロ アクション
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288302"
---
# <a name="openview-macro-action"></a>OpenView マクロ アクション

**適用先:** Access 2013、Office 2013

In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>設定値

"OpenView/ビューを開く" アクションの引数は次のとおりです。

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
<td><p><strong>View Name/ビュー名</strong></p></td>
<td><p>開くビューの名前を指定します。 [マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ビュー名</strong>] ボックスには、カレントデータベースのすべてのビューが表示されます。 この引数は省略できません。 ライブラリ データベースで "OpenView/ビューを開く" アクションが定義されているマクロを実行すると、この名前のビューが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>ビューを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>ビューを開くときのデータ入力モードを指定します。これはデータシート  ビューで開いているビューにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでビューをダブルクリックした場合や、ナビゲーション ウィンドウでビューを右クリックして目的のコマンドをクリックした場合と同じです。

> [!TIP]
> - You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.
> - If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.

To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.

