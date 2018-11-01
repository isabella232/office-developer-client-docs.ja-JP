---
title: 集計関数、CALC 関数、および NEW キーワード
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ee1bff23e1bcf04c1a9fd4cfc807edbd541148
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882379"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="7bfff-102">集計関数、CALC 関数、および NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="7bfff-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="7bfff-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7bfff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bfff-104">データ シェイプと、次の関数がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7bfff-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="7bfff-105">*チャプター エイリアス*は、操作することで、列を含むチャプターに割り当てられた名前です。</span><span class="sxs-lookup"><span data-stu-id="7bfff-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="7bfff-106">チャプター エイリアスは、完全修飾名、*列名、* すべてピリオドで区切られたを含むチャプターにつながるので構成されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7bfff-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="7bfff-107">など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。</span><span class="sxs-lookup"><span data-stu-id="7bfff-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bfff-108">集計関数</span><span class="sxs-lookup"><span data-stu-id="7bfff-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="7bfff-109">説明</span><span class="sxs-lookup"><span data-stu-id="7bfff-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-110">合計 (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-111">指定された列に含まれるすべての値の合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-112">AVG (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-113">指定された列に含まれるすべての値の平均値を計算します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-114">MAX (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-115">指定された列内の最大値を計算します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-116">MIN (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-117">指定された列内の最小値を計算します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-118">カウント (<em>チャプター エイリアス</em>[.<em>列名</em>])</span><span class="sxs-lookup"><span data-stu-id="7bfff-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="7bfff-p103">指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</span><span class="sxs-lookup"><span data-stu-id="7bfff-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-121">STDEV (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-122">指定された列内の標準偏差を計算します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-123">任意 (<em>チャプター エイリアス</em>です<em>。列名</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-p104">指定された列の値です。ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。
</span><span class="sxs-lookup"><span data-stu-id="7bfff-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <span data-ttu-id="7bfff-126">列の値がチャプター内の全行について同じでない場合、SHAPE コマンドは、ANY 関数の値として、複数ある値のうち任意のものを 1 つ返します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bfff-127">計算済みの式</span><span class="sxs-lookup"><span data-stu-id="7bfff-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="7bfff-128">説明</span><span class="sxs-lookup"><span data-stu-id="7bfff-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-129">計算式 (<em>式</em>)</span><span class="sxs-lookup"><span data-stu-id="7bfff-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="7bfff-p105">任意の式を計算しますが、CALC 関数を含む <strong>Recordset</strong> の行のみが対象となります。「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」に記載されている関数を使用した任意の式を計算できます。</span><span class="sxs-lookup"><span data-stu-id="7bfff-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bfff-132">NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="7bfff-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="7bfff-133">説明</span><span class="sxs-lookup"><span data-stu-id="7bfff-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-134">新しい<em>フィールドの種類</em>[(<em>幅</em> | <em>スケール</em> | <em>精度</em> | <em>エラー</em> [、<em>スケール</em> | <em>エラー</em>])]</span><span class="sxs-lookup"><span data-stu-id="7bfff-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="7bfff-135">指定された型の空の列を <strong>Recordset</strong> に追加します。</span><span class="sxs-lookup"><span data-stu-id="7bfff-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bfff-136">NEW キーワードと共に渡す*フィールドの型*には、次のデータ型のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7bfff-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bfff-137">OLE DB のデータ型</span><span class="sxs-lookup"><span data-stu-id="7bfff-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="7bfff-138">該当する ADO のデータ型</span><span class="sxs-lookup"><span data-stu-id="7bfff-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="7bfff-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="7bfff-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="7bfff-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="7bfff-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="7bfff-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="7bfff-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="7bfff-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="7bfff-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="7bfff-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="7bfff-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="7bfff-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="7bfff-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="7bfff-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="7bfff-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="7bfff-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="7bfff-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="7bfff-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="7bfff-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="7bfff-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="7bfff-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="7bfff-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="7bfff-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfff-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="7bfff-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="7bfff-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="7bfff-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="7bfff-160">adBinary、ない、adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="7bfff-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-161">が</span><span class="sxs-lookup"><span data-stu-id="7bfff-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="7bfff-162">ファミリ、それぞれ、adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="7bfff-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="7bfff-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="7bfff-164">adWChar、adVarWChar、adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="7bfff-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="7bfff-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="7bfff-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="7bfff-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="7bfff-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="7bfff-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="7bfff-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="7bfff-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="7bfff-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="7bfff-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="7bfff-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="7bfff-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="7bfff-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="7bfff-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="7bfff-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="7bfff-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bfff-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="7bfff-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="7bfff-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="7bfff-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bfff-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="7bfff-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="7bfff-178">adError</span><span class="sxs-lookup"><span data-stu-id="7bfff-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bfff-179">新しいフィールドがあるとき decimal 型 (OLE db では、DBTYPE\_10 進数、または ADO では、adDecimal)、有効桁数と小数点部桁数の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bfff-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

