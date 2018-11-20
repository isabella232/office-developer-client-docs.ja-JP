---
title: 集計関数、CALC 関数、NEW キーワード
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb3e667a23d5bfd1d3dda5b4eb8dbd60a47e36ba
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025988"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="4cd44-102">集計関数、CALC 関数、NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="4cd44-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="4cd44-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4cd44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4cd44-104">データ シェイプと、次の関数がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4cd44-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="4cd44-105">*チャプター エイリアス*は、操作することで、列を含むチャプターに割り当てられた名前です。</span><span class="sxs-lookup"><span data-stu-id="4cd44-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="4cd44-106">チャプター エイリアスは、完全修飾名、*列名、* すべてピリオドで区切られたを含むチャプターにつながるので構成されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4cd44-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="4cd44-107">など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。</span><span class="sxs-lookup"><span data-stu-id="4cd44-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cd44-108">集計関数</span><span class="sxs-lookup"><span data-stu-id="4cd44-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="4cd44-109">説明</span><span class="sxs-lookup"><span data-stu-id="4cd44-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-110">合計 (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-111">指定された列に含まれるすべての値の合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-112">AVG (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-113">指定された列に含まれるすべての値の平均値を計算します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-114">MAX (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-115">指定された列内の最大値を計算します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-116">MIN (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-117">指定された列内の最小値を計算します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-118">カウント (<em>チャプター エイリアス</em>[.<em>列名</em>])</span><span class="sxs-lookup"><span data-stu-id="4cd44-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="4cd44-p103">指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</span><span class="sxs-lookup"><span data-stu-id="4cd44-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-121">STDEV (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-122">指定された列内の標準偏差を計算します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-123">任意 (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-p104">指定された列の値です。ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。
</span><span class="sxs-lookup"><span data-stu-id="4cd44-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="4cd44-126"><strong>注</strong>: 列に、章内の行のすべてに同じ値が含まれていない場合 SHAPE コマンド任意に返す任意の関数の値を指定する値の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="4cd44-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cd44-127">計算済みの式</span><span class="sxs-lookup"><span data-stu-id="4cd44-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="4cd44-128">説明</span><span class="sxs-lookup"><span data-stu-id="4cd44-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-129">計算式 (<em>式</em>)</span><span class="sxs-lookup"><span data-stu-id="4cd44-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="4cd44-p105">任意の式を計算しますが、CALC 関数を含む <strong>Recordset</strong> の行のみが対象となります。「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」に記載されている関数を使用した任意の式を計算できます。</span><span class="sxs-lookup"><span data-stu-id="4cd44-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cd44-132">NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="4cd44-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="4cd44-133">説明</span><span class="sxs-lookup"><span data-stu-id="4cd44-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-134">新しい<em>フィールドの種類</em>[(<em>幅</em> | <em>スケール</em> | <em>精度</em> | <em>エラー</em> [、<em>スケール</em> | <em>エラー</em>])]</span><span class="sxs-lookup"><span data-stu-id="4cd44-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="4cd44-135">指定された型の空の列を <strong>Recordset</strong> に追加します。</span><span class="sxs-lookup"><span data-stu-id="4cd44-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="4cd44-136">NEW キーワードと共に渡す*フィールドの型*には、次のデータ型のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4cd44-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cd44-137">OLE DB のデータ型</span><span class="sxs-lookup"><span data-stu-id="4cd44-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="4cd44-138">該当する ADO のデータ型</span><span class="sxs-lookup"><span data-stu-id="4cd44-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="4cd44-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="4cd44-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="4cd44-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="4cd44-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="4cd44-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="4cd44-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="4cd44-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="4cd44-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="4cd44-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="4cd44-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="4cd44-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="4cd44-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="4cd44-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="4cd44-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="4cd44-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="4cd44-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="4cd44-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="4cd44-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="4cd44-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="4cd44-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="4cd44-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="4cd44-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="4cd44-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="4cd44-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="4cd44-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="4cd44-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="4cd44-160">adBinary、ない、adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="4cd44-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-161">が</span><span class="sxs-lookup"><span data-stu-id="4cd44-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="4cd44-162">ファミリ、それぞれ、adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="4cd44-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="4cd44-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="4cd44-164">adWChar、adVarWChar、adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="4cd44-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="4cd44-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="4cd44-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="4cd44-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="4cd44-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="4cd44-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="4cd44-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="4cd44-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="4cd44-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="4cd44-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="4cd44-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="4cd44-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="4cd44-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="4cd44-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="4cd44-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="4cd44-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cd44-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="4cd44-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="4cd44-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="4cd44-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cd44-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="4cd44-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="4cd44-178">adError</span><span class="sxs-lookup"><span data-stu-id="4cd44-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4cd44-179">新しいフィールドがあるとき decimal 型 (OLE db では、DBTYPE\_10 進数、または ADO では、adDecimal)、有効桁数と小数点部桁数の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cd44-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

