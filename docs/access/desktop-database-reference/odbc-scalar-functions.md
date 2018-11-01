---
title: ODBC スカラー関数
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 21e6000e8620011f5f6f0c2481bb9c03fd71bab5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887958"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="ee345-102">ODBC スカラー関数</span><span class="sxs-lookup"><span data-stu-id="ee345-102">ODBC Scalar Functions</span></span>


<span data-ttu-id="ee345-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ee345-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee345-p101">Microsoft® Access SQL では、スカラー関数で ODBC 定義構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee345-p101">Microsoft® Access SQL supports the use of the ODBC defined syntax for scalar functions. For example, the query:</span></span>

<span data-ttu-id="ee345-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span><span class="sxs-lookup"><span data-stu-id="ee345-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="ee345-107">このクエリは、株式価格の変化の絶対値が 5 よりも大きいすべての列を返します。</span><span class="sxs-lookup"><span data-stu-id="ee345-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="ee345-p102">ODBC 定義構文を使用できるスカラー関数のサブセットがサポートされています。次の表は、使用できるスカラー関数の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="ee345-p102">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="ee345-110">SQL ステートメントで関数を使用するためのエスケープ構文の完全な説明と、引数の記述方法については、ODBC のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee345-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="ee345-111">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="ee345-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee345-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="ee345-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="ee345-113">LENGTH</span><span class="sxs-lookup"><span data-stu-id="ee345-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="ee345-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="ee345-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-115">CHAR</span><span class="sxs-lookup"><span data-stu-id="ee345-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="ee345-116">LOCATE</span><span class="sxs-lookup"><span data-stu-id="ee345-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="ee345-117">SPACE</span><span class="sxs-lookup"><span data-stu-id="ee345-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-118">CONCAT</span><span class="sxs-lookup"><span data-stu-id="ee345-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="ee345-119">LTRIM</span><span class="sxs-lookup"><span data-stu-id="ee345-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="ee345-120">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="ee345-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="ee345-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="ee345-122">RIGHT</span><span class="sxs-lookup"><span data-stu-id="ee345-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="ee345-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="ee345-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-124">LEFT</span><span class="sxs-lookup"><span data-stu-id="ee345-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="ee345-125">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="ee345-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee345-126">ABS</span><span class="sxs-lookup"><span data-stu-id="ee345-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="ee345-127">FLOOR</span><span class="sxs-lookup"><span data-stu-id="ee345-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="ee345-128">SIN</span><span class="sxs-lookup"><span data-stu-id="ee345-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="ee345-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="ee345-130">LOG</span><span class="sxs-lookup"><span data-stu-id="ee345-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="ee345-131">SQRT</span><span class="sxs-lookup"><span data-stu-id="ee345-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-132">CEILING</span><span class="sxs-lookup"><span data-stu-id="ee345-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="ee345-133">POWER</span><span class="sxs-lookup"><span data-stu-id="ee345-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="ee345-134">TAN</span><span class="sxs-lookup"><span data-stu-id="ee345-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-135">COS</span><span class="sxs-lookup"><span data-stu-id="ee345-135">COS</span></span></p></td>
<td><p><span data-ttu-id="ee345-136">RAND</span><span class="sxs-lookup"><span data-stu-id="ee345-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="ee345-137">MOD</span><span class="sxs-lookup"><span data-stu-id="ee345-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-138">EXP</span><span class="sxs-lookup"><span data-stu-id="ee345-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="ee345-139">SIGN</span><span class="sxs-lookup"><span data-stu-id="ee345-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="ee345-140">時間と日付</span><span class="sxs-lookup"><span data-stu-id="ee345-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee345-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="ee345-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="ee345-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ee345-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="ee345-143">MONTH</span><span class="sxs-lookup"><span data-stu-id="ee345-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="ee345-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="ee345-145">YEAR</span><span class="sxs-lookup"><span data-stu-id="ee345-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="ee345-146">WEEK</span><span class="sxs-lookup"><span data-stu-id="ee345-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-147">NOW</span><span class="sxs-lookup"><span data-stu-id="ee345-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="ee345-148">HOUR</span><span class="sxs-lookup"><span data-stu-id="ee345-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="ee345-149">QUARTER</span><span class="sxs-lookup"><span data-stu-id="ee345-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee345-150">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="ee345-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="ee345-151">MINUTE</span><span class="sxs-lookup"><span data-stu-id="ee345-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="ee345-152">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="ee345-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee345-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="ee345-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="ee345-154">SECOND</span><span class="sxs-lookup"><span data-stu-id="ee345-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="ee345-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="ee345-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="ee345-156">データ型の変換</span><span class="sxs-lookup"><span data-stu-id="ee345-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee345-157">CONVERT</span><span class="sxs-lookup"><span data-stu-id="ee345-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="ee345-158">次のデータ型にリテラル文字列を変換することができます。SQL_FLOAT、SQL_DOUBLE、SQL_NUMERIC、SQL_INTEGER、SQL_REAL、SQL_SMALLINT、SQL_VARCHAR および SQL_DATETIME。</span><span class="sxs-lookup"><span data-stu-id="ee345-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

