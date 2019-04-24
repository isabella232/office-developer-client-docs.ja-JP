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
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305937"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>ワイルドカードによる文字列の比較

**適用先:** Access 2013、Office 2013

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
<td><p>*や</p></td>
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


角かっこ (\[ \]) で囲まれた1つまたは複数の文字 (*charlist*) のグループを使用して *、式*の任意の1文字と一致させることができます。 *charlist*には、ANSI 文字セットのほぼすべての文字を含めることができます。局番. 特殊文字の左角かっこ (\[ )、疑問符 (?)、番号記号 (\#)、およびアスタリスク (\*) を使用して、角かっこで囲まれている場合にのみ直接一致させることができます。 グループ内の右角かっこ ( \]) は、それ自体と一致させるために使用することはできませんが、グループの外側の文字として使用できます。

角かっこで囲まれた単純な文字のリストに加えて、 *charlist*で文字の範囲を指定するには、ハイフン (-) を使用して範囲の上限と下限を区切ります。 たとえば、パターンで\[a-z\]を使用する** と、*式*内の対応する文字位置に a ~ z の範囲内の大文字が含まれている場合に一致が返されます。範囲を区切ることなく、複数の範囲をかっこ内に含めることができます。 たとえば、zA \[-Z0 は、英数字に\]一致します。

ANSI SQL のワイルドカード (%) に注意することが重要です。および (\_) は、microsoft jet version 4 .x および microsoft OLE DB Provider for jet でのみ使用できます。 Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。

パターン マッチングに関する重要な規則としては、これ以外に次のようなものがあります。

- charlist の先頭に\!感嘆符 () を** 指定すると、引数*charlist*に指定した文字以外の文字が*式*に含まれている場合は、一致が行われることを意味します。 角かっこの外側に置くと、感嘆符そのものに一致します。

- ハイフン (-) は、引数 *charlist* の先頭 (感嘆符を指定している場合にはその直後) または末尾に記述すると、ハイフンそのものに一致します。それ以外の位置に置かれた場合は、文字の範囲を示します。

- 文字の範囲は、[A-Z]、[あ-ん]、[0-9] などのように昇順で指定する必要があります。 \[a ~ z\]は有効なパターンですが\[、z-\] a は有効ではありません。

- 文字シーケンス\[ \]は無視されます。長さ0の文字列 ("") と見なされます。

