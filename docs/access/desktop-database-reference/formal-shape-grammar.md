---
title: 正式な Shape 文法
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1fcc725a554496f7aa6c7e9ad07402aecabf9416
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615453"
---
# <a name="formal-shape-grammar"></a>正式な Shape 文法

**適用先**: Access 2013、Office 2013

すべての Shape コマンドの作成における正式な文法を以下に示します。

  - 文法的に必須の項は、山かっこ ("\<\>") で区切られたテキスト文字列です。

  - 省略可能な用語は、角かっこ (" ") で \[ \] 区切ります。

  - パイプ記号 ("|") は、代替項目であることを示します。

  - 省略符号 ("...") は、繰り返し代替項目であることを示します。

  - *Alpha* は、英字による文字列であることを示します。

  - *Digit* は、数字による文字列であることを示します。

  - *Unicode-digit* は、Unicode 数字による文字列であることを示します。

その他のすべての項はリテラルです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>用語</p></th>
<th><p>定義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;shape-command&gt;</p></td>
<td><p>SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{ &lt; provider-command-text &gt; } |<br />
( &lt; shape-command &gt; ) |<br />
TABLE &lt; 引用符で囲まれた名前&gt; |<br />
&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>APPEND &lt; エイリアスフィールド リスト&gt; |</p>
<p>COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field..] &gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>( &lt; relation-exp &gt; ) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p>
<p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;フィールド名 &gt; TO &lt; child-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;child-ref&gt;</p></td>
<td><p>&lt;フィールド名&gt; |</p>
<p>PARAMETER &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;number&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;フィールドリスト&gt;</p></td>
<td><p>&lt;field-name &gt; [, &lt; field-name &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SUM( &lt; 修飾フィールド名 &gt; ) |</p>
<p>AVG( &lt; 修飾フィールド名 &gt; ) |</p>
<p>MIN( &lt; qualified-field-name &gt; ) |</p>
<p>MAX( &lt; qualified-field-name &gt; ) |</p>
<p>COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</p>
<p>STDEV( &lt; qualified-field-name &gt; ) |</p>
<p>ANY( &lt; 修飾フィールド名 &gt; )</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC( &lt; 式 &gt; )</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾フィールド名&gt;</p></td>
<td><p>&lt;alias &gt; .[ &lt;alias &gt; ...] &lt;フィールド名&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;フィールド名&gt;</p></td>
<td><p>&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-name&gt;</p></td>
<td><p>&quot;&lt;string&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>[ &lt; string &gt; ] |</p>
<p>&lt;name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾名&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;name&gt;</p></td>
<td><p>α [ α | | _ | # | : | ..]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;number&gt;</p></td>
<td><p>digit [digit...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NEW &lt; フィールド型 &gt; [( number &lt; &gt; [, number &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-type&gt;</p></td>
<td><p>OLE DB または ADO のデータ型</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...</p></td>
</tr>
<tr class="odd">
<td><p>&lt;式&gt;</p></td>
<td><p>同じ行でオペランドが他の非 CALC 列の Visual Basic for Application 式</p></td>
</tr>
</tbody>
</table>

