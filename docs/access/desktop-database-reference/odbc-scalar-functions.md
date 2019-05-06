---
title: ODBC スカラー関数
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288512"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="43e17-102">ODBC スカラー関数</span><span class="sxs-lookup"><span data-stu-id="43e17-102">ODBC scalar functions</span></span>

<span data-ttu-id="43e17-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="43e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43e17-104">Microsoft Access SQL では、スカラー関数で ODBC 定義構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43e17-104">Microsoft® Access SQL supports the use of the ODBC defined syntax for scalar functions. For example, the query:</span></span> 

<span data-ttu-id="43e17-105">たとえば、クエリ `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` は、株式価格の変化の絶対値が 5 よりも大きいすべての列を返します。</span><span class="sxs-lookup"><span data-stu-id="43e17-105">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="43e17-p101">ODBC 定義構文を使用できるスカラー関数のサブセットがサポートされています。次の表に、使用できるスカラー関数の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="43e17-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="43e17-108">SQL ステートメントで関数を使用するためのエスケープ構文の完全な説明と、引数の記述方法については、ODBC のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43e17-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="43e17-109">文字列を処理する関数</span><span class="sxs-lookup"><span data-stu-id="43e17-109">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e17-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="43e17-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="43e17-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="43e17-111">length</span></span></p></td>
<td><p><span data-ttu-id="43e17-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="43e17-112">RTrim</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="43e17-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="43e17-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="43e17-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="43e17-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="43e17-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="43e17-116">Concat</span></span></p></td>
<td><p><span data-ttu-id="43e17-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="43e17-117">LTrim</span></span></p></td>
<td><p><span data-ttu-id="43e17-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="43e17-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="43e17-119">LCase</span></span></p></td>
<td><p><span data-ttu-id="43e17-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="43e17-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="43e17-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="43e17-121">UCase</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="43e17-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="43e17-123">数値を処理する関数</span><span class="sxs-lookup"><span data-stu-id="43e17-123">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e17-124">ABS</span><span class="sxs-lookup"><span data-stu-id="43e17-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="43e17-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="43e17-125">Floor</span></span></p></td>
<td><p><span data-ttu-id="43e17-126">SIN</span><span class="sxs-lookup"><span data-stu-id="43e17-126">sin</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="43e17-127">ATAN Function</span></span></p></td>
<td><p><span data-ttu-id="43e17-128">LOG</span><span class="sxs-lookup"><span data-stu-id="43e17-128">Log</span></span></p></td>
<td><p><span data-ttu-id="43e17-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="43e17-129">Sqrt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="43e17-130">Ceiling</span></span></p></td>
<td><p><span data-ttu-id="43e17-131">POWER</span><span class="sxs-lookup"><span data-stu-id="43e17-131">Power</span></span></p></td>
<td><p><span data-ttu-id="43e17-132">TAN</span><span class="sxs-lookup"><span data-stu-id="43e17-132">Tan</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-133">COS</span><span class="sxs-lookup"><span data-stu-id="43e17-133">cos</span></span></p></td>
<td><p><span data-ttu-id="43e17-134">RAND</span><span class="sxs-lookup"><span data-stu-id="43e17-134">Rand</span></span></p></td>
<td><p><span data-ttu-id="43e17-135">MOD</span><span class="sxs-lookup"><span data-stu-id="43e17-135">Mod</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-136">EXP</span><span class="sxs-lookup"><span data-stu-id="43e17-136">Exp</span></span></p></td>
<td><p><span data-ttu-id="43e17-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="43e17-137">Sign</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="43e17-138">時間と日付を処理する関数</span><span class="sxs-lookup"><span data-stu-id="43e17-138">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e17-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="43e17-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="43e17-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="43e17-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="43e17-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="43e17-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="43e17-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="43e17-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="43e17-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="43e17-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="43e17-144">Week</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-145">NOW</span><span class="sxs-lookup"><span data-stu-id="43e17-145">Now</span></span></p></td>
<td><p><span data-ttu-id="43e17-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="43e17-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="43e17-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="43e17-147">Quarter</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e17-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="43e17-148">dayOfMonth</span></span></p></td>
<td><p><span data-ttu-id="43e17-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="43e17-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="43e17-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="43e17-150">MonthName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e17-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="43e17-151">dayOfWeek</span></span></p></td>
<td><p><span data-ttu-id="43e17-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="43e17-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="43e17-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="43e17-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="43e17-154">データ型の変換</span><span class="sxs-lookup"><span data-stu-id="43e17-154">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e17-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="43e17-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="43e17-156">次のデータ型にリテラル文字列を変換することができます。SQL_FLOAT、SQL_DOUBLE、SQL_NUMERIC、SQL_INTEGER、SQL_REAL、SQL_SMALLINT、SQL_VARCHAR および SQL_DATETIME。</span><span class="sxs-lookup"><span data-stu-id="43e17-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

