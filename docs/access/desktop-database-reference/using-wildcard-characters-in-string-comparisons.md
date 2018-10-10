---
title: ワイルドカードによる文字列の比較
TOCTitle: Using Wildcard Characters in String Comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73946560d06d12c9bdb72b41ce0f560ad9df3e65
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477200"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>ワイルドカードによる文字列の比較


**適用されます**Access 2013 |。Office 2013

パターン マッチングには、文字列比較を行うためのさまざまな機能が組み込まれています。次の表は、 **Like** 演算子で使用できるワイルドカード文字と、それらに一致する文字または数字を示したものです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><em>パターン</em>に文字</p></th>
<th><p>引数 <em>expression</em> 中で一致する文字または数字</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? または _ (アンダースコア)</p></td>
<td><p>任意の 1 文字</p></td>
</tr>
<tr class="even">
<td><p>*%</p></td>
<td><p>0 文字以上の文字</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>任意の半角の数字 (0 ～ 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p><em>Charlist</em>に文字の任意の 1 します。</p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p><em>Charlist</em>に含まれない文字の任意の 1 します。</p></td>
</tr>
</tbody>
</table>


角かっこで囲まれた文字 (*charlist*) のグループを使用することができます (\[ \])*式で*、 *charlist*内の任意の 1 文字に一致するように含めることができますほぼすべての文字の ANSI 文字セットを含む桁です。 かっこの文字を使用することができます (\[ ) は、疑問符 (?)、シャープ記号 (\#)、または半角のアスタリスク (\*) のみの場合は、角かっこで囲んだ直接本人とを照合します。 右角かっこを使用することはできません ( \]) するが、自身に一致するようにグループ内で使用できますグループの外に個々 の文字として。

*Charlist*は、角かっこで囲まれた文字の簡単な一覧だけでなく文字にハイフン (-) と、範囲の下限を使用して文字の範囲を指定できます。 などを使用して\[A ~ Z\] *パターン*一致*式*で対応する文字の位置には、大文字の A から Z までの範囲内のいずれかが含まれている場合にします。範囲を区切ることがなく、角かっこ内の複数の範囲を含めることができます。 たとえば、 \[、-zA-Z0-9\]英数字の文字に一致します。

注意することが重要、ANSI SQL のワイルドカード (%) と (\_)、Microsoft® Jet のバージョンでのみ利用 4.X および Microsoft OLE DB プロバイダーの Jet です。 Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。

パターン マッチングに関する重要な規則としては、これ以外に次のようなものがあります。

  - 感嘆符 (\!)*式*で見つかった*charlist*の以外の文字がある場合に一致が行われたが*charlist*の先頭にします。 角かっこの外側に置くと、感嘆符そのものに一致します。

  - 自体を比較するのには先頭 (感嘆符を使用する場合) または*charlist*の最後にあるハイフン (-) を使用できます。 それ以外の位置に置かれた場合は、文字の範囲を示します。

  - 文字の範囲は、[A-Z]、[あ-ん]、[0-9] などのように昇順で指定する必要があります。 \[A ~ Z\]は、有効なパターンが、 \[Z A\]ではありません。

  - 文字シーケンス\[\]は無視されます。長さ 0 の文字列と見なされます ("")。

