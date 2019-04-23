---
title: OpenFunction マクロ アクション
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288365"
---
# <a name="openfunction-macro-action"></a>OpenFunction マクロ アクション

**適用先:** Access 2013、Office 2013

In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>設定値

"OpenFunction/関数を開く" アクションの引数は次のとおりです。

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
<td><p><strong>Function Name/関数名</strong></p></td>
<td><p>開くユーザー定義関数の名前を指定します。 [マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>関数名</strong>] ボックスには、カレント データベース内のユーザー定義関数がすべて表示されます。 これは必須の引数です。ライブラリデータベースで<strong>function</strong>アクションを含むマクロを実行すると、最初にライブラリデータベースでこの名前の関数が検索され、次にカレントデータベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>ユーザー定義関数を開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>ユーザー定義関数を開くときのデータ入力モードを指定します。これはデータシート ビューで開いているユーザー定義関数にのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでユーザー定義関数をダブルクリックした場合や、ナビゲーション ウィンドウで関数を右クリックしてビューをクリックした場合と同じです。

Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.

> [!TIP]
> - You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.
> - If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.

To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.

