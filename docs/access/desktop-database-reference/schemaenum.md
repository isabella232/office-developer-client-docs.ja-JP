---
title: SchemaEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c7f9f9e52f2220a384ba73a64d96dd93fec2cd91
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871284"
---
# <a name="schemaenum"></a><span data-ttu-id="f160d-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="f160d-102">SchemaEnum</span></span>

<span data-ttu-id="f160d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f160d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f160d-104">**OpenSchema** メソッドが取得するスキーマ [Recordset](openschema-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="f160d-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="f160d-105">備考</span><span class="sxs-lookup"><span data-stu-id="f160d-105">Remarks</span></span>

<span data-ttu-id="f160d-106">機能と各 ADO 定数に返される列の詳細については、 *OLE DB プログラマ リファレンス*の「付録 B トピックを参照して。</span><span class="sxs-lookup"><span data-stu-id="f160d-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="f160d-107">各トピックの名前は、次の表の [説明] セクションでは、かっこ内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f160d-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="f160d-108">機能と各 ADO MD 定数に返される列の詳細については、 *OLE DB for OLAP*のマニュアルの第 23 章のトピックを参照しています。</span><span class="sxs-lookup"><span data-stu-id="f160d-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="f160d-109">各トピックの名前を括弧内に表示し、アスタリスクでマークされている (\*) 次の表の [説明] 列にします。</span><span class="sxs-lookup"><span data-stu-id="f160d-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="f160d-110">OLE DB ドキュメントの中の列のデータ型は、ADO の「[DataTypeEnum](datatypeenum.md)」の説明を参考に、ADO データ型に読み換えてください。</span><span class="sxs-lookup"><span data-stu-id="f160d-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="f160d-111">など、OLE DB データ型の**DBTYPE\_WSTR**は、ADO データ型**adWChar**に相当します。</span><span class="sxs-lookup"><span data-stu-id="f160d-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="f160d-112">ADO では、定数**adSchemaDBInfoKeywords**と**adSchemaDBInfoLiterals**のスキーマのような結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f160d-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="f160d-113">ADO では、**レコード セット**を作成し、それぞれ**IDBInfo::GetKeywords**と**IDBInfo::GetLiteralInfo**メソッドの戻り値を使用して各行を入力します。</span><span class="sxs-lookup"><span data-stu-id="f160d-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="f160d-114">これらのメソッドに関する追加情報については、 *OLE DB プログラマ リファレンス*」の IDBInfo セクションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="f160d-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="f160d-115">定数</span><span class="sxs-lookup"><span data-stu-id="f160d-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="f160d-116">値</span><span class="sxs-lookup"><span data-stu-id="f160d-116">Value</span></span></p></th>
<th><p><span data-ttu-id="f160d-117">説明</span><span class="sxs-lookup"><span data-stu-id="f160d-117">Description</span></span></p></th>
<th><p><span data-ttu-id="f160d-118">制約列</span><span class="sxs-lookup"><span data-stu-id="f160d-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f160d-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-120">0</span><span class="sxs-lookup"><span data-stu-id="f160d-120">0</span></span></p></td>
<td><p><span data-ttu-id="f160d-121">カタログに定義され、所定のユーザーが所有するアサーションを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-122">(ASSERTIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f160d-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-127">1</span><span class="sxs-lookup"><span data-stu-id="f160d-127">1</span></span></p></td>
<td><p><span data-ttu-id="f160d-128">DBMS からアクセスできるカタログに関連付けられている物理的属性を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="f160d-129">(CATALOGS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-132">2</span><span class="sxs-lookup"><span data-stu-id="f160d-132">2</span></span></p></td>
<td><p><span data-ttu-id="f160d-133">カタログに定義され、所定のユーザーがアクセスできる文字セットを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-134">(CHARACTER_SETS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="f160d-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="f160d-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-139">5</span><span class="sxs-lookup"><span data-stu-id="f160d-139">5</span></span></p></td>
<td><p><span data-ttu-id="f160d-140">カタログに定義され、所定のユーザーが所有する CHECK 制約を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-141">(CHECK_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f160d-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-146">3</span><span class="sxs-lookup"><span data-stu-id="f160d-146">3</span></span></p></td>
<td><p><span data-ttu-id="f160d-147">カタログに定義され、所定のユーザーがアクセスできる文字照合順序を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-148">(COLLATIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="f160d-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="f160d-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-153">13</span><span class="sxs-lookup"><span data-stu-id="f160d-153">13</span></span></p></td>
<td><p><span data-ttu-id="f160d-154">カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルの列に対する特権を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f160d-155">(COLUMN_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-158">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="f160d-160">権限の許可者</span><span class="sxs-lookup"><span data-stu-id="f160d-160">GRANTOR</span></span><br />
<span data-ttu-id="f160d-161">被設定者</span><span class="sxs-lookup"><span data-stu-id="f160d-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-163">4</span><span class="sxs-lookup"><span data-stu-id="f160d-163">4</span></span></p></td>
<td><p><span data-ttu-id="f160d-164">カタログに定義され、所定のユーザーがアクセスできるテーブルの列 (ビューも含む) を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-165">(COLUMNS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-168">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-171">11</span><span class="sxs-lookup"><span data-stu-id="f160d-171">11</span></span></p></td>
<td><p><span data-ttu-id="f160d-172">カタログに定義され、そのカタログに定義されたドメインに依存し、所定のユーザーが所有する列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f160d-173">(COLUMN_DOMAIN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="f160d-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="f160d-176">ドメイン名</span><span class="sxs-lookup"><span data-stu-id="f160d-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="f160d-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-179">6</span><span class="sxs-lookup"><span data-stu-id="f160d-179">6</span></span></p></td>
<td><p><span data-ttu-id="f160d-180">カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使う列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f160d-181">(CONSTRAINT_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-184">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-187">7</span><span class="sxs-lookup"><span data-stu-id="f160d-187">7</span></span></p></td>
<td><p><span data-ttu-id="f160d-188">カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使うテーブルを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="f160d-189">(CONSTRAINT_TABLE_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-194">32</span><span class="sxs-lookup"><span data-stu-id="f160d-194">32</span></span></p></td>
<td><p><span data-ttu-id="f160d-195">スキーマ (プロバイダーがスキーマをサポートしていない場合はカタログ) 内の利用できるキューブに関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="f160d-196">(CUBES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-201">30</span><span class="sxs-lookup"><span data-stu-id="f160d-201">30</span></span></p></td>
<td><p><span data-ttu-id="f160d-202">プロバイダー固有のキーワードの一覧を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="f160d-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-204">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="f160d-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-206">31</span><span class="sxs-lookup"><span data-stu-id="f160d-206">31</span></span></p></td>
<td><p><span data-ttu-id="f160d-207">テキスト コマンドで使う、プロバイダー固有のリテラルの一覧を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="f160d-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-209">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="f160d-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-211">33</span><span class="sxs-lookup"><span data-stu-id="f160d-211">33</span></span></p></td>
<td><p><span data-ttu-id="f160d-212">所定のキューブの分析コードに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="f160d-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="f160d-213">各ディメンションに対して 1 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="f160d-213">It has one row for each dimension.</span></span> <span data-ttu-id="f160d-214">(DIMENSIONS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-217">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="f160d-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-221">27</span><span class="sxs-lookup"><span data-stu-id="f160d-221">27</span></span></p></td>
<td><p><span data-ttu-id="f160d-222">所定のユーザーがカタログに定義した外部キー列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="f160d-223">(FOREIGN_KEYS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-231">34</span><span class="sxs-lookup"><span data-stu-id="f160d-231">34</span></span></p></td>
<td><p><span data-ttu-id="f160d-232">次元で利用できる階層に関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="f160d-233">(HIERARCHIES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-236">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="f160d-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-241">12</span><span class="sxs-lookup"><span data-stu-id="f160d-241">12</span></span></p></td>
<td><p><span data-ttu-id="f160d-242">カタログに定義され、所定のユーザーが所有するインデックスを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-243">(INDEXES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-246">INDEX_NAME を指定</span><span class="sxs-lookup"><span data-stu-id="f160d-246">INDEX_NAME</span></span><br />
<span data-ttu-id="f160d-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-247">TYPE</span></span><br />
<span data-ttu-id="f160d-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-250">8</span><span class="sxs-lookup"><span data-stu-id="f160d-250">8</span></span></p></td>
<td><p><span data-ttu-id="f160d-251">カタログに定義され、所定のユーザーがキーとして制約した列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="f160d-252">(KEY_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f160d-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="f160d-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-258">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-261">35</span><span class="sxs-lookup"><span data-stu-id="f160d-261">35</span></span></p></td>
<td><p><span data-ttu-id="f160d-262">次元で利用できるレベルに関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="f160d-263">(LEVELS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-266">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="f160d-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-272">36</span><span class="sxs-lookup"><span data-stu-id="f160d-272">36</span></span></p></td>
<td><p><span data-ttu-id="f160d-273">利用できる単位に関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-273">Returns information about the available measures.</span></span> <span data-ttu-id="f160d-274">(MEASURES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-277">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="f160d-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-281">38</span><span class="sxs-lookup"><span data-stu-id="f160d-281">38</span></span></p></td>
<td><p><span data-ttu-id="f160d-282">利用できるメンバーに関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-282">Returns information about the available members.</span></span> <span data-ttu-id="f160d-283">(MEMBERS 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-286">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="f160d-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="f160d-291">順序付けが MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="f160d-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="f160d-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="f160d-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="f160d-295">ツリー演算子 (詳細については、OLE DB for OLAP のマニュアルを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f160d-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-297">28</span><span class="sxs-lookup"><span data-stu-id="f160d-297">28</span></span></p></td>
<td><p><span data-ttu-id="f160d-298">所定のユーザーがカタログに定義した主キー列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="f160d-299">(PRIMARY_KEYS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-304">29</span><span class="sxs-lookup"><span data-stu-id="f160d-304">29</span></span></p></td>
<td><p><span data-ttu-id="f160d-305">プロシージャが返す行セットの列に関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="f160d-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="f160d-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f160d-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f160d-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-312">26</span><span class="sxs-lookup"><span data-stu-id="f160d-312">26</span></span></p></td>
<td><p><span data-ttu-id="f160d-313">プロシージャのパラメーターとリターン コードに関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="f160d-314">(PROCEDURE_PARAMETERS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f160d-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f160d-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-320">16</span><span class="sxs-lookup"><span data-stu-id="f160d-320">16</span></span></p></td>
<td><p><span data-ttu-id="f160d-321">カタログに定義され、所定のユーザーが所有するプロシージャを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-322">(PROCEDURES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="f160d-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="f160d-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-328">37</span><span class="sxs-lookup"><span data-stu-id="f160d-328">37</span></span></p></td>
<td><p><span data-ttu-id="f160d-329">次元の各レベルで利用できるプロパティに関する情報を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="f160d-330">(PROPERTIES 行セット \*)</span><span class="sxs-lookup"><span data-stu-id="f160d-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="f160d-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-333">CUBE_NAME</span></span><br />
<span data-ttu-id="f160d-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="f160d-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="f160d-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-341">-1</span><span class="sxs-lookup"><span data-stu-id="f160d-341">-1</span></span></p></td>
<td><p><span data-ttu-id="f160d-342">プロバイダーが非標準の専用のスキーマ クエリを定義する場合に使います。</span><span class="sxs-lookup"><span data-stu-id="f160d-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="f160d-343">&lt;プロバイダーの特定&gt;</span><span class="sxs-lookup"><span data-stu-id="f160d-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-345">22</span><span class="sxs-lookup"><span data-stu-id="f160d-345">22</span></span></p></td>
<td><p><span data-ttu-id="f160d-346">データ プロバイダーがサポートする (基本) データ型を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="f160d-347">(PROVIDER_TYPES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-348">DATA_TYPE</span></span><br />
<span data-ttu-id="f160d-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="f160d-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-351">9</span><span class="sxs-lookup"><span data-stu-id="f160d-351">9</span></span></p></td>
<td><p><span data-ttu-id="f160d-352">カタログに定義され、所定のユーザーが所有する参照制約を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-353">(REFERENTIAL_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f160d-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-358">17</span><span class="sxs-lookup"><span data-stu-id="f160d-358">17</span></span></p></td>
<td><p><span data-ttu-id="f160d-359">所定のユーザーが所有するスキーマ (データベース オブジェクト) を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="f160d-360">(SCHEMATA 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="f160d-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="f160d-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="f160d-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-365">18</span><span class="sxs-lookup"><span data-stu-id="f160d-365">18</span></span></p></td>
<td><p><span data-ttu-id="f160d-366">カタログに定義された SQL 実装処理データがサポートする準拠レベル、オプション、および言語を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="f160d-367">(SQL_LANGUAGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-368">&lt;なし&gt;</span><span class="sxs-lookup"><span data-stu-id="f160d-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-370">19</span><span class="sxs-lookup"><span data-stu-id="f160d-370">19</span></span></p></td>
<td><p><span data-ttu-id="f160d-371">カタログに定義され、所定のユーザーが所有する統計値を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-372">(STATISTICS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-377">10</span><span class="sxs-lookup"><span data-stu-id="f160d-377">10</span></span></p></td>
<td><p><span data-ttu-id="f160d-378">カタログに定義され、所定のユーザーが所有するテーブル制約を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="f160d-379">(TABLE_CONSTRAINTS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="f160d-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="f160d-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-385">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-388">14</span><span class="sxs-lookup"><span data-stu-id="f160d-388">14</span></span></p></td>
<td><p><span data-ttu-id="f160d-389">カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルに対する特権を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f160d-390">(TABLE_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-393">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-394">権限の許可者</span><span class="sxs-lookup"><span data-stu-id="f160d-394">GRANTOR</span></span><br />
<span data-ttu-id="f160d-395">被設定者</span><span class="sxs-lookup"><span data-stu-id="f160d-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-397">20</span><span class="sxs-lookup"><span data-stu-id="f160d-397">20</span></span></p></td>
<td><p><span data-ttu-id="f160d-398">カタログに定義され、所定のユーザーがアクセスできるテーブル (ビューも含む) を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-399">(TABLES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-402">TABLE_NAME</span></span><br />
<span data-ttu-id="f160d-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-405">21</span><span class="sxs-lookup"><span data-stu-id="f160d-405">21</span></span></p></td>
<td><p><span data-ttu-id="f160d-406">カタログに定義され、所定のユーザーがアクセスできる文字変換を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-407">(TRANSLATIONS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="f160d-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="f160d-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-412">39</span><span class="sxs-lookup"><span data-stu-id="f160d-412">39</span></span></p></td>
<td><p><span data-ttu-id="f160d-413">将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="f160d-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-415">15</span><span class="sxs-lookup"><span data-stu-id="f160d-415">15</span></span></p></td>
<td><p><span data-ttu-id="f160d-416">カタログに定義され、所定のユーザーが利用できる、または権限を持つオブジェクトに対する USAGE 特権を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="f160d-417">(USAGE_PRIVILEGES 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="f160d-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="f160d-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="f160d-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="f160d-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="f160d-422">権限の許可者</span><span class="sxs-lookup"><span data-stu-id="f160d-422">GRANTOR</span></span><br />
<span data-ttu-id="f160d-423">被設定者</span><span class="sxs-lookup"><span data-stu-id="f160d-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-425">24</span><span class="sxs-lookup"><span data-stu-id="f160d-425">24</span></span></p></td>
<td><p><span data-ttu-id="f160d-426">カタログに定義され、所定のユーザーが所有する、表示テーブルが依存する列を返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="f160d-427">(VIEW_COLUMN_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="f160d-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="f160d-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-432">23</span><span class="sxs-lookup"><span data-stu-id="f160d-432">23</span></span></p></td>
<td><p><span data-ttu-id="f160d-433">カタログに定義され、所定のユーザーがアクセスできるビューを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="f160d-434">(VIEWS 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="f160d-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="f160d-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="f160d-439">25</span><span class="sxs-lookup"><span data-stu-id="f160d-439">25</span></span></p></td>
<td><p><span data-ttu-id="f160d-440">カタログに定義され、所定のユーザーが所有し、表示テーブルが依存するテーブルを返します。
</span><span class="sxs-lookup"><span data-stu-id="f160d-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="f160d-441">(VIEW_TABLE_USAGE 行セット)</span><span class="sxs-lookup"><span data-stu-id="f160d-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="f160d-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f160d-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="f160d-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f160d-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="f160d-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="f160d-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f160d-445">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="f160d-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="f160d-446">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f160d-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f160d-447">定数</span><span class="sxs-lookup"><span data-stu-id="f160d-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f160d-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="f160d-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="f160d-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="f160d-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f160d-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="f160d-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f160d-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="f160d-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="f160d-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="f160d-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="f160d-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="f160d-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="f160d-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="f160d-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="f160d-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="f160d-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="f160d-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="f160d-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="f160d-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="f160d-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f160d-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="f160d-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f160d-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="f160d-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="f160d-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f160d-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="f160d-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="f160d-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="f160d-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="f160d-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f160d-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="f160d-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="f160d-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="f160d-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="f160d-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f160d-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="f160d-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f160d-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="f160d-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

