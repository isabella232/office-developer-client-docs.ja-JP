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
ms.openlocfilehash: 4e841da9d401558311682f0abcbefde9161b71b3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025995"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="97d55-102">ODBC スカラー関数</span><span class="sxs-lookup"><span data-stu-id="97d55-102">ODBC scalar functions</span></span>

<span data-ttu-id="97d55-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="97d55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97d55-104">Microsoft Access SQL では、スカラー関数で ODBC 定義構文を使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="97d55-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="97d55-105">クエリでは、 `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` 、株式の価格の変化の絶対値が 5 より大きい場合、すべての行を返します。</span><span class="sxs-lookup"><span data-stu-id="97d55-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="97d55-p101">ODBC 定義構文を使用できるスカラー関数のサブセットがサポートされています。次の表は、使用できるスカラー関数の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="97d55-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="97d55-108">SQL ステートメントで関数を使用するためのエスケープ構文の完全な説明と、引数の記述方法については、ODBC のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="97d55-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="97d55-109">文字列関数</span><span class="sxs-lookup"><span data-stu-id="97d55-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97d55-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="97d55-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="97d55-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="97d55-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="97d55-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="97d55-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="97d55-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="97d55-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="97d55-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="97d55-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="97d55-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="97d55-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="97d55-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="97d55-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="97d55-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="97d55-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="97d55-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="97d55-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="97d55-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="97d55-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="97d55-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="97d55-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="97d55-123">数値関数</span><span class="sxs-lookup"><span data-stu-id="97d55-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97d55-124">ABS</span><span class="sxs-lookup"><span data-stu-id="97d55-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="97d55-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="97d55-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="97d55-126">SIN</span><span class="sxs-lookup"><span data-stu-id="97d55-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="97d55-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="97d55-128">LOG</span><span class="sxs-lookup"><span data-stu-id="97d55-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="97d55-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="97d55-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="97d55-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="97d55-131">POWER</span><span class="sxs-lookup"><span data-stu-id="97d55-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="97d55-132">TAN</span><span class="sxs-lookup"><span data-stu-id="97d55-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-133">COS</span><span class="sxs-lookup"><span data-stu-id="97d55-133">COS</span></span></p></td>
<td><p><span data-ttu-id="97d55-134">RAND</span><span class="sxs-lookup"><span data-stu-id="97d55-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="97d55-135">MOD</span><span class="sxs-lookup"><span data-stu-id="97d55-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-136">EXP</span><span class="sxs-lookup"><span data-stu-id="97d55-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="97d55-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="97d55-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="97d55-138">時刻と日付の関数</span><span class="sxs-lookup"><span data-stu-id="97d55-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97d55-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="97d55-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="97d55-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="97d55-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="97d55-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="97d55-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="97d55-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="97d55-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="97d55-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="97d55-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="97d55-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-145">NOW</span><span class="sxs-lookup"><span data-stu-id="97d55-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="97d55-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="97d55-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="97d55-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="97d55-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97d55-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="97d55-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="97d55-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="97d55-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="97d55-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="97d55-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97d55-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="97d55-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="97d55-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="97d55-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="97d55-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="97d55-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="97d55-154">データ型の変換</span><span class="sxs-lookup"><span data-stu-id="97d55-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97d55-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="97d55-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="97d55-156">次のデータ型にリテラル文字列を変換することができます。SQL_FLOAT、SQL_DOUBLE、SQL_NUMERIC、SQL_INTEGER、SQL_REAL、SQL_SMALLINT、SQL_VARCHAR および SQL_DATETIME。</span><span class="sxs-lookup"><span data-stu-id="97d55-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

