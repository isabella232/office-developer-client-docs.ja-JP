---
title: ODBC スカラー関数
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288512"
---
# <a name="odbc-scalar-functions"></a>ODBC スカラー関数

**適用先:** Access 2013、Office 2013

Microsoft access SQL では、スカラー関数に対して定義されている ODBC 構文の使用をサポートしています。 

たとえば、クエリ`SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5`は、株の価格の変更の絶対値が5を超えたすべての行を返します。

ODBC 定義構文を使用できるスカラー関数のサブセットがサポートされています。次の表は、使用できるスカラー関数の一覧を示します。

SQL ステートメントで関数を使用するためのエスケープ構文の完全な説明と、引数の記述方法については、ODBC のマニュアルを参照してください。

## <a name="string-functions"></a>文字列関数

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>長さ</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>CHAR</p></td>
<td><p>ら</p></td>
<td><p>SPACE</p></td>
</tr>
<tr class="odd">
<td><p>CONCAT</p></td>
<td><p>LTRIM</p></td>
<td><p>副</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>RIGHT</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>LEFT</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>数値関数

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>窓</p></td>
<td><p>SIN</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>ログイン</p></td>
<td><p>SQRT</p></td>
</tr>
<tr class="odd">
<td><p>限度</p></td>
<td><p>POWER</p></td>
<td><p>TAN</p></td>
</tr>
<tr class="even">
<td><p>面上</p></td>
<td><p>RAND</p></td>
<td><p>モダン</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p>付け</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Time & Date 関数

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>日付 (curdate</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>月末</p></td>
</tr>
<tr class="even">
<td><p>curtime</p></td>
<td><p>今年</p></td>
<td><p>回</p></td>
</tr>
<tr class="odd">
<td><p>今</p></td>
<td><p>毎</p></td>
<td><p>現</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>部分</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>補助</p></td>
<td><p>dayname</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>データ型の変換

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>変換</p></td>
<td><p>次のデータ型にリテラル文字列を変換することができます。SQL_FLOAT、SQL_DOUBLE、SQL_NUMERIC、SQL_INTEGER、SQL_REAL、SQL_SMALLINT、SQL_VARCHAR および SQL_DATETIME。</p></td>
</tr>
</tbody>
</table>

