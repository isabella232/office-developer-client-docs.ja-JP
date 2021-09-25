---
title: ワイルドカードによる文字列の比較
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f46c1cd6ea03b671cf0048b0535d418742a6a673
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572649"
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


かっこ ( ) で囲まれた 1 つ以上の文字 (*charlist*) のグループを使用して、式内の任意の 1 文字に一致し、文字リストには、数字を含む \[ \] ANSI文字セット内のほぼすべての文字を含めることができます。 特殊文字の開始かっこ ( ) 、疑問符 (?)、番号記号 ( )、アスタリスク ( ) を使用して、角かっこで囲む場合にのみ直接一致 \[ \# \* できます。 グループ内の閉じかっこ ( ) を使用して、それ自体を一致することはできませんが、個々の文字としてグループの外部 \] で使用できます。

かっこで囲まれた文字の簡単なリストに加えて *、charlist* はハイフン (-) を使用して範囲の上限と下限を区切って、文字の範囲を指定できます。 たとえば、A ~ Z をパターンで使用すると、式の対応する文字位置に A ~ Z の範囲の大文字が含まれている場合に一致 \[ \] します。  範囲を区切ることなく、かっこ内に複数の範囲を含めできます。 たとえば \[ 、a-zA-Z0-9 は \] 任意の英数字と一致します。

ANSI SQL ワイルドカード (%) と ( ) は、Microsoft Jet バージョン 4.X および Microsoft OLE DB Provider for Jet でのみ使用できます \_ 。 Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。

パターン マッチングに関する重要な規則としては、これ以外に次のようなものがあります。

- 文字リストの先頭にある感嘆符 ( ) は、文字リスト内の文字以外の文字が式で見つかった場合に一致 \! が行われたという意味 *です*。 角かっこの外側に置くと、感嘆符そのものに一致します。

- ハイフン (-) は、引数 *charlist* の先頭 (感嘆符を指定している場合にはその直後) または末尾に記述すると、ハイフンそのものに一致します。それ以外の位置に置かれた場合は、文字の範囲を示します。

- 文字の範囲は、[A-Z]、[あ-ん]、[0-9] などのように昇順で指定する必要があります。 \[A-Z \] は有効なパターンですが \[ 、Z-A \] は無効です。

- 文字シーケンスは \[ \] 無視されます。長さ 0 の文字列 ("") と見なされます。

