---
title: "'OpenView/ビューを開く' マクロ アクション"
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad607f852f5af21bc2979bd635286b86d18489a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477467"
---
# <a name="openview-macro-action"></a>"OpenView/ビューを開く" マクロ アクション


**適用されます**Access 2013 |。Office 2013

Access プロジェクトで、 **OpenView**アクションをデータシート ビュー、デザイン ビュー、または印刷プレビューでビューを開くに使用できます。 データシート ビューで開いた場合、その名前のビューが実行されます。 ビューを開くときのデータ入力モードの設定を行ったり、ビューで表示するレコードを制限したりできます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**OpenView**アクションには、次の引数があります。

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
<td><p>開くビューの名前を指定します。 マクロ ビルダー] ウィンドウの [<strong>ビュー名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベース内のすべてのビューを示しています。 この引数は省略できません。 ライブラリ データベースで、 <strong>OpenView</strong>アクションを含むマクロを実行する場合は、最初の検索にライブラリ データベースで、し、[現在のデータベース内にこの名前のビューです。</p></td>
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


## <a name="remarks"></a>解説

このアクションの動作は、ナビゲーション ウィンドウでビューをダブルクリックした場合や、ナビゲーション ウィンドウでビューを右クリックして目的のコマンドをクリックした場合と同じです。

**ヒント**

  - ナビゲーション ウィンドウからマクロのアクション行にビューをドラッグできます。 ビューをデータシート ビューで開く**OpenView**アクションが自動的に作成します。

  - (ことを示すビューとレコードの数が影響を受ける)、ビューを実行するときに通常表示されるシステム メッセージが表示されない場合は、これらのメッセージの表示を抑制する**SetWarning**アクションを使用することができます。

**OpenView**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenView**メソッドを使用します。

