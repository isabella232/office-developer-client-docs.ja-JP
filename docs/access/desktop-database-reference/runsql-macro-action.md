---
title: RunSQL マクロ アクション
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308996"
---
# <a name="runsql-macro-action"></a>RunSQL マクロ アクション

**適用先:** Access 2013、Office 2013

**RunSQL** アクションを使用すると、Access のアクション クエリを、対応する SQL ステートメントを使用して実行できます。また、データ定義クエリも実行できます。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>設定値

**RunSQL** アクションの引数は次のとおりです。

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
<td><p><strong>SQL Statement/SQL ステートメント</strong></p></td>
<td><p>実行するアクション クエリまたはデータ定義クエリに対応する SQL ステートメントを指定します。このステートメントの最大長は 255 バイトです。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Use Transaction/トランザクションの使用</strong></p></td>
<td><p>このクエリをトランザクションに含める場合は [ <strong>はい</strong>] を選択します。このトランザクションを使用しない場合は [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>はい</strong>] です。この引数に [ <strong>いいえ</strong>] を選択すると、クエリの実行速度が上がります。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

アクション クエリを使用すると、レコードの追加、削除、および更新を実行したり、クエリの結果セットを新しいテーブルとして保存することができます。データ定義クエリを使用すると、テーブルの作成、変更、および削除とインデックスの作成および削除を実行できます。 **RunSQL** アクションを使用すると、ストアド クエリを使用せず、このような処理をマクロから直接実行できます。

255 バイトを超える SQL ステートメントを入力する必要がある場合は、Visual Basic for Applications (VBA) モジュールで **DoCmd** オブジェクトの **RunSQL** メソッドを使用します。VBA では、最大 32,768 バイトの SQL ステートメントを入力できます。

Access のクエリは、実際には、クエリ ウィンドウのデザイン グリッドを使用してクエリをデザインするときに作成される SQL ステートメントです。次の表は、Access のアクション クエリとデータ定義クエリ、およびこれらのクエリに対応する SQL ステートメントを示しています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>クエリの種類</p></th>
<th><p>SQL ステートメント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>アクション</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>追加</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>削除</p></td>
<td><p>DELETE</p></td>
</tr>
<tr class="even">
<td><p>テーブル作成</p></td>
<td><p>[...] を選択します。分ける</p></td>
</tr>
<tr class="odd">
<td><p>更新</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>データ定義 (SQL 固有)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>テーブルの作成</p></td>
<td><p>CREATE TABLE</p></td>
</tr>
<tr class="even">
<td><p>テーブルの変更</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>テーブルの削除</p></td>
<td><p>DROP TABLE</p></td>
</tr>
<tr class="even">
<td><p>インデックスの作成</p></td>
<td><p>CREATE INDEX</p></td>
</tr>
<tr class="odd">
<td><p>インデックスの削除</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

これらのステートメントと IN 句を組み合わせて使用すると、別のデータベース内のデータを変更することもできます。

> [!NOTE]
> [!メモ] 選択クエリまたはクロス集計クエリをマクロから実行するには、 **OpenQuery** アクションの "View/ビュー" 引数を使用して、既存の選択クエリまたはクロス集計クエリをデータシート ビューで開きます。また、同様に、既存のアクション クエリおよび SQL 固有のクエリを実行することもできます。
