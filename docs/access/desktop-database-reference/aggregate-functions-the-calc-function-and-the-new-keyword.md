---
title: 集計関数、CALC 関数、および NEW キーワード
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db726ea0b51a345e0e40c9814cef100b90b1350f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947890"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>集計関数、CALC 関数、および NEW キーワード


**適用されます**Access 2013、Office 2013。

データ シェイプと、次の関数がサポートされています。 *チャプター エイリアス*は、操作することで、列を含むチャプターに割り当てられた名前です。

チャプター エイリアスは、完全修飾名、*列名、* すべてピリオドで区切られたを含むチャプターにつながるので構成されている可能性があります。 など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。

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
<td><p>合計 (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列に含まれるすべての値の合計を計算します。</p></td>
</tr>
<tr class="even">
<td><p>AVG (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列に含まれるすべての値の平均値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>MAX (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列内の最大値を計算します。</p></td>
</tr>
<tr class="even">
<td><p>MIN (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列内の最小値を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>カウント (<em>チャプター エイリアス</em>[.<em>列名</em>])</p></td>
<td><p>指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</p></td>
</tr>
<tr class="even">
<td><p>STDEV (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列内の標準偏差を計算します。</p></td>
</tr>
<tr class="odd">
<td><p>任意 (<em>チャプター エイリアス</em>です<em>。列名</em>)</p></td>
<td><p>指定された列の値です。ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。
</p>

> [!NOTE]
> 列の値がチャプター内の全行について同じでない場合、SHAPE コマンドは、ANY 関数の値として、複数ある値のうち任意のものを 1 つ返します。


<p></p></td>
</tr>
</tbody>
</table>


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
<td><p>計算式 (<em>式</em>)</p></td>
<td><p>任意の式を計算しますが、CALC 関数を含む <strong>Recordset</strong> の行のみが対象となります。「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」に記載されている関数を使用した任意の式を計算できます。</p></td>
</tr>
</tbody>
</table>


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
<td><p>新しい<em>フィールドの種類</em>[(<em>幅</em> | <em>スケール</em> | <em>精度</em> | <em>エラー</em> [、<em>スケール</em> | <em>エラー</em>])]</p></td>
<td><p>指定された型の空の列を <strong>Recordset</strong> に追加します。</p></td>
</tr>
</tbody>
</table>


NEW キーワードと共に渡す*フィールドの型*には、次のデータ型のいずれかを指定できます。

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
<td><p>adBinary、ない、adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>が</p></td>
<td><p>ファミリ、それぞれ、adLongVarChar</p></td>
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


新しいフィールドがあるとき decimal 型 (OLE db では、DBTYPE\_10 進数、または ADO では、adDecimal)、有効桁数と小数点部桁数の値を指定する必要があります。

