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
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="f04b3-102">ワイルドカードによる文字列の比較</span><span class="sxs-lookup"><span data-stu-id="f04b3-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="f04b3-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f04b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f04b3-p101">パターン マッチングには、文字列比較を行うためのさまざまな機能が組み込まれています。次の表は、 **Like** 演算子で使用できるワイルドカード文字と、それらに一致する文字または数字を示したものです。</span><span class="sxs-lookup"><span data-stu-id="f04b3-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f04b3-106">引数 <em>pattern</em> 中の文字</span><span class="sxs-lookup"><span data-stu-id="f04b3-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="f04b3-107">引数 <em>expression</em> 中で一致する文字または数字</span><span class="sxs-lookup"><span data-stu-id="f04b3-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f04b3-p102">? または _ (アンダースコア)</span><span class="sxs-lookup"><span data-stu-id="f04b3-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="f04b3-110">任意の 1 文字</span><span class="sxs-lookup"><span data-stu-id="f04b3-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f04b3-111">\* または %</span><span class="sxs-lookup"><span data-stu-id="f04b3-111">or (\*)</span></span></p></td>
<td><p><span data-ttu-id="f04b3-112">0 文字以上の文字</span><span class="sxs-lookup"><span data-stu-id="f04b3-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="f04b3-113">任意の半角の数字 (0 ～ 9)</span><span class="sxs-lookup"><span data-stu-id="f04b3-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f04b3-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="f04b3-114">[<em>!charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="f04b3-115">引数 <em>charlist</em> に含まれる任意の全角または半角の 1 文字</span><span class="sxs-lookup"><span data-stu-id="f04b3-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f04b3-116">[!<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="f04b3-116">[<em>!charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="f04b3-117">引数 <em>charlist</em> に含まれない任意の全角または半角の 1 文字</span><span class="sxs-lookup"><span data-stu-id="f04b3-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f04b3-118">角かっこ (\[ \]) の中の、1 文字以上の文字のグループ (*charlist*) を使用して、任意の 1 文字に一致させることができ*expression、* および*charlist* は、ANSI 文字コードのほぼすべての文字を含み、また数字も含みます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-118">You can use a group of one or more characters ( *charlist*  ) enclosed in brackets ([ ]) to match any single character in  *expression,*  and  *charlist*  can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="f04b3-119">角かっこで囲まれている場合は、特殊文字の左角かっこ (\[ )、 疑問符 (?)、番号記号 (\#)、星印 (\*) を使用して、直接一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-119">You can use the special characters opening bracket ([ ), question mark (?), number sign (#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="f04b3-120">右角かっこ ( \]) は、グループ内で一致させるのに使用することはできませんが、グループの外で個別に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-120">You cannot use the closing bracket ( ]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="f04b3-121">角かっこ内の文字の一覧に加えて、*charlist* は、ハイフン (-) を使用して文字の範囲を指定し、その範囲を上下の境界で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="f04b3-122">たとえば、*pattern*結果が一致した \[A-Z\] を使用して、 *expression* の対応する文字位置が、A ～ Z の範囲で大文字を含んでいる場合は、 範囲を区切ることなく角かっこ内の複数の範囲を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-122">In addition to a simple list of characters enclosed in brackets,  charlist  can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range. For example, using [A-Z] in  pattern  results in a match if the corresponding character position in  expression  contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges. For example, [a-zA-Z0-9] matches any alphanumeric character.</span></span> <span data-ttu-id="f04b3-123">たとえば、\[a-zA-Z0-9\] はすべての英数字の検索に一致します。</span><span class="sxs-lookup"><span data-stu-id="f04b3-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="f04b3-124">ANSI SQL ワイルドカード (%) と (\_) は、Microsoft Jet version 4.X および Microsoft OLE DB Provider for Jet でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-124">It is important to note that the ANSI SQL wildcards (%) and (_) are only available with Microsoft® Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="f04b3-125">Microsoft Access や DAO を介して使用する場合は、リテラルとして取り扱われます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="f04b3-126">パターン マッチングに関する重要な規則は、他に次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="f04b3-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="f04b3-127">*charlist* の先頭に感嘆符 (\!) を置くと、*expression* の *charlist* 内の文字以外での一致を意味します。</span><span class="sxs-lookup"><span data-stu-id="f04b3-127">An exclamation mark (!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="f04b3-128">角かっこの外側に置くと、感嘆符そのものに一致します。</span><span class="sxs-lookup"><span data-stu-id="f04b3-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="f04b3-p107">ハイフン (-) は、引数 *charlist* の先頭 (感嘆符を指定している場合にはその直後) または末尾に記述すると、ハイフンそのものに一致します。それ以外の位置に置かれた場合は、文字の範囲を示します。</span><span class="sxs-lookup"><span data-stu-id="f04b3-p107">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself. In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="f04b3-131">文字の範囲を指定すると、文字が昇順 (A-z または 0-100) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="f04b3-132">\[A-Z\] は有効なパターンですが、\[Z-A\] は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="f04b3-132">[A-Z] is a valid pattern, but [Z-A] is not.</span></span>

- <span data-ttu-id="f04b3-133">文字の並び \[ \] は、空文字列 ("") と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f04b3-133">The character sequence [ ] is ignored; it is considered to be a zero-length string ("").</span></span>

