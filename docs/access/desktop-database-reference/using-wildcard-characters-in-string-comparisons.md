---
title: ワイルドカードによる文字列の比較
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305937"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>ワイルドカードによる文字列の比較

**適用先**: Access 2013、Office 2013

パターン マッチングには、文字列比較を行うためのさまざまな機能が組み込まれています。次の表は、 **Like** 演算子で使用できるワイルドカード文字と、それらに一致する文字または数字を示したものです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数 <em>pattern</em> 中の文字</p></th>
<th><p>引数 <em>expression</em> 中で一致する文字または数字</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? または _ (アンダースコア)</p></td>
<td><p>任意の 1 文字</p></td>
</tr>
<tr class="even">
<td><p>* または %</p></td>
<td><p>0 文字以上の文字</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>任意の半角の数字 (0 ～ 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p>引数 <em>charlist</em> に含まれる任意の全角または半角の 1 文字</p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p>引数 <em>charlist</em> に含まれない任意の全角または半角の 1 文字</p></td>
</tr>
</tbody>
</table>


角かっこ (\[ \]) の中の、1 文字以上の文字のグループ (*charlist*) を使用して、任意の 1 文字に一致させることができ*expression、* および*charlist* は、ANSI 文字コードのほぼすべての文字を含み、また数字も含みます。 角かっこで囲まれている場合は、特殊文字の左角かっこ (\[ )、 疑問符 (?)、番号記号 (\#)、星印 (\*) を使用して、直接一致させることができます。 右角かっこ ( \]) は、グループ内で一致させるのに使用することはできませんが、グループの外で個別に使用することができます。

角かっこ内の文字の一覧に加えて、*charlist* は、ハイフン (-) を使用して文字の範囲を指定し、その範囲を上下の境界で区切ることができます。 たとえば、*pattern*結果が一致した \[A-Z\] を使用して、 *expression* の対応する文字位置が、A ～ Z の範囲で大文字を含んでいる場合は、 範囲を区切ることなく角かっこ内の複数の範囲を含むことができます。 たとえば、\[a-zA-Z0-9\] はすべての英数字の検索に一致します。

ANSI SQL ワイルドカード (%) と (\_) は、Microsoft Jet version 4.X および Microsoft OLE DB Provider for Jet でのみ使用できます。 Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。

パターン マッチングに関する重要な規則は、他に次のようなものがあります。

- *charlist* の先頭に感嘆符 (\!) を置くと、*expression* の *charlist* 内の文字以外での一致を意味します。 角かっこの外側に置くと、感嘆符そのものに一致します。

- ハイフン (-) は、引数 *charlist* の先頭 (感嘆符を指定している場合にはその直後) または末尾に記述すると、ハイフンそのものに一致します。それ以外の位置に置かれた場合は、文字の範囲を示します。

- 文字の範囲を指定すると、文字が昇順 (A-z または 0-100) で表示されます。 \[A-Z\] は有効なパターンですが、\[Z-A\] は有効ではありません。

- 文字の並び \[ \] は、空文字列 ("") と見なされます。

