---
title: 正式な Shape 文法
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f226faa303a4ff99a062449548478d32fc60612
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877150"
---
# <a name="formal-shape-grammar"></a>正式な Shape 文法


**適用されます**Access 2013、Office 2013。

すべての Shape コマンドの作成における正式な文法を以下に示します。

  - 文法的に必須の項は、山かっこ ("\<\>") で区切られたテキスト文字列です。

  - オプションの項は、角かっこで区切られます ("\[ \]")。

  - パイプ記号 ("|") は、代替項目であることを示します。

  - 省略符号 ("...") は、繰り返し代替項目であることを示します。

  - *アルファ*は、アルファベット文字の文字列を示します。

  - *数字*は、数値の文字列を示します。

  - *Unicode 文字*は、unicode 数字の文字列を示します。

その他のすべての項はリテラルです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>項</p></th>
<th><p>定義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;shape コマンド&gt;</p></td>
<td><p>図形 [&lt;テーブル exp&gt; [AS]&lt;別名&gt;] [&lt;] 図形の操作&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;テーブル exp&gt;</p></td>
<td><p>{&lt;プロバイダー]&gt;} |<br />
(&lt;図形コマンド&gt;)。<br />
テーブル&lt;引用符で囲まれた名前&gt; |<br />
&lt;引用符で囲まれた名前&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;図形操作&gt;</p></td>
<td><p>追加&lt;エイリアス]&gt; |</p>
<p>計算&lt;エイリアス]&gt; [BY&lt;フィールド リスト&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;エイリアスのフィールドの一覧&gt;</p></td>
<td><p>&lt;エイリアス フィールド&gt;[、&lt;の別名フィールド.&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;エイリアス フィールド&gt;</p></td>
<td><p>&lt;フィールド exp&gt; [AS]&lt;別名&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;フィールド exp&gt;</p></td>
<td><p>(&lt;関係 exp&gt;)。</p>
<p>&lt;計算 exp&gt; |</p>
<p>&lt;集計 exp&gt; |</p>
<p>&lt;新しい exp 関数&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;テーブル exp&gt; [AS]&lt;別名&gt;]</p>
<p>&lt;テーブル exp&gt; [AS]&lt;別名&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;関係の条件の一覧&gt;</p></td>
<td><p>&lt;関係条件&gt;[、&lt;関係条件&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;関係条件&gt;</p></td>
<td><p>&lt;フィールド名&gt;TO&lt;子参照&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;子参照&gt;</p></td>
<td><p>&lt;フィールド名&gt; |</p>
<p>パラメーター&lt;パラメーター渡し&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;パラメーター渡し&gt;</p></td>
<td><p>&lt;番号&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;フィールド リスト&gt;</p></td>
<td><p>&lt;フィールド名&gt;[、&lt;フィールド名&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;集計 exp&gt;</p></td>
<td><p>合計 (&lt;修飾フィールド名&gt;)。</p>
<p>AVG (&lt;修飾フィールド名&gt;)。</p>
<p>MIN (&lt;修飾フィールド名&gt;)。</p>
<p>MAX (&lt;修飾フィールド名&gt;)。</p>
<p>カウント (&lt;修飾エイリアス&gt; | &lt;修飾名&gt;)。</p>
<p>STDEV (&lt;修飾フィールド名&gt;)。</p>
<p>任意 (&lt;修飾フィールド名&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;計算 exp&gt;</p></td>
<td><p>再計算実行 (&lt;式&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾フィールド名&gt;</p></td>
<td><p>&lt;エイリアス&gt;。[&lt;別名&gt;...]&lt;フィールド名&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;エイリアス&gt;</p></td>
<td><p>&lt;引用符で囲まれた名前&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;フィールド名&gt;</p></td>
<td><p>&lt;引用符で囲まれた名前&gt;[AS]&lt;別名&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;引用符で囲まれた名前&gt;</p></td>
<td><p>&quot;&lt;文字列&gt;&quot; |</p>
<p>'&lt;文字列&gt;' |</p>
<p>[&lt;文字列&gt;] |</p>
<p>&lt;名&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;修飾された名前&gt;</p></td>
<td><p>エイリアス [.alias.]</p></td>
</tr>
<tr class="even">
<td><p>&lt;名&gt;</p></td>
<td><p>alpha [アルファ | 数字 | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;番号&gt;</p></td>
<td><p>数字 [桁]</p></td>
</tr>
<tr class="even">
<td><p>&lt;新しい exp 関数&gt;</p></td>
<td><p>新しい&lt;フィールドの型&gt;[(&lt;数&gt;[、&lt;数&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;フィールドの型&gt;</p></td>
<td><p>OLE DB または ADO のデータ型</p></td>
</tr>
<tr class="even">
<td><p>&lt;文字列&gt;</p></td>
<td><p>unicode 文字 [unicode 文字です..]。</p></td>
</tr>
<tr class="odd">
<td><p>&lt;式&gt;</p></td>
<td><p>同じ行でオペランドが他の非 CALC 列の Visual Basic for Application 式</p></td>
</tr>
</tbody>
</table>

