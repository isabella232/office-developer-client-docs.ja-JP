---
title: 集計関数、CALC 関数、NEW キーワード
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297194"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>集計関数、CALC 関数、NEW キーワード


**適用先:** Access 2013、Office 2013

データ シェイプ機能では、次の関数がサポートされています。 演算の対象となる列を含むチャプターに付けられる名前は、"チャプター エイリアス" です。

チャプター エイリアスは、完全修飾名で表すことができます。これには、対象となる列名を含むチャプターに至るまでの各チャプター列の名前を、ピリオドで区切って表記します。たとえば、親チャプター chap1 に子チャプター chap2 が含まれており、chap2 に集計列 amt が含まれている場合、完全修飾名は chap1.chap2.amt となります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>集計関数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM (<em>チャプターエイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列に含まれるすべての値の合計を計算します。</p></td>
</tr>
<tr class="even">
<td><p>AVG (<em>チャプター-エイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列に含まれるすべての値の平均値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>MAX (<em>チャプターエイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列内の最大値を計算します。</p></td>
</tr>
<tr class="even">
<td><p>MIN (<em>チャプターエイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列内の最小値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>COUNT (<em>chapter-alias</em>[.<em>列名</em>])</p></td>
<td><p>指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</p></td>
</tr>
<tr class="even">
<td><p>STDEV (<em>チャプターエイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列内の標準偏差を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>任意 (<em>チャプター-エイリアス)</em><em>列名</em>)</p></td>
<td><p>指定された列の値です。 ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。</p><p><strong>注</strong>: 列に、チャプター内のすべての行について同じ値が含まれていない場合、SHAPE コマンドは、ANY 関数の値となる値の1つを任意に返します。</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>計算済みの式</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC (<em>式</em>)</p></td>
<td><p>任意の式を計算しますが、CALC 関数を含む <strong>Recordset</strong> の行のみが対象となります。「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」に記載されている関数を使用した任意の式を計算できます。</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>NEW キーワード</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>新しい<em>フィールドの種類</em>[(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</p></td>
<td><p>指定された型の空の列を <strong>Recordset</strong> に追加します。</p></td>
</tr>
</tbody>
</table>

<br/>

NEW キーワードと共に渡すフィールドの型には、次のデータ型のうちいずれかを指定できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>OLE DB のデータ型</p></th>
<th><p>該当する ADO のデータ型</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adbstr</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adboolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adアン signedtinyint</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adtinyint</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adアン signedsmallint</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adアン signedint</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adbigint</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adアン signedbigint</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adguid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adbinary、い、adlongvarbinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adchar、adVarChar、adlongvarchar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adwchar、adVarWChar、adlongvarwchar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>addbdate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>addbtime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>addbtimestamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adfiletime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>aderror</p></td>
</tr>
</tbody>
</table>


新しいフィールドの型が decimal (OLE DB、DBTYPE\_decimal、または ADO, adDecimal) の場合、精度とスケールの値を指定する必要があります。

