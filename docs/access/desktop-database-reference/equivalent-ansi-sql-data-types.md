---
title: 同等の ANSI SQL のデータ型
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293512"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="5da07-102">同等の ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="5da07-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="5da07-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5da07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5da07-104">次の表は、ANSI SQL データ型、同等の Microsoft Access データベース エンジンの SQL データ型、有効な類義語を一覧表示しています。</span><span class="sxs-lookup"><span data-stu-id="5da07-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="5da07-105">また、この表には同等の Microsoft SQL Server™ のデータ型も示されています。</span><span class="sxs-lookup"><span data-stu-id="5da07-105">It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5da07-106">ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="5da07-106">ANSI SQL
data type</span></span></p></th>
<th><p><span data-ttu-id="5da07-107">Microsoft Access SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="5da07-107">Microsoft Access
SQL data type</span></span></p></th>
<th><p><span data-ttu-id="5da07-108">類義語</span><span class="sxs-lookup"><span data-stu-id="5da07-108">Synonym lookup</span></span></p></th>
<th><p><span data-ttu-id="5da07-109">Microsoft SQL Server のデータ型</span><span class="sxs-lookup"><span data-stu-id="5da07-109">Microsoft SQL
Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5da07-110">BIT、BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="5da07-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="5da07-111">BINARY (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-112">VARBINARY、BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="5da07-112">VARBINARY,
BINARY VARYING
BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="5da07-113">BINARY、VARBINARY</span><span class="sxs-lookup"><span data-stu-id="5da07-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-114">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="5da07-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-115">BIT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-116">BOOLEAN、LOGICAL、LOGICAL1、YESNO</span><span class="sxs-lookup"><span data-stu-id="5da07-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="5da07-117">BIT</span><span class="sxs-lookup"><span data-stu-id="5da07-117">Bit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-118">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="5da07-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="5da07-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="5da07-120">INTEGER1、BYTE</span><span class="sxs-lookup"><span data-stu-id="5da07-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="5da07-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="5da07-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-122">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="5da07-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-123">COUNTER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="5da07-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="5da07-125">(メモを参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-126">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="5da07-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="5da07-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="5da07-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="5da07-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="5da07-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="5da07-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-130">DATE、TIME、TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="5da07-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="5da07-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="5da07-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="5da07-132">DATE、TIME (メモを参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-132">DATE, TIME  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="5da07-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-134">非サポート</span><span class="sxs-lookup"><span data-stu-id="5da07-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="5da07-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="5da07-136">GUID</span><span class="sxs-lookup"><span data-stu-id="5da07-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="5da07-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="5da07-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5da07-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="5da07-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5da07-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="5da07-140">NUMERIC、DEC</span><span class="sxs-lookup"><span data-stu-id="5da07-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="5da07-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5da07-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-142">REAL</span><span class="sxs-lookup"><span data-stu-id="5da07-142">Real.</span></span></p></td>
<td><p><span data-ttu-id="5da07-143">REAL</span><span class="sxs-lookup"><span data-stu-id="5da07-143">Real.</span></span></p></td>
<td><p><span data-ttu-id="5da07-144">SINGLE、FLOAT4、IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="5da07-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="5da07-145">REAL</span><span class="sxs-lookup"><span data-stu-id="5da07-145">Real.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-146">DOUBLE PRECISION、FLOAT</span><span class="sxs-lookup"><span data-stu-id="5da07-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="5da07-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5da07-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="5da07-148">DOUBLE、FLOAT8、IEEEDOUBLE、NUMBER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5da07-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="5da07-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="5da07-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="5da07-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="5da07-152">SHORT、INTEGER2</span><span class="sxs-lookup"><span data-stu-id="5da07-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="5da07-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="5da07-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5da07-154">Integer</span></span></p></td>
<td><p><span data-ttu-id="5da07-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5da07-155">Integer</span></span></p></td>
<td><p><span data-ttu-id="5da07-156">LONG、INT、INTEGER4</span><span class="sxs-lookup"><span data-stu-id="5da07-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="5da07-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="5da07-157">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="5da07-158">Interval</span></span></p></td>
<td><p><span data-ttu-id="5da07-159">非サポート</span><span class="sxs-lookup"><span data-stu-id="5da07-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5da07-160">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5da07-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-161">非サポート</span><span class="sxs-lookup"><span data-stu-id="5da07-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="5da07-162">Image</span></span></p></td>
<td><p><span data-ttu-id="5da07-163">LONGBINARY、GENERAL、OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="5da07-163">LONGBINARY,  GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="5da07-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="5da07-164">Image</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da07-165">非サポート</span><span class="sxs-lookup"><span data-stu-id="5da07-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="5da07-166">TEXT (メモを参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-166">TEXT  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-167">LONGTEXT、LONGCHAR、MEMO、NOTE、NTEXT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="5da07-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da07-169">CHARACTER、CHARACTER VARYING、NATIONAL CHARACTER、NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="5da07-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="5da07-170">CHAR (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-171">TEXT(n)、ALPHANUMERIC、CHARACTER, STRING、VARCHAR、CHARACTER VARYING、NCHAR、NATIONAL CHARACTER、NATIONAL CHAR、NATIONAL CHARACTER VARYING、NATIONAL CHAR VARYING (メモを参照)</span><span class="sxs-lookup"><span data-stu-id="5da07-171">TEXT(n), ALPHANUMERIC,  CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="5da07-172">CHAR、VARCHAR、NCHAR、NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="5da07-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="5da07-p102">Microsoft Access SQL のデータ型 BIT は、ANSI SQL のデータ型 BIT とは異なります。Microsoft Access SQL のデータ型 BINARY が ANSI SQL のデータ型 BIT と同じ役割を果たします。Microsoft Access SQL のデータ型 BIT に相当する ANSI SQL のデータ型はありません。</span><span class="sxs-lookup"><span data-stu-id="5da07-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="5da07-176">データ型 TIMESTAMP を、データ型 DATETIME の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="5da07-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="5da07-p103">データ型 NUMERIC を、データ型 FLOAT または DOUBLE の別名として使用することはできません。データ型 NUMERIC を、データ型 DECIMAL の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="5da07-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="5da07-179">LONGTEXT 型フィールドでは、データは常に Unicode 表示形式で格納されます。</span><span class="sxs-lookup"><span data-stu-id="5da07-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="5da07-p104">データ型 TEXT を文字列の長さ (たとえば TEXT(25)) を指定しないで使用すると、LONGTEXT 型フィールドが作成されます。このため、[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントのデータ型と Microsoft SQL Server のデータ型の整合性を保つことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="5da07-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="5da07-182">CHAR 型フィールドでは、データは常に Unicode 表示形式で格納されます。データ型 CHAR は、ANSI SQL のデータ型 NATIONAL CHAR に相当します。</span><span class="sxs-lookup"><span data-stu-id="5da07-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="5da07-p105">たとえば TEXT(25) のように、フィールドのデータ型が、文字列の長さを指定したデータ型 TEXT である場合、そのフィールドのデータ型はデータ型 CHAR と一致します。データ型が一致することによって、文字列の長さが指定されていない TEXT データ型と Microsoft SQL Server のデータ型の間の整合性が保たれると共に、以前に作成された Microsoft Jet 用のアプリケーションで使用されているデータ型との下位互換性が保たれます。</span><span class="sxs-lookup"><span data-stu-id="5da07-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


