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
# <a name="formal-shape-grammar"></a><span data-ttu-id="b3d44-102">正式な Shape 文法</span><span class="sxs-lookup"><span data-stu-id="b3d44-102">Formal shape grammar</span></span>

<span data-ttu-id="b3d44-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3d44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3d44-104">すべての Shape コマンドの作成における正式な文法を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="b3d44-105">文法的に必須の項は、山かっこ ("\<\>") で区切られたテキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="b3d44-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="b3d44-106">省略可能な用語は、角かっこ (\[ \]"") で区切ります。</span><span class="sxs-lookup"><span data-stu-id="b3d44-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="b3d44-107">パイプ記号 ("|") は、代替項目であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="b3d44-108">省略符号 ("...") は、繰り返し代替項目であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="b3d44-109">*Alpha* は、英字による文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="b3d44-110">*Digit* は、数字による文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="b3d44-111">*Unicode-digit* は、Unicode 数字による文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3d44-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="b3d44-112">その他のすべての項はリテラルです。</span><span class="sxs-lookup"><span data-stu-id="b3d44-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3d44-113">用語</span><span class="sxs-lookup"><span data-stu-id="b3d44-113">Term</span></span></p></th>
<th><p><span data-ttu-id="b3d44-114">定義</span><span class="sxs-lookup"><span data-stu-id="b3d44-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-115">&lt;shape-コマンド&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-116">shape [&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]] [&lt;shape-action&gt;]</span><span class="sxs-lookup"><span data-stu-id="b3d44-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-118">{&lt;プロバイダ-コマンド-テキスト&gt;} |</span><span class="sxs-lookup"><span data-stu-id="b3d44-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="b3d44-119">(&lt;図形-コマンド&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="b3d44-120">引用符&lt;で囲まれたテーブル名&gt; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="b3d44-121">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-122">&lt;図形-アクション&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-123">エイリアス&lt;フィールドリストを追加する&gt; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="b3d44-124">エイリアス&lt;でフィールドを計算する&gt; -リスト&lt;(フィールドリスト&gt;)</span><span class="sxs-lookup"><span data-stu-id="b3d44-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-125">&lt;エイリアスが付いたフィールドリスト&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-126">&lt;エイリアスフィールド&gt; [、 &lt;エイリアスフィールド]&gt;]</span><span class="sxs-lookup"><span data-stu-id="b3d44-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-127">&lt;エイリアスフィールド&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-128">&lt;フィールド-exp&gt; [[AS] &lt;エイリアス&gt;]</span><span class="sxs-lookup"><span data-stu-id="b3d44-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-129">&lt;フィールド exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-130">(&lt;relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-131">&lt;計算済-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="b3d44-132">&lt;集計-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="b3d44-133">&lt;新規-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-135">&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]</span><span class="sxs-lookup"><span data-stu-id="b3d44-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="b3d44-136">&lt;table-exp&gt; [[AS] &lt;エイリアス&gt;]</span><span class="sxs-lookup"><span data-stu-id="b3d44-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-137">&lt;relation-リスト&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-138">&lt;リレーションシップ-同&gt;一 [ &lt;(リレーション&gt;)]</span><span class="sxs-lookup"><span data-stu-id="b3d44-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-139">&lt;relation&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-140">&lt;フィールド名&gt;と&lt;子の参照&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-141">&lt;子参照&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-142">&lt;フィールド名&gt; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="b3d44-143">パラメーター &lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-144">&lt;パラメーター ref&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-145">&lt;件数&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-146">&lt;フィールドリスト&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-147">&lt;フィールド名&gt; [、 &lt;フィールド名]&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-148">&lt;集計-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-149">SUM (&lt;修飾フィールド名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-150">AVG (&lt;修飾フィールド名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-151">MIN (&lt;修飾フィールド名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-152">MAX (&lt;修飾フィールド名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-153">COUNT (&lt;修飾名付き&gt; | &lt;エイリアス名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-154">STDEV (&lt;修飾フィールド名&gt;) |</span><span class="sxs-lookup"><span data-stu-id="b3d44-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="b3d44-155">ANY (&lt;修飾フィールド名&gt;)</span><span class="sxs-lookup"><span data-stu-id="b3d44-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-156">&lt;計算済-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-157">CALC (&lt;式&gt;)</span><span class="sxs-lookup"><span data-stu-id="b3d44-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-158">&lt;修飾フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-159">&lt;エイリアス&gt;。[&lt;エイリアス&gt;...]&lt;フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-160">&lt;エイリアス&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-161">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-162">&lt;フィールド名&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-163">&lt;引用符で囲ま&gt;れた名前 [ &lt;[&gt;AS] エイリアス]</span><span class="sxs-lookup"><span data-stu-id="b3d44-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-164">&lt;引用符で囲まれた名前&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-165">&quot;&lt;表す&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="b3d44-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="b3d44-166">'&lt;string&gt;' |</span><span class="sxs-lookup"><span data-stu-id="b3d44-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="b3d44-167">[&lt;string&gt;] |</span><span class="sxs-lookup"><span data-stu-id="b3d44-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="b3d44-168">&lt;拡張子&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-169">&lt;修飾名&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-170">エイリアス [...]</span><span class="sxs-lookup"><span data-stu-id="b3d44-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-171">&lt;拡張子&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-172">α [α | 桁 | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="b3d44-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-173">&lt;件数&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-174">数字 [数字...]</span><span class="sxs-lookup"><span data-stu-id="b3d44-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-175">&lt;新規-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-176">新しい&lt;フィールドの種類&gt; [(&lt;数値&gt; [, &lt;number&gt;])]</span><span class="sxs-lookup"><span data-stu-id="b3d44-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-177">&lt;フィールドの種類&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-178">OLE DB または ADO のデータ型</span><span class="sxs-lookup"><span data-stu-id="b3d44-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3d44-179">&lt;表す&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="b3d44-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3d44-181">&lt;式&gt;</span><span class="sxs-lookup"><span data-stu-id="b3d44-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="b3d44-182">同じ行でオペランドが他の非 CALC 列の Visual Basic for Application 式</span><span class="sxs-lookup"><span data-stu-id="b3d44-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

