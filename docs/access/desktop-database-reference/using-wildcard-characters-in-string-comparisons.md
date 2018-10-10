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
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="5dcc6-102">ワイルドカードによる文字列の比較</span><span class="sxs-lookup"><span data-stu-id="5dcc6-102">Using Wildcard Characters in String Comparisons</span></span>


<span data-ttu-id="5dcc6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dcc6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5dcc6-p101">パターン マッチングには、文字列比較を行うためのさまざまな機能が組み込まれています。次の表は、 **Like** 演算子で使用できるワイルドカード文字と、それらに一致する文字または数字を示したものです。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dcc6-106"><em>パターン</em>に文字</span><span class="sxs-lookup"><span data-stu-id="5dcc6-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="5dcc6-107">引数 <em>expression</em> 中で一致する文字または数字</span><span class="sxs-lookup"><span data-stu-id="5dcc6-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dcc6-p102">? または _ (アンダースコア)</span><span class="sxs-lookup"><span data-stu-id="5dcc6-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="5dcc6-110">任意の 1 文字</span><span class="sxs-lookup"><span data-stu-id="5dcc6-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dcc6-111">\*%</span><span class="sxs-lookup"><span data-stu-id="5dcc6-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="5dcc6-112">0 文字以上の文字</span><span class="sxs-lookup"><span data-stu-id="5dcc6-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="5dcc6-113">任意の半角の数字 (0 ～ 9)</span><span class="sxs-lookup"><span data-stu-id="5dcc6-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dcc6-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="5dcc6-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="5dcc6-115"><em>Charlist</em>に文字の任意の 1 します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p><span data-ttu-id="5dcc6-117"><em>Charlist</em>に含まれない文字の任意の 1 します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5dcc6-118">角かっこで囲まれた文字 (*charlist*) のグループを使用することができます (\[ \])*式で*、 *charlist*内の任意の 1 文字に一致するように含めることができますほぼすべての文字の ANSI 文字セットを含む桁です。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="5dcc6-119">かっこの文字を使用することができます (\[ ) は、疑問符 (?)、シャープ記号 (\#)、または半角のアスタリスク (\*) のみの場合は、角かっこで囲んだ直接本人とを照合します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="5dcc6-120">右角かっこを使用することはできません ( \]) するが、自身に一致するようにグループ内で使用できますグループの外に個々 の文字として。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="5dcc6-121">*Charlist*は、角かっこで囲まれた文字の簡単な一覧だけでなく文字にハイフン (-) と、範囲の下限を使用して文字の範囲を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="5dcc6-122">などを使用して\[A ~ Z\] *パターン*一致*式*で対応する文字の位置には、大文字の A から Z までの範囲内のいずれかが含まれている場合にします。範囲を区切ることがなく、角かっこ内の複数の範囲を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="5dcc6-123">たとえば、 \[、-zA-Z0-9\]英数字の文字に一致します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="5dcc6-124">注意することが重要、ANSI SQL のワイルドカード (%) と (\_)、Microsoft® Jet のバージョンでのみ利用 4.X および Microsoft OLE DB プロバイダーの Jet です。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft® Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="5dcc6-125">Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="5dcc6-126">パターン マッチングに関する重要な規則としては、これ以外に次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-126">Other important rules for pattern matching include the following:</span></span>

  - <span data-ttu-id="5dcc6-127">感嘆符 (\!)*式*で見つかった*charlist*の以外の文字がある場合に一致が行われたが*charlist*の先頭にします。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="5dcc6-128">角かっこの外側に置くと、感嘆符そのものに一致します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-128">When used outside brackets, the exclamation mark matches itself.</span></span>

  - <span data-ttu-id="5dcc6-129">自体を比較するのには先頭 (感嘆符を使用する場合) または*charlist*の最後にあるハイフン (-) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="5dcc6-130">それ以外の位置に置かれた場合は、文字の範囲を示します。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

  - <span data-ttu-id="5dcc6-131">文字の範囲は、[A-Z]、[あ-ん]、[0-9] などのように昇順で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="5dcc6-132">\[A ~ Z\]は、有効なパターンが、 \[Z A\]ではありません。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

  - <span data-ttu-id="5dcc6-133">文字シーケンス\[\]は無視されます。長さ 0 の文字列と見なされます ("")。</span><span class="sxs-lookup"><span data-stu-id="5dcc6-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>
