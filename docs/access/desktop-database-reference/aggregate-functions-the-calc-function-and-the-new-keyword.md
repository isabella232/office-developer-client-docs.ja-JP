---
title: 集計関数、CALC 関数、NEW キーワード
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297194"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="710a6-102">集計関数、CALC 関数、NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="710a6-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="710a6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="710a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="710a6-104">データ シェイプ機能では、次の関数がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="710a6-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="710a6-105">演算の対象となる列を含むチャプターに付けられる名前は、"チャプター エイリアス" です。</span><span class="sxs-lookup"><span data-stu-id="710a6-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="710a6-p102">チャプター エイリアスは、完全修飾名で表すことができます。これには、対象となる列名を含むチャプターに至るまでの各チャプター列の名前を、ピリオドで区切って表記します。たとえば、親チャプター chap1 に子チャプター chap2 が含まれており、chap2 に集計列 amt が含まれている場合、完全修飾名は chap1.chap2.amt となります。</span><span class="sxs-lookup"><span data-stu-id="710a6-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="710a6-108">集計関数</span><span class="sxs-lookup"><span data-stu-id="710a6-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="710a6-109">説明</span><span class="sxs-lookup"><span data-stu-id="710a6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="710a6-110">SUM (<em>チャプターエイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-111">指定された列に含まれるすべての値の合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="710a6-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-112">AVG (<em>チャプター-エイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-113">指定された列に含まれるすべての値の平均値を計算します。</span><span class="sxs-lookup"><span data-stu-id="710a6-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-114">MAX (<em>チャプターエイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-115">指定された列内の最大値を計算します。</span><span class="sxs-lookup"><span data-stu-id="710a6-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-116">MIN (<em>チャプターエイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-117">指定された列内の最小値を計算します。</span><span class="sxs-lookup"><span data-stu-id="710a6-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-118">COUNT (<em>chapter-alias</em>[.<em>列名</em>])</span><span class="sxs-lookup"><span data-stu-id="710a6-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="710a6-p103">指定されたエイリアス内の行数をカウントします。列が指定されている場合は、その列が null でない行のみがカウント対象となります。</span><span class="sxs-lookup"><span data-stu-id="710a6-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-121">STDEV (<em>チャプターエイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-122">指定された列内の標準偏差を計算します。</span><span class="sxs-lookup"><span data-stu-id="710a6-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-123">任意 (<em>チャプター-エイリアス)</em><em>列名</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-124">指定された列の値です。</span><span class="sxs-lookup"><span data-stu-id="710a6-124">A value of the specified column.</span></span> <span data-ttu-id="710a6-125">ANY の値を予測できるのは、その列の値がチャプター内の全行について同じである場合のみです。</span><span class="sxs-lookup"><span data-stu-id="710a6-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="710a6-126"><strong>注</strong>: 列に、チャプター内のすべての行について同じ値が含まれていない場合、SHAPE コマンドは、ANY 関数の値となる値の1つを任意に返します。</span><span class="sxs-lookup"><span data-stu-id="710a6-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
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
<th><p><span data-ttu-id="710a6-127">計算済みの式</span><span class="sxs-lookup"><span data-stu-id="710a6-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="710a6-128">説明</span><span class="sxs-lookup"><span data-stu-id="710a6-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="710a6-129">CALC (<em>式</em>)</span><span class="sxs-lookup"><span data-stu-id="710a6-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="710a6-p105">任意の式を計算しますが、CALC 関数を含む <strong>Recordset</strong> の行のみが対象となります。「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」に記載されている関数を使用した任意の式を計算できます。</span><span class="sxs-lookup"><span data-stu-id="710a6-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
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
<th><p><span data-ttu-id="710a6-132">NEW キーワード</span><span class="sxs-lookup"><span data-stu-id="710a6-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="710a6-133">説明</span><span class="sxs-lookup"><span data-stu-id="710a6-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="710a6-134">新しい<em>フィールドの種類</em>[(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span><span class="sxs-lookup"><span data-stu-id="710a6-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="710a6-135">指定された型の空の列を <strong>Recordset</strong> に追加します。</span><span class="sxs-lookup"><span data-stu-id="710a6-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="710a6-136">NEW キーワードと共に渡すフィールドの型には、次のデータ型のうちいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="710a6-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="710a6-137">OLE DB のデータ型</span><span class="sxs-lookup"><span data-stu-id="710a6-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="710a6-138">該当する ADO のデータ型</span><span class="sxs-lookup"><span data-stu-id="710a6-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="710a6-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="710a6-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="710a6-140">adbstr</span><span class="sxs-lookup"><span data-stu-id="710a6-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="710a6-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="710a6-142">adboolean</span><span class="sxs-lookup"><span data-stu-id="710a6-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="710a6-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="710a6-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="710a6-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="710a6-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="710a6-146">adアン signedtinyint</span><span class="sxs-lookup"><span data-stu-id="710a6-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="710a6-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="710a6-148">adtinyint</span><span class="sxs-lookup"><span data-stu-id="710a6-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="710a6-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="710a6-150">adアン signedsmallint</span><span class="sxs-lookup"><span data-stu-id="710a6-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="710a6-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="710a6-152">adアン signedint</span><span class="sxs-lookup"><span data-stu-id="710a6-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="710a6-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="710a6-154">adbigint</span><span class="sxs-lookup"><span data-stu-id="710a6-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="710a6-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="710a6-156">adアン signedbigint</span><span class="sxs-lookup"><span data-stu-id="710a6-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="710a6-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="710a6-158">adguid</span><span class="sxs-lookup"><span data-stu-id="710a6-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="710a6-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="710a6-160">adbinary、い、adlongvarbinary</span><span class="sxs-lookup"><span data-stu-id="710a6-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="710a6-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="710a6-162">adchar、adVarChar、adlongvarchar</span><span class="sxs-lookup"><span data-stu-id="710a6-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="710a6-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="710a6-164">adwchar、adVarWChar、adlongvarwchar</span><span class="sxs-lookup"><span data-stu-id="710a6-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="710a6-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="710a6-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="710a6-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="710a6-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="710a6-168">addbdate</span><span class="sxs-lookup"><span data-stu-id="710a6-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="710a6-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="710a6-170">addbtime</span><span class="sxs-lookup"><span data-stu-id="710a6-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="710a6-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="710a6-172">addbtimestamp</span><span class="sxs-lookup"><span data-stu-id="710a6-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="710a6-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="710a6-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="710a6-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710a6-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="710a6-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="710a6-176">adfiletime</span><span class="sxs-lookup"><span data-stu-id="710a6-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710a6-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="710a6-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="710a6-178">aderror</span><span class="sxs-lookup"><span data-stu-id="710a6-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="710a6-179">新しいフィールドの型が decimal (OLE DB、DBTYPE\_decimal、または ADO, adDecimal) の場合、精度とスケールの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="710a6-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

