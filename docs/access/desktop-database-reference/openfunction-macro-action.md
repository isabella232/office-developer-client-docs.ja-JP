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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720213"
---
# <a name="openfunction-macro-action"></a>OpenFunction マクロ アクション

**適用されます**Access 2013、Office 2013。

Access プロジェクトで、ユーザー定義関数をデータシート ビュー、インライン関数のデザイン ビュー、ビューの SQL テキスト エディターで開くに**OpenFunction**アクションを使用することができます (スカラーのまたはテーブル ユーザー定義関数)、または印刷プレビューします。 このアクションでは、データシート ビューで開くと、ユーザー定義関数を実行します。 また、ユーザー定義関数に対してデータ入力モードを選択して、ユーザー定義関数を表示するレコードを制限できます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

**OpenFunction**アクションには、次の引数があります。

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
<td><p>開くユーザー定義関数の名前。 マクロ ビルダー] ウィンドウの [<strong>関数名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースですべてのユーザー定義関数を示しています。 これは、必要な引数です。ライブラリ データベースで<strong>Function</strong>アクションが定義されたマクロを実行すると、Microsoft Access は最初ライブラリ データベースで、[し、[現在のデータベース内にこの名前の関数を検索します。</p></td>
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


## <a name="remarks"></a>解説

このアクションの動作は、ナビゲーション ウィンドウでユーザー定義関数をダブルクリックした場合や、ナビゲーション ウィンドウで関数を右クリックしてビューをクリックした場合と同じです。

ユーザー定義関数を開いているときに、デザイン ビューに切り替え、ユーザー定義関数に対して**データ モード**引数の設定を削除します。 再びデータシート ビューに切り替えても、元の設定には戻りません。

> [!TIP]
> - ナビゲーション ウィンドウでユーザー定義関数を選択し、マクロのアクション行にドラッグできます。 **OpenFunction**操作、ユーザー定義関数をデータシート ビューに表示を自動的に作成されます。
> - ユーザー定義関数を実行するときに表示されるシステム メッセージを表示したくない場合 (ユーザー定義関数を示す、レコードの数が影響を受けるアクションを使って、 **SetWarning**の表示を非表示にするこれらのメッセージです。

**OpenFunction**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenFunction**メソッドを使用します。

