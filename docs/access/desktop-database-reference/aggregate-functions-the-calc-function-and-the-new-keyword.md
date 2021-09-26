---
title: 集計関数、CALC 関数、NEW キーワード
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 33bb2aa973e91293c45d3d8bebbf57d6d7b7c20d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607438"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>集計関数、CALC 関数、NEW キーワード


**適用先**: Access 2013、Office 2013

データ シェイプ機能では、次の関数がサポートされています。演算の対象となる列を含むチャプターに付けられる名前は、"チャプター エイリアス" です。

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
<td><p>SUM(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列に含まれるすべての値の合計を計算します。</p></td>
</tr>
<tr class="even">
<td><p>AVG(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列に含まれるすべての値の平均値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>MAX(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列内の最大値を計算します。</p></td>
</tr>
<tr class="even">
<td><p>MIN(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列内の最小値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</p></td>
<td><p>指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</p></td>
</tr>
<tr class="even">
<td><p>STDEV(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列内の標準偏差を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>ANY(<em>chapter-alias</em>.<em>column-name</em>)</p></td>
<td><p>指定された列の値です。ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。
</p><p><strong>注</strong>: 列にチャプター内のすべての行に同じ値が含まれている場合、SHAPE コマンドは ANY 関数の値として任意に 1 つの値を返します。</p></td>
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
<td><p>CALC(<em>式</em>)</p></td>
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
<td><p>NEW<em>フィールド型</em>[(<em>width</em>  |  <em>scale precision</em>  |  <em></em>  |  <em>error</em> [, <em>scale</em>  |  <em>error</em>])]</p></td>
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
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adBinary、AdVarBinary、adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adChar、adVarChar、adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adWChar、adVarWChar、adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


新しいフィールドが decimal 型 (OLE DB、DBTYPE DECIMAL、または ADO の adDecimal) の場合は、精度とスケールの値を指定する \_ 必要があります。

