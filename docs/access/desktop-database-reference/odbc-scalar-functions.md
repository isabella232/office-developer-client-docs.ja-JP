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
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288512"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="d4be5-102">ODBC スカラー関数</span><span class="sxs-lookup"><span data-stu-id="d4be5-102">ODBC scalar functions</span></span>

<span data-ttu-id="d4be5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4be5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4be5-104">Microsoft access SQL では、スカラー関数に対して定義されている ODBC 構文の使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d4be5-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="d4be5-105">たとえば、クエリ`SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5`は、株の価格の変更の絶対値が5を超えたすべての行を返します。</span><span class="sxs-lookup"><span data-stu-id="d4be5-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="d4be5-p101">ODBC 定義構文を使用できるスカラー関数のサブセットがサポートされています。次の表は、使用できるスカラー関数の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="d4be5-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="d4be5-108">SQL ステートメントで関数を使用するためのエスケープ構文の完全な説明と、引数の記述方法については、ODBC のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4be5-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="d4be5-109">文字列関数</span><span class="sxs-lookup"><span data-stu-id="d4be5-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="d4be5-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="d4be5-111">長さ</span><span class="sxs-lookup"><span data-stu-id="d4be5-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="d4be5-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="d4be5-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="d4be5-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="d4be5-114">ら</span><span class="sxs-lookup"><span data-stu-id="d4be5-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="d4be5-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="d4be5-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="d4be5-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="d4be5-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="d4be5-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="d4be5-118">副</span><span class="sxs-lookup"><span data-stu-id="d4be5-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="d4be5-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="d4be5-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="d4be5-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="d4be5-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="d4be5-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="d4be5-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="d4be5-123">数値関数</span><span class="sxs-lookup"><span data-stu-id="d4be5-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-124">ABS</span><span class="sxs-lookup"><span data-stu-id="d4be5-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="d4be5-125">窓</span><span class="sxs-lookup"><span data-stu-id="d4be5-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="d4be5-126">SIN</span><span class="sxs-lookup"><span data-stu-id="d4be5-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="d4be5-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="d4be5-128">ログイン</span><span class="sxs-lookup"><span data-stu-id="d4be5-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="d4be5-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="d4be5-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-130">限度</span><span class="sxs-lookup"><span data-stu-id="d4be5-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="d4be5-131">POWER</span><span class="sxs-lookup"><span data-stu-id="d4be5-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="d4be5-132">TAN</span><span class="sxs-lookup"><span data-stu-id="d4be5-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-133">面上</span><span class="sxs-lookup"><span data-stu-id="d4be5-133">COS</span></span></p></td>
<td><p><span data-ttu-id="d4be5-134">RAND</span><span class="sxs-lookup"><span data-stu-id="d4be5-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="d4be5-135">モダン</span><span class="sxs-lookup"><span data-stu-id="d4be5-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-136">\*</span><span class="sxs-lookup"><span data-stu-id="d4be5-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="d4be5-137">付け</span><span class="sxs-lookup"><span data-stu-id="d4be5-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="d4be5-138">Time & Date 関数</span><span class="sxs-lookup"><span data-stu-id="d4be5-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-139">日付 (curdate</span><span class="sxs-lookup"><span data-stu-id="d4be5-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="d4be5-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4be5-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="d4be5-141">月末</span><span class="sxs-lookup"><span data-stu-id="d4be5-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-142">curtime</span><span class="sxs-lookup"><span data-stu-id="d4be5-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="d4be5-143">今年</span><span class="sxs-lookup"><span data-stu-id="d4be5-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="d4be5-144">回</span><span class="sxs-lookup"><span data-stu-id="d4be5-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-145">今</span><span class="sxs-lookup"><span data-stu-id="d4be5-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="d4be5-146">毎</span><span class="sxs-lookup"><span data-stu-id="d4be5-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="d4be5-147">現</span><span class="sxs-lookup"><span data-stu-id="d4be5-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4be5-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="d4be5-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="d4be5-149">部分</span><span class="sxs-lookup"><span data-stu-id="d4be5-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="d4be5-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="d4be5-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="d4be5-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="d4be5-152">補助</span><span class="sxs-lookup"><span data-stu-id="d4be5-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="d4be5-153">dayname</span><span class="sxs-lookup"><span data-stu-id="d4be5-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="d4be5-154">データ型の変換</span><span class="sxs-lookup"><span data-stu-id="d4be5-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4be5-155">変換</span><span class="sxs-lookup"><span data-stu-id="d4be5-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="d4be5-156">次のデータ型にリテラル文字列を変換することができます。SQL_FLOAT、SQL_DOUBLE、SQL_NUMERIC、SQL_INTEGER、SQL_REAL、SQL_SMALLINT、SQL_VARCHAR および SQL_DATETIME。</span><span class="sxs-lookup"><span data-stu-id="d4be5-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

