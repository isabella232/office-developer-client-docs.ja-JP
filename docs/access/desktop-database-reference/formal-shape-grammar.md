---
title: 正式な Shape 文法
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292322"
---
# <a name="formal-shape-grammar"></a>正式な Shape 文法

**適用先:** Access 2013、Office 2013

すべての Shape コマンドの作成における正式な文法を以下に示します。

  - 文法的に必須の項は、山かっこ ("\<\>") で区切られたテキスト文字列です。

  - 省略可能な用語は、角かっこ (\[ \]"") で区切ります。

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
<td><p>&lt;shape-コマンド&gt;</p></td>
<td><p>shape [&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]] [&lt;shape-action&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{&lt;プロバイダ-コマンド-テキスト&gt;} |<br />
(&lt;図形-コマンド&gt;) |<br />
引用符&lt;で囲まれたテーブル名&gt; |<br />
&lt;引用符で囲まれた名前&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;図形-アクション&gt;</p></td>
<td><p>エイリアス&lt;フィールドリストを追加する&gt; |</p>
<p>エイリアス&lt;でフィールドを計算する&gt; -リスト&lt;(フィールドリスト&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;エイリアスが付いたフィールドリスト&gt;</p></td>
<td><p>&lt;エイリアスフィールド&gt; [、 &lt;エイリアスフィールド]&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;エイリアスフィールド&gt;</p></td>
<td><p>&lt;フィールド-exp&gt; [[AS] &lt;エイリアス&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;フィールド exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;計算済-exp&gt; |</p>
<p>&lt;集計-exp&gt; |</p>
<p>&lt;新規-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]</p>
<p>&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-リスト&gt;</p></td>
<td><p>&lt;リレーションシップ-同&gt;一 [ &lt;(リレーション&gt;)]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation&gt;</p></td>
<td><p>&lt;フィールド名&gt;と&lt;子の参照&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;子参照&gt;</p></td>
<td><p>&lt;フィールド名&gt; |</p>
<p>パラメーター &lt;param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;パラメーター ref&gt;</p></td>
<td><p>&lt;件数&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;フィールドリスト&gt;</p></td>
<td><p>&lt;フィールド名&gt; [、 &lt;フィールド名]&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;集計-exp&gt;</p></td>
<td><p>SUM (&lt;修飾フィールド名&gt;) |</p>
<p>AVG (&lt;修飾フィールド名&gt;) |</p>
<p>MIN (&lt;修飾フィールド名&gt;) |</p>
<p>MAX (&lt;修飾フィールド名&gt;) |</p>
<p>COUNT (&lt;修飾名付き&gt; | &lt;エイリアス名&gt;) |</p>
<p>STDEV (&lt;修飾フィールド名&gt;) |</p>
<p>ANY (&lt;修飾フィールド名&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;計算済-exp&gt;</p></td>
<td><p>CALC (&lt;式&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾フィールド名&gt;</p></td>
<td><p>&lt;エイリアス&gt;。[&lt;エイリアス&gt;...]&lt;フィールド名&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;エイリアス&gt;</p></td>
<td><p>&lt;引用符で囲まれた名前&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;フィールド名&gt;</p></td>
<td><p>&lt;引用符で囲ま&gt;れた名前 [ &lt;[&gt;AS] エイリアス]</p></td>
</tr>
<tr class="even">
<td><p>&lt;引用符で囲まれた名前&gt;</p></td>
<td><p>&quot;&lt;表す&gt;&quot; |</p>
<p>'&lt;string&gt;' |</p>
<p>[&lt;string&gt;] |</p>
<p>&lt;拡張子&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾名&gt;</p></td>
<td><p>エイリアス [...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;拡張子&gt;</p></td>
<td><p>α [α | 桁 | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;件数&gt;</p></td>
<td><p>数字 [数字...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;新規-exp&gt;</p></td>
<td><p>新しい&lt;フィールドの種類&gt; [(&lt;数値&gt; [, &lt;number&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;フィールドの種類&gt;</p></td>
<td><p>OLE DB または ADO のデータ型</p></td>
</tr>
<tr class="even">
<td><p>&lt;表す&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;式&gt;</p></td>
<td><p>同じ行でオペランドが他の非 CALC 列の Visual Basic for Application 式</p></td>
</tr>
</tbody>
</table>

