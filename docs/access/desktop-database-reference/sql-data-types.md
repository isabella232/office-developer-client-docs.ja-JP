---
title: SQL データ型 (Access デスクトップ データベース リファレンス)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 0c3e12a1ff9f02f3b2ad85ed47ee496b998b73c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617413"
---
# <a name="sql-data-types"></a>SQL データ型

**適用先**: Access 2013、Office 2013

Microsoft Access データベース エンジン SQL のデータ型は、Microsoft Jet データベース エンジンで定義される 13 種類の基本データ型と、それらのデータ型として認識されるいくつかの別名で構成されます。

次の表に主要な SQL Server データ型を一覧表示します。これらの基本データ型を次の表に示します。同義語については、「[Microsoft Access データベース エンジン SQL 予約語](sql-reserved-words.md)」を参照してください。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>データ型</p></th>
<th><p>記憶領域サイズ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 文字あたり 1 バイト</p></td>
<td><p>このデータ型のフィールドには、どの型のデータでも格納できます。他のデータ型への変換 (たとえば、TEXT 型へ) は行われません。バイナリ フィールドにデータを入力する方法は、データをどのように出力するかを決めるものです。</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 バイト</p></td>
<td><p>"はい" と "いいえ" の値と、このいずれかの値のみを含むフィールド。</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 バイト</p></td>
<td><p>0 ～ 255 の整数値。</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 バイト</p></td>
<td><p>-922,337,203,685,477.5808 ～ 922,337,203,685,477.5807 の範囲の整数。</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (「DOUBLE」を参照)</p></td>
<td><p>8 バイト</p></td>
<td><p>100 ～ 9999 年の日付または時刻の値。</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 ビット</p></td>
<td><p>リモート プロシージャ コールで使用される一意の識別番号。</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 バイト</p></td>
<td><p>- 3.402823E38 ～ - 1.401298E-45 の負の値、1.401298E-45 ～ 3.402823E38 の正の値、および 0 の単精度浮動小数点値。</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 バイト</p></td>
<td><p>– 1.79769313486232E308 ～ – 4.94065645841247E-324 の負の値、4.94065645841247E-324 ～ 1.79769313486232E308 の正の値、および 0 の倍精度浮動小数点値。</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 バイト</p></td>
<td><p>-32,768 ～ 32,767 の整数値 (次の「メモ」を参照)。</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 バイト</p></td>
<td><p>-2,147,483,648 ～ 2,147,483,647 の整数値 (次の「メモ」を参照)。</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 バイト</p></td>
<td><p>1028 - 1 ～ - 1028 - 1 の値を格納する真数データ型。有効桁数 (1 ～ 28) と小数点以下桁数 (0 ～ 定義された精度) の両方を定義できます。既定の有効桁数は 18、小数点以下桁数は 0 です。</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>1 文字あたり 2 バイト (「メモ」を参照)</p></td>
<td><p>0 ～ 2.14 GB。</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>必須</p></td>
<td><p>0 ～ 2.14 GB。OLE オブジェクトで使用。</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>1 文字につき 2 バイト (次の「メモ」を参照)</p></td>
<td><p>0 ～ 255 文字</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - [ALTER TABLE ステートメント](alter-table-statement-microsoft-access-sql.md)を使用して、シード値とインクリメント値を変更できます。変更した後にテーブルに挿入された行の列には、新しいシード値とインクリメント値に従って自動的に作成された値が格納されます。変更前と変更後のシード値およびインクリメント値に従って作成された値が一致する場合は、複製が作成されます。列が主キーである場合は、新しい列を挿入すると、複製の作成時にエラーになります。
> - 自動インクリメントが設定されている列に対して最後に使用された値を調べるために、SELECT @@IDENTITY ステートメントを使用することができます。テーブル名を指定することはできません。最後に更新されたテーブルで、自動インクリメントが設定された列に格納されている値が返されます。
