---
title: schemaenum (Access デスクトップデータベースリファレンス)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308864"
---
# <a name="schemaenum"></a><span data-ttu-id="612b6-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="612b6-102">SchemaEnum</span></span>

<span data-ttu-id="612b6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="612b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="612b6-104">**OpenSchema** メソッドが取得するスキーマ [Recordset](openschema-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="612b6-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="612b6-105">注釈</span><span class="sxs-lookup"><span data-stu-id="612b6-105">Remarks</span></span>

<span data-ttu-id="612b6-106">各 ADO 定数に返される関数と列については、「OLE DB Programmer's Reference」 (英語) の Appendix B のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="612b6-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="612b6-107">各トピックの名前は、次の表の [説明] セクションにかっこで囲んで一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="612b6-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="612b6-108">各 ADO MD 定数に返される関数と列については、OLE DB for OLAP に関する Chapter 23 のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="612b6-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="612b6-109">各トピックの名前は、次の表の [説明] 列に\*、かっこで囲んで、アスタリスク () 付きでマークされています。</span><span class="sxs-lookup"><span data-stu-id="612b6-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="612b6-110">OLE DB ドキュメントの中の列のデータ型は、ADO の「[DataTypeEnum](datatypeenum.md)」の説明を参考に、ADO データ型に読み換えてください。</span><span class="sxs-lookup"><span data-stu-id="612b6-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="612b6-111">たとえば、 **DBTYPE\_WSTR**の OLE DB データ型は、ADO データ型の**adwchar**と同じです。</span><span class="sxs-lookup"><span data-stu-id="612b6-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="612b6-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="612b6-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="612b6-113">ADO は**Recordset**を作成し、各行に、 **IDBInfo:: getkeywords**および**IDBInfo:: GetLiteralInfo**メソッドで返される値をそれぞれ入力します。</span><span class="sxs-lookup"><span data-stu-id="612b6-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="612b6-114">これらのメソッドの詳細については、「 *OLE DB プログラマリファレンス*」の「IDBInfo」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="612b6-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="612b6-115">定数</span><span class="sxs-lookup"><span data-stu-id="612b6-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="612b6-116">値</span><span class="sxs-lookup"><span data-stu-id="612b6-116">Value</span></span></p></th>
<th><p><span data-ttu-id="612b6-117">説明</span><span class="sxs-lookup"><span data-stu-id="612b6-117">Description</span></span></p></th>
<th><p><span data-ttu-id="612b6-118">制約列</span><span class="sxs-lookup"><span data-stu-id="612b6-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="612b6-119"><strong>adschemaasserts</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-120">.0</span><span class="sxs-lookup"><span data-stu-id="612b6-120">0</span></span></p></td>
<td><p><span data-ttu-id="612b6-121">カタログに定義され、所定のユーザーが所有するアサーションを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-122">(ASSERTIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="612b6-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-127">1-d</span><span class="sxs-lookup"><span data-stu-id="612b6-127">1</span></span></p></td>
<td><p><span data-ttu-id="612b6-128">DBMS からアクセスできるカタログに関連付けられている物理的属性を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="612b6-129">(CATALOGS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-132">pbm-2</span><span class="sxs-lookup"><span data-stu-id="612b6-132">2</span></span></p></td>
<td><p><span data-ttu-id="612b6-133">カタログに定義され、所定のユーザーがアクセスできる文字セットを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-134">(CHARACTER_SETS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="612b6-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="612b6-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-138"><strong>adschemacheckconstraints</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-139">5</span><span class="sxs-lookup"><span data-stu-id="612b6-139">5</span></span></p></td>
<td><p><span data-ttu-id="612b6-140">カタログに定義され、所定のユーザーが所有する CHECK 制約を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-141">(CHECK_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="612b6-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-146">1/3</span><span class="sxs-lookup"><span data-stu-id="612b6-146">3</span></span></p></td>
<td><p><span data-ttu-id="612b6-147">カタログに定義され、所定のユーザーがアクセスできる文字照合順序を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-148">(COLLATIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="612b6-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="612b6-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-153">スリー</span><span class="sxs-lookup"><span data-stu-id="612b6-153">13</span></span></p></td>
<td><p><span data-ttu-id="612b6-154">カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルの列に対する特権を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="612b6-155">(COLUMN_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-158">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="612b6-160">交付</span><span class="sxs-lookup"><span data-stu-id="612b6-160">GRANTOR</span></span><br />
<span data-ttu-id="612b6-161">与え</span><span class="sxs-lookup"><span data-stu-id="612b6-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-163">2/4</span><span class="sxs-lookup"><span data-stu-id="612b6-163">4</span></span></p></td>
<td><p><span data-ttu-id="612b6-164">カタログに定義され、所定のユーザーがアクセスできるテーブルの列 (ビューも含む) を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-165">(COLUMNS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-168">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-171">#</span><span class="sxs-lookup"><span data-stu-id="612b6-171">11</span></span></p></td>
<td><p><span data-ttu-id="612b6-172">カタログに定義され、そのカタログに定義されたドメインに依存し、所定のユーザーが所有する列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="612b6-173">(COLUMN_DOMAIN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="612b6-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="612b6-176">ドメイン名</span><span class="sxs-lookup"><span data-stu-id="612b6-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="612b6-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-179">シックス</span><span class="sxs-lookup"><span data-stu-id="612b6-179">6</span></span></p></td>
<td><p><span data-ttu-id="612b6-180">カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使う列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="612b6-181">(CONSTRAINT_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-184">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-187">7</span><span class="sxs-lookup"><span data-stu-id="612b6-187">7</span></span></p></td>
<td><p><span data-ttu-id="612b6-188">カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使うテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="612b6-189">(CONSTRAINT_TABLE_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-194">32</span><span class="sxs-lookup"><span data-stu-id="612b6-194">32</span></span></p></td>
<td><p><span data-ttu-id="612b6-195">スキーマ (プロバイダーがスキーマをサポートしていない場合はカタログ) 内の利用できるキューブに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="612b6-196">(CUBES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-200"><strong>adschemadbinのキーワード</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-201">31</span><span class="sxs-lookup"><span data-stu-id="612b6-201">30</span></span></p></td>
<td><p><span data-ttu-id="612b6-202">プロバイダー固有のキーワードの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="612b6-203">(IDBInfo:: getkeywords \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-204">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="612b6-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-205"><strong>adschemadbinの方法</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-206">31</span><span class="sxs-lookup"><span data-stu-id="612b6-206">31</span></span></p></td>
<td><p><span data-ttu-id="612b6-207">テキスト コマンドで使う、プロバイダー固有のリテラルの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="612b6-208">(IDBInfo:: GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-209">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="612b6-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-210"><strong>adschemadimensions</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-211">33</span><span class="sxs-lookup"><span data-stu-id="612b6-211">33</span></span></p></td>
<td><p><span data-ttu-id="612b6-212">所定のキューブの次元に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="612b6-213">次元ごとに 1 行が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="612b6-213">It has one row for each dimension.</span></span> <span data-ttu-id="612b6-214">(DIMENSIONS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-217">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="612b6-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-221">27</span><span class="sxs-lookup"><span data-stu-id="612b6-221">27</span></span></p></td>
<td><p><span data-ttu-id="612b6-222">所定のユーザーがカタログに定義した外部キー列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="612b6-223">(FOREIGN_KEYS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-230"><strong>adschemahierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-231">34</span><span class="sxs-lookup"><span data-stu-id="612b6-231">34</span></span></p></td>
<td><p><span data-ttu-id="612b6-232">次元で利用できる階層に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="612b6-233">(HIERARCHIES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-236">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="612b6-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-240"><strong>adschemaindexes</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-241">個</span><span class="sxs-lookup"><span data-stu-id="612b6-241">12</span></span></p></td>
<td><p><span data-ttu-id="612b6-242">カタログに定義され、所定のユーザーが所有するインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-243">(INDEXES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-246">INDEX_NAME</span></span><br />
<span data-ttu-id="612b6-247">種類</span><span class="sxs-lookup"><span data-stu-id="612b6-247">TYPE</span></span><br />
<span data-ttu-id="612b6-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-249"><strong>adschemakeycolumnusage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-250">~</span><span class="sxs-lookup"><span data-stu-id="612b6-250">8</span></span></p></td>
<td><p><span data-ttu-id="612b6-251">カタログに定義され、所定のユーザーがキーとして制約した列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="612b6-252">(KEY_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="612b6-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="612b6-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-258">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-261">35</span><span class="sxs-lookup"><span data-stu-id="612b6-261">35</span></span></p></td>
<td><p><span data-ttu-id="612b6-262">次元で利用できるレベルに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="612b6-263">(LEVELS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-266">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="612b6-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-271"><strong>adschemameasures</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-272">36</span><span class="sxs-lookup"><span data-stu-id="612b6-272">36</span></span></p></td>
<td><p><span data-ttu-id="612b6-273">利用できる単位に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-273">Returns information about the available measures.</span></span> <span data-ttu-id="612b6-274">(MEASURES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-277">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="612b6-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-281">38</span><span class="sxs-lookup"><span data-stu-id="612b6-281">38</span></span></p></td>
<td><p><span data-ttu-id="612b6-282">利用できるメンバーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-282">Returns information about the available members.</span></span> <span data-ttu-id="612b6-283">(MEMBERS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-286">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="612b6-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="612b6-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="612b6-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="612b6-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="612b6-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="612b6-295">Tree 演算子 (詳細については、「OLE DB For OLAP」ドキュメントを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="612b6-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-297">個</span><span class="sxs-lookup"><span data-stu-id="612b6-297">28</span></span></p></td>
<td><p><span data-ttu-id="612b6-298">所定のユーザーがカタログに定義した主キー列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="612b6-299">(PRIMARY_KEYS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-304">29</span><span class="sxs-lookup"><span data-stu-id="612b6-304">29</span></span></p></td>
<td><p><span data-ttu-id="612b6-305">プロシージャが返す行セットの列に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="612b6-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="612b6-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="612b6-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="612b6-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-312">日</span><span class="sxs-lookup"><span data-stu-id="612b6-312">26</span></span></p></td>
<td><p><span data-ttu-id="612b6-313">プロシージャのパラメーターとリターン コードに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="612b6-314">(PROCEDURE_PARAMETERS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="612b6-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="612b6-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-319"><strong>adschemaprocedures</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-320">16</span><span class="sxs-lookup"><span data-stu-id="612b6-320">16</span></span></p></td>
<td><p><span data-ttu-id="612b6-321">カタログに定義され、所定のユーザーが所有するプロシージャを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-322">(PROCEDURES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="612b6-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="612b6-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-327"><strong>adschemaproperties</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-328">37</span><span class="sxs-lookup"><span data-stu-id="612b6-328">37</span></span></p></td>
<td><p><span data-ttu-id="612b6-329">次元の各レベルで利用できるプロパティに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="612b6-330">(PROPERTIES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="612b6-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="612b6-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-333">CUBE_NAME</span></span><br />
<span data-ttu-id="612b6-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="612b6-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="612b6-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-341">-1</span><span class="sxs-lookup"><span data-stu-id="612b6-341">-1</span></span></p></td>
<td><p><span data-ttu-id="612b6-342">プロバイダーが非標準の専用のスキーマ クエリを定義する場合に使います。</span><span class="sxs-lookup"><span data-stu-id="612b6-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="612b6-343">&lt;プロバイダー固有&gt;</span><span class="sxs-lookup"><span data-stu-id="612b6-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-344"><strong>adschemaprovidertypes</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-345">×</span><span class="sxs-lookup"><span data-stu-id="612b6-345">22</span></span></p></td>
<td><p><span data-ttu-id="612b6-346">データ プロバイダーがサポートする (基本) データ型を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="612b6-347">(PROVIDER_TYPES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-348">DATA_TYPE</span></span><br />
<span data-ttu-id="612b6-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="612b6-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-350"><strong>adschema・ entialconstraints</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-351">i-9</span><span class="sxs-lookup"><span data-stu-id="612b6-351">9</span></span></p></td>
<td><p><span data-ttu-id="612b6-352">カタログに定義され、所定のユーザーが所有する参照制約を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-353">(REFERENTIAL_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="612b6-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-358">インチ</span><span class="sxs-lookup"><span data-stu-id="612b6-358">17</span></span></p></td>
<td><p><span data-ttu-id="612b6-359">所定のユーザーが所有するスキーマ (データベース オブジェクト) を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="612b6-360">(SCHEMATA 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="612b6-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="612b6-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="612b6-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-365">個</span><span class="sxs-lookup"><span data-stu-id="612b6-365">18</span></span></p></td>
<td><p><span data-ttu-id="612b6-366">カタログに定義された SQL 実装処理データがサポートする準拠レベル、オプション、および言語を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="612b6-367">(SQL_LANGUAGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-368">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="612b6-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-369"><strong>adschemastatistics</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-370">年</span><span class="sxs-lookup"><span data-stu-id="612b6-370">19</span></span></p></td>
<td><p><span data-ttu-id="612b6-371">カタログに定義され、所定のユーザーが所有する統計値を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-372">(STATISTICS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-377">個</span><span class="sxs-lookup"><span data-stu-id="612b6-377">10</span></span></p></td>
<td><p><span data-ttu-id="612b6-378">カタログに定義され、所定のユーザーが所有するテーブル制約を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="612b6-379">(TABLE_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="612b6-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="612b6-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-385">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-387"><strong>adschematableprivileges</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-388">第</span><span class="sxs-lookup"><span data-stu-id="612b6-388">14</span></span></p></td>
<td><p><span data-ttu-id="612b6-389">カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルに対する特権を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="612b6-390">(TABLE_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-393">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-394">交付</span><span class="sxs-lookup"><span data-stu-id="612b6-394">GRANTOR</span></span><br />
<span data-ttu-id="612b6-395">与え</span><span class="sxs-lookup"><span data-stu-id="612b6-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-396"><strong>adschematables ル</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-397">1280</span><span class="sxs-lookup"><span data-stu-id="612b6-397">20</span></span></p></td>
<td><p><span data-ttu-id="612b6-398">カタログに定義され、所定のユーザーがアクセスできるテーブル (ビューも含む) を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-399">(TABLES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-402">TABLE_NAME</span></span><br />
<span data-ttu-id="612b6-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-404"><strong>adschematranslran</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-405">21</span><span class="sxs-lookup"><span data-stu-id="612b6-405">21</span></span></p></td>
<td><p><span data-ttu-id="612b6-406">カタログに定義され、所定のユーザーがアクセスできる文字変換を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-407">(TRANSLATIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="612b6-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="612b6-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-412">39</span><span class="sxs-lookup"><span data-stu-id="612b6-412">39</span></span></p></td>
<td><p><span data-ttu-id="612b6-413">将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="612b6-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-414"><strong>adschemaの権限</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-415">約</span><span class="sxs-lookup"><span data-stu-id="612b6-415">15</span></span></p></td>
<td><p><span data-ttu-id="612b6-416">カタログに定義され、所定のユーザーが利用できる、または権限を持つオブジェクトに対する USAGE 特権を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="612b6-417">(USAGE_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="612b6-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="612b6-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="612b6-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="612b6-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="612b6-422">交付</span><span class="sxs-lookup"><span data-stu-id="612b6-422">GRANTOR</span></span><br />
<span data-ttu-id="612b6-423">与え</span><span class="sxs-lookup"><span data-stu-id="612b6-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-424"><strong>adschemaviewcolumnusage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-425">ソケット</span><span class="sxs-lookup"><span data-stu-id="612b6-425">24</span></span></p></td>
<td><p><span data-ttu-id="612b6-426">カタログに定義され、所定のユーザーが所有する、表示テーブルが依存する列を返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="612b6-427">(VIEW_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="612b6-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="612b6-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-431"><strong>adschemaviews</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-432">最高</span><span class="sxs-lookup"><span data-stu-id="612b6-432">23</span></span></p></td>
<td><p><span data-ttu-id="612b6-433">カタログに定義され、所定のユーザーがアクセスできるビューを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="612b6-434">(VIEWS 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="612b6-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="612b6-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-438"><strong>adschemaviewtableusage</strong></span><span class="sxs-lookup"><span data-stu-id="612b6-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="612b6-439">まで</span><span class="sxs-lookup"><span data-stu-id="612b6-439">25</span></span></p></td>
<td><p><span data-ttu-id="612b6-440">カタログに定義され、所定のユーザーが所有し、表示テーブルが依存するテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="612b6-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="612b6-441">(VIEW_TABLE_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="612b6-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="612b6-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="612b6-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="612b6-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="612b6-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="612b6-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="612b6-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="612b6-445">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="612b6-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="612b6-446">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="612b6-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="612b6-447">定数</span><span class="sxs-lookup"><span data-stu-id="612b6-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="612b6-448">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-449">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-450">AdoEnums セット</span><span class="sxs-lookup"><span data-stu-id="612b6-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-451">AdoEnums 制約</span><span class="sxs-lookup"><span data-stu-id="612b6-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-452">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-453">AdoEnums 特権</span><span class="sxs-lookup"><span data-stu-id="612b6-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-454">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-455">AdoEnums domainusage</span><span class="sxs-lookup"><span data-stu-id="612b6-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-456">AdoEnums CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="612b6-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-457">AdoEnums CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="612b6-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-458">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-459">AdoEnums DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="612b6-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-460">AdoEnums DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="612b6-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-461">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-462">AdoEnums FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="612b6-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-463">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-464">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-465">AdoEnums (keycolumnusage)</span><span class="sxs-lookup"><span data-stu-id="612b6-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-466">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-467">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-468">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-469">AdoEnums キー</span><span class="sxs-lookup"><span data-stu-id="612b6-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-470">AdoEnums PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="612b6-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-471">AdoEnums PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="612b6-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-472">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-473">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-474">AdoEnums 固有のスキーマ</span><span class="sxs-lookup"><span data-stu-id="612b6-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-475">AdoEnums の種類</span><span class="sxs-lookup"><span data-stu-id="612b6-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-476">AdoEnums REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="612b6-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-477">AdoEnums SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="612b6-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-478">AdoEnums SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="612b6-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-479">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-480">AdoEnums TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="612b6-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-481">AdoEnums 特権</span><span class="sxs-lookup"><span data-stu-id="612b6-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-482">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-483">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-484">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-485">AdoEnums 特権</span><span class="sxs-lookup"><span data-stu-id="612b6-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-486">AdoEnums columnusage</span><span class="sxs-lookup"><span data-stu-id="612b6-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612b6-487">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="612b6-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="612b6-488">AdoEnums の使用</span><span class="sxs-lookup"><span data-stu-id="612b6-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

