---
title: RecordsetOptionEnum 列挙 (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476663"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>RecordsetOptionEnum 列挙 (DAO)


**適用されます**Access 2013 |。Office 2013

**OpenRecordset** メソッドで、新しい **Recordset** オブジェクトの特性を指定するために使用します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>ユーザーが新しいレコードをダイナセットに追加するのを許可しますが、既存のレコードを読み取ることは許可しません。</p></td>
</tr>
<tr class="even">
<td><p>指定できます。</p></td>
<td><p>32</p></td>
<td><p>ダイナセット内の他のレコードに影響を与えないフィールドにのみ更新を適用します (ダイナセット タイプとスナップショット タイプのみ)。</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>他のユーザーが Recordset のレコードを読み取れないようにします (テーブル タイプのみ)。</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>他のユーザーが Recordset のレコードを変更できないようにします。</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>SQLPrepare ODBC 関数を最初に呼び出さずに、クエリを実行します。</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p> 
128 
</p></td>
<td><p>エラーが発生した場合、更新をロールバックします。</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>前方スクロールのみのスナップショット タイプ Recordset を作成します (スナップショット タイプのみ)。</p></td>
</tr>
<tr class="even">
<td><p>組み合わせて</p></td>
<td><p>16</p></td>
<td><p>他のレコードに影響が及ぶ場合でも、すべてのダイナセット フィールドに更新を適用します (ダイナセット タイプとスナップショット タイプのみ)。</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Recordset を読み取り専用として開きます。</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>クエリを非同期で実行します。</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>編集中のデータを別のユーザーが変更している場合、実行時エラーを生成します (ダイナセット タイプのみ)。</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>ODBC データベースに SQL ステートメントを送信します (スナップショット タイプのみ)。</p></td>
</tr>
</tbody>
</table>

