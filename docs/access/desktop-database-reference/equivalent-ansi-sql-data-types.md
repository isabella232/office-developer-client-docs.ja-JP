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
ms.openlocfilehash: d1a07e3a7565e15fc5689bf73fe066a3529d3234
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946280"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="babba-102">同等の ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="babba-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="babba-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="babba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="babba-104">次の表は、ANSI SQL でサポートされているデータ型、およびそれらと一致する Microsoft Access データベース エンジン SQL でサポートされているデータ型とその別名を示したものです。</span><span class="sxs-lookup"><span data-stu-id="babba-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="babba-105">同等の Microsoft SQL Server™ データ型を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="babba-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="babba-106">ANSI SQL のデータ型</span><span class="sxs-lookup"><span data-stu-id="babba-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="babba-107">Microsoft Access SQL データ型</span><span class="sxs-lookup"><span data-stu-id="babba-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="babba-108">
別名</span><span class="sxs-lookup"><span data-stu-id="babba-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="babba-109">Microsoft SQL Server データ型</span><span class="sxs-lookup"><span data-stu-id="babba-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="babba-110">BIT、BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="babba-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="babba-111">BINARY (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-112">VARBINARY 型、バイナリのビットが異なるさまざまな</span><span class="sxs-lookup"><span data-stu-id="babba-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="babba-113">BINARY、VARBINARY</span><span class="sxs-lookup"><span data-stu-id="babba-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-114">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-115">BIT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-116">BOOLEAN、LOGICAL、LOGICAL1、YESNO</span><span class="sxs-lookup"><span data-stu-id="babba-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="babba-117">BIT</span><span class="sxs-lookup"><span data-stu-id="babba-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-118">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="babba-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="babba-120">INTEGER1、BYTE</span><span class="sxs-lookup"><span data-stu-id="babba-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="babba-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="babba-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-122">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-123">COUNTER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="babba-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="babba-125">(次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-126">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="babba-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="babba-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="babba-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="babba-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="babba-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-130">DATE、TIME、TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="babba-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="babba-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="babba-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="babba-132">日付、時刻 (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="babba-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="babba-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-134">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="babba-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="babba-136">GUID</span><span class="sxs-lookup"><span data-stu-id="babba-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="babba-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="babba-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="babba-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="babba-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="babba-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="babba-140">NUMERIC、DEC</span><span class="sxs-lookup"><span data-stu-id="babba-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="babba-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="babba-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-142">REAL</span><span class="sxs-lookup"><span data-stu-id="babba-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="babba-143">REAL</span><span class="sxs-lookup"><span data-stu-id="babba-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="babba-144">SINGLE、FLOAT4、IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="babba-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="babba-145">REAL</span><span class="sxs-lookup"><span data-stu-id="babba-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-146">DOUBLE PRECISION、FLOAT</span><span class="sxs-lookup"><span data-stu-id="babba-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="babba-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="babba-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="babba-148">DOUBLE、FLOAT8、IEEEDOUBLE、NUMBER (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="babba-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="babba-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="babba-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="babba-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="babba-152">SHORT、INTEGER2</span><span class="sxs-lookup"><span data-stu-id="babba-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="babba-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="babba-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="babba-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="babba-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="babba-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="babba-156">LONG、INT、INTEGER4</span><span class="sxs-lookup"><span data-stu-id="babba-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="babba-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="babba-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="babba-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="babba-159">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="babba-160">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-161">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="babba-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="babba-163">文字列では、一般に、OLE オブジェクト</span><span class="sxs-lookup"><span data-stu-id="babba-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="babba-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="babba-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="babba-165">使用不可</span><span class="sxs-lookup"><span data-stu-id="babba-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="babba-166">テキスト (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="babba-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-167">LONGTEXT、LONGCHAR、MEMO、NOTE、NTEXT (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="babba-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="babba-169">CHARACTER、CHARACTER VARYING、NATIONAL CHARACTER、NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="babba-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="babba-170">CHAR (次の「メモ」を参照)</span><span class="sxs-lookup"><span data-stu-id="babba-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-171">TEXT(n)、英数字、文字、文字列、varchar 型、文字 VARYING、NCHAR、国別文字、国際文字、国別文字 VARYING、国立の CHAR VARYING (メモを参照してください)</span><span class="sxs-lookup"><span data-stu-id="babba-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="babba-172">CHAR、VARCHAR、NCHAR、NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="babba-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="babba-p102">Microsoft Access SQL のデータ型 BIT は、ANSI SQL のデータ型 BIT とは異なります。Microsoft Access SQL のデータ型 BINARY が ANSI SQL のデータ型 BIT と同じ役割を果たします。Microsoft Access SQL のデータ型 BIT に相当する ANSI SQL のデータ型はありません。</span><span class="sxs-lookup"><span data-stu-id="babba-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="babba-176">データ型 TIMESTAMP を、データ型 DATETIME の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="babba-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="babba-p103">データ型 NUMERIC を、データ型 FLOAT または DOUBLE の別名として使用することはできません。データ型 NUMERIC を、データ型 DECIMAL の別名として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="babba-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="babba-179">LONGTEXT 型フィールドでは、データは常に Unicode 表示形式で格納されます。</span><span class="sxs-lookup"><span data-stu-id="babba-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="babba-p104">データ型 TEXT を文字列の長さ (たとえば TEXT(25)) を指定しないで使用すると、LONGTEXT 型フィールドが作成されます。このため、[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントのデータ型と Microsoft SQL Server のデータ型の整合性を保つことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="babba-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="babba-182">CHAR 型フィールドでは、データは常に Unicode 表示形式で格納されます。データ型 CHAR は、ANSI SQL のデータ型 NATIONAL CHAR に相当します。</span><span class="sxs-lookup"><span data-stu-id="babba-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="babba-p105">たとえば TEXT(25) のように、フィールドのデータ型が、文字列の長さを指定したデータ型 TEXT である場合、そのフィールドのデータ型はデータ型 CHAR と一致します。データ型が一致することによって、文字列の長さが指定されていない TEXT データ型と Microsoft SQL Server のデータ型の間の整合性が保たれると共に、以前に作成された Microsoft Jet 用のアプリケーションで使用されているデータ型との下位互換性が保たれます。</span><span class="sxs-lookup"><span data-stu-id="babba-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


