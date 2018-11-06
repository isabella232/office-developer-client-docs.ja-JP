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
ms.openlocfilehash: d80065c976a014ccf379bdc2016b0324cb02b269
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998148"
---
# <a name="opentable-macro-action"></a>OpenTable マクロ アクション

**適用されます**Access 2013、Office 2013。

**OpenTable**アクションを使用すると、データシート ビュー、デザイン ビュー、または印刷プレビューでテーブルを開きます。 テーブルを開くときのデータ入力モードを選択することもできます。

## <a name="setting"></a>設定値

**OpenTable**アクションには、次の引数があります。

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
<td><p>開くテーブル名を指定します。 マクロ ビルダー] ウィンドウの [<strong>テーブル名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベース内のすべてのテーブルを表示します。 この引数は省略できません。 ライブラリ データベースで<strong>OpenTable</strong>アクションを含むマクロを実行する場合 Microsoft Access は、そのライブラリ データベースで、次に現在のデータベースで最初にこの名前のテーブルを探します。</p></td>
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

## <a name="remarks"></a>解説

このアクションの動作は、ナビゲーション ウィンドウでテーブルをダブルクリックした場合や、ナビゲーション ウィンドウでテーブルを右クリックしてビューをクリックした場合と同じです。

> [!TIP]
> ナビゲーション ウィンドウからテーブルをドラッグするにはマクロのアクション行にします。 テーブルをデータシート ビューで開きます**OpenTable**アクションが自動的に作成します。

**OpenTable**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenTable**メソッドを使用します。

