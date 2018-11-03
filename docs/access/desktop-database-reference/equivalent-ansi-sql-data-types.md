---
title: Microsoft Access データベース エンジン SQL と ANSI SQL のデータ型
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed13aab8d1f6851dd05ea2d79877e34c14665a3f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937163"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="cb381-102">Microsoft Access データベース エンジン SQL と ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="cb381-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="cb381-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cb381-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb381-104">次の表は、ANSI SQL でサポートされているデータ型、およびそれらと一致する Microsoft Access データベース エンジン SQL でサポートされているデータ型とその別名を示したものです。</span><span class="sxs-lookup"><span data-stu-id="cb381-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="cb381-105">同等の Microsoft SQL Server™ データ型を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb381-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb381-106">ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="cb381-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="cb381-107">Microsoft Access SQL データ型</span><span class="sxs-lookup"><span data-stu-id="cb381-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="cb381-108">
別名</span><span class="sxs-lookup"><span data-stu-id="cb381-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="cb381-109">Microsoft SQL Server データ型</span><span class="sxs-lookup"><span data-stu-id="cb381-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb381-110">BIT、BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="cb381-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="cb381-111">BINARY (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-112">VARBINARY 型、バイナリのビットが異なるさまざまな</span><span class="sxs-lookup"><span data-stu-id="cb381-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="cb381-113">BINARY、VARBINARY</span><span class="sxs-lookup"><span data-stu-id="cb381-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-114">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-115">BIT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-116">BOOLEAN、LOGICAL、LOGICAL1、YESNO</span><span class="sxs-lookup"><span data-stu-id="cb381-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="cb381-117">BIT</span><span class="sxs-lookup"><span data-stu-id="cb381-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-118">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="cb381-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="cb381-120">INTEGER1、BYTE</span><span class="sxs-lookup"><span data-stu-id="cb381-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="cb381-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="cb381-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-122">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-123">COUNTER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="cb381-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="cb381-125">(次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-126">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="cb381-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="cb381-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="cb381-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="cb381-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="cb381-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-130">DATE、TIME、TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="cb381-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="cb381-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="cb381-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="cb381-132">日付、時刻 (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="cb381-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="cb381-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-134">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="cb381-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="cb381-136">GUID</span><span class="sxs-lookup"><span data-stu-id="cb381-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="cb381-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="cb381-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cb381-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="cb381-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cb381-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="cb381-140">NUMERIC、DEC</span><span class="sxs-lookup"><span data-stu-id="cb381-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="cb381-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cb381-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-142">REAL</span><span class="sxs-lookup"><span data-stu-id="cb381-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="cb381-143">REAL</span><span class="sxs-lookup"><span data-stu-id="cb381-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="cb381-144">SINGLE、FLOAT4、IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="cb381-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="cb381-145">REAL</span><span class="sxs-lookup"><span data-stu-id="cb381-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-146">DOUBLE PRECISION、FLOAT</span><span class="sxs-lookup"><span data-stu-id="cb381-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="cb381-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cb381-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="cb381-148">DOUBLE、FLOAT8、IEEEDOUBLE、NUMBER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cb381-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cb381-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="cb381-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cb381-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="cb381-152">SHORT、INTEGER2</span><span class="sxs-lookup"><span data-stu-id="cb381-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="cb381-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cb381-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cb381-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="cb381-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cb381-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="cb381-156">LONG、INT、INTEGER4</span><span class="sxs-lookup"><span data-stu-id="cb381-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="cb381-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cb381-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="cb381-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="cb381-159">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="cb381-160">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-161">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="cb381-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="cb381-163">文字列では、一般に、OLE オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cb381-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="cb381-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="cb381-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb381-165">使用不可</span><span class="sxs-lookup"><span data-stu-id="cb381-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cb381-166">テキスト (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="cb381-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-167">LONGTEXT、LONGCHAR、MEMO、NOTE、NTEXT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="cb381-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb381-169">CHARACTER、CHARACTER VARYING、NATIONAL CHARACTER、NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="cb381-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="cb381-170">CHAR (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="cb381-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-171">TEXT(n)、英数字、文字、文字列、varchar 型、文字 VARYING、NCHAR、国別文字、国際文字、国別文字 VARYING、国立の CHAR VARYING (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="cb381-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cb381-172">CHAR、VARCHAR、NCHAR、NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="cb381-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="cb381-p102">Microsoft Access SQL のデータ型 BIT は、ANSI SQL のデータ型 BIT とは異なります。Microsoft Access SQL のデータ型 BINARY が ANSI SQL のデータ型 BIT と同じ役割を果たします。Microsoft Access SQL のデータ型 BIT に相当する ANSI SQL のデータ型はありません。</span><span class="sxs-lookup"><span data-stu-id="cb381-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="cb381-176">データ型 TIMESTAMP を、データ型 DATETIME の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="cb381-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="cb381-p103">データ型 NUMERIC を、データ型 FLOAT または DOUBLE の別名として使用することはできません。データ型 NUMERIC を、データ型 DECIMAL の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="cb381-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="cb381-179">LONGTEXT 型フィールドでは、データは常に Unicode 表示形式で格納されます。</span><span class="sxs-lookup"><span data-stu-id="cb381-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="cb381-p104">データ型 TEXT を文字列の長さ (たとえば TEXT(25)) を指定しないで使用すると、LONGTEXT 型フィールドが作成されます。このため、[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントのデータ型と Microsoft SQL Server のデータ型の整合性を保つことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="cb381-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="cb381-182">CHAR 型フィールドでは、データは常に Unicode 表示形式で格納されます。データ型 CHAR は、ANSI SQL のデータ型 NATIONAL CHAR に相当します。</span><span class="sxs-lookup"><span data-stu-id="cb381-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="cb381-p105">たとえば TEXT(25) のように、フィールドのデータ型が、文字列の長さを指定したデータ型 TEXT である場合、そのフィールドのデータ型はデータ型 CHAR と一致します。データ型が一致することによって、文字列の長さが指定されていない TEXT データ型と Microsoft SQL Server のデータ型の間の整合性が保たれると共に、以前に作成された Microsoft Jet 用のアプリケーションで使用されているデータ型との下位互換性が保たれます。</span><span class="sxs-lookup"><span data-stu-id="cb381-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


