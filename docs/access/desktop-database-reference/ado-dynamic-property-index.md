---
title: ADO の動的プロパティ インデックス
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f385f3637f9a64ff94d571345d88fbaa088d126
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876065"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="a31e5-102">ADO の動的プロパティ インデックス</span><span class="sxs-lookup"><span data-stu-id="a31e5-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="a31e5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a31e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a31e5-p101">データ プロバイダー、サービス プロバイダー、およびサービス コンポーネントでは、開いていない **Connection** オブジェクトおよび [Recordset](connection-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションに動的プロパティを追加できます。これらのオブジェクトが開いている場合は、任意のプロバイダーでも追加プロパティを挿入できます。これらのプロパティの一部は、「 [ADO の動的プロパティ](ado-dynamic-properties.md)」の一覧に示されています。「[付録 A: プロバイダー](appendix-a-providers.md)」には、特定のプロバイダーごとに、さらに詳細な一覧が示されています。</span><span class="sxs-lookup"><span data-stu-id="a31e5-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="a31e5-p102">以下の表は、標準的な OLE DB プロバイダーの動的プロパティの ADO 名と OLE DB 名の対応表です。プロバイダーによっては、さらに多くのプロパティをサポートしている場合があります。プロバイダーに固有の動的プロパティの詳細については、各プロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a31e5-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="a31e5-p103">「OLE DB プログラマ リファレンス」では、ADO プロパティ名が "説明" 欄に示されています。標準的なプロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a31e5-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="a31e5-114">「付録 C: プロパティ表」</span><span class="sxs-lookup"><span data-stu-id="a31e5-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="a31e5-115">「Supported Properties of the Cursor Service」 (英語)</span><span class="sxs-lookup"><span data-stu-id="a31e5-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="a31e5-116">「Supported Properties of the Persistence Provider」 (英語)</span><span class="sxs-lookup"><span data-stu-id="a31e5-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="a31e5-117">「Supported OLE DB Properties of the Remoting Provider」 （英語)</span><span class="sxs-lookup"><span data-stu-id="a31e5-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="a31e5-118">解説</span><span class="sxs-lookup"><span data-stu-id="a31e5-118">Remarks</span></span>

<span data-ttu-id="a31e5-119">表中で使用されている番号の意味は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a31e5-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="a31e5-p104">(1) このプロパティは、ブール型 (Boolean) のフラグで、指定したインターフェイスを使用するかどうかを示します。等価の OLE DB プロパティが存在する場合は、その名前を示します。</span><span class="sxs-lookup"><span data-stu-id="a31e5-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="a31e5-122">(2)、ADO のブックマークを「設定」プロパティは、内部的に生成の下位互換性を維持して、DBPROP の OLE DB プロパティにマップされている\_クラス。</span><span class="sxs-lookup"><span data-stu-id="a31e5-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="a31e5-123">これは、ADO プロパティ IRowsetLocate に対応するプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="a31e5-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="a31e5-124">(3) ADO プロパティ名 "Hidden Columns" は、OLE DB プロパティ名の "説明" 欄では "Hidden Columns Count" となっています。</span><span class="sxs-lookup"><span data-stu-id="a31e5-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="a31e5-p106">(4) 階層レコードセットの場合、ADO プロパティ "Maximum Rows" はすべての子に適用されます。行が返される順序に応じて、結果セットには、各親のすべての子や一部の子が取得される場合、子が取得されない場合、孤立した子が取得される場合があります。したがって、階層レコードセットをリシェイプする場合、子の ID はそれぞれ一意である必要があります。一般的に、[Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーでは、親から継承できるプロパティと継承できないプロパティを区別できません。</span><span class="sxs-lookup"><span data-stu-id="a31e5-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="a31e5-129">(5) 対応するものがありません。</span><span class="sxs-lookup"><span data-stu-id="a31e5-129">(5) Does not apply.</span></span>

<span data-ttu-id="a31e5-130">**Connection の動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="a31e5-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a31e5-131">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a31e5-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a31e5-132">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a31e5-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="a31e5-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a31e5-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a31e5-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="a31e5-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a31e5-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a31e5-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="a31e5-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a31e5-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a31e5-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a31e5-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a31e5-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a31e5-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="a31e5-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a31e5-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a31e5-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="a31e5-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a31e5-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a31e5-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="a31e5-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a31e5-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a31e5-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="a31e5-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="a31e5-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a31e5-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="a31e5-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a31e5-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a31e5-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="a31e5-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a31e5-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a31e5-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="a31e5-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a31e5-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a31e5-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="a31e5-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a31e5-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a31e5-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="a31e5-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="a31e5-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="a31e5-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a31e5-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a31e5-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="a31e5-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a31e5-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a31e5-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="a31e5-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="a31e5-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="a31e5-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a31e5-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a31e5-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a31e5-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="a31e5-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a31e5-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a31e5-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="a31e5-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a31e5-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a31e5-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-177">Location</span><span class="sxs-lookup"><span data-stu-id="a31e5-177">Location</span></span></p></td>
<td><p><span data-ttu-id="a31e5-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="a31e5-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="a31e5-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a31e5-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a31e5-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="a31e5-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a31e5-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a31e5-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="a31e5-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a31e5-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a31e5-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="a31e5-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a31e5-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a31e5-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-187">Mode</span><span class="sxs-lookup"><span data-stu-id="a31e5-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="a31e5-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="a31e5-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="a31e5-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a31e5-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a31e5-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="a31e5-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a31e5-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a31e5-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a31e5-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="a31e5-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a31e5-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a31e5-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="a31e5-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a31e5-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a31e5-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="a31e5-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a31e5-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a31e5-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="a31e5-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="a31e5-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="a31e5-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="a31e5-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a31e5-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a31e5-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a31e5-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="a31e5-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a31e5-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a31e5-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="a31e5-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a31e5-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="a31e5-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a31e5-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a31e5-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-215">Password</span><span class="sxs-lookup"><span data-stu-id="a31e5-215">Password</span></span></p></td>
<td><p><span data-ttu-id="a31e5-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a31e5-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="a31e5-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="a31e5-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="a31e5-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="a31e5-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a31e5-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a31e5-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="a31e5-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a31e5-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a31e5-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="a31e5-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a31e5-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a31e5-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="a31e5-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a31e5-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a31e5-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="a31e5-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a31e5-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a31e5-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="a31e5-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a31e5-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a31e5-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="a31e5-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a31e5-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a31e5-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="a31e5-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a31e5-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a31e5-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="a31e5-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a31e5-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a31e5-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="a31e5-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a31e5-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a31e5-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="a31e5-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a31e5-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="a31e5-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a31e5-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a31e5-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="a31e5-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a31e5-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a31e5-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="a31e5-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a31e5-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a31e5-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-253">User ID</span><span class="sxs-lookup"><span data-stu-id="a31e5-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="a31e5-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a31e5-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-255">User Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="a31e5-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a31e5-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a31e5-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a31e5-259">**Recordset の動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="a31e5-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="a31e5-260">**Recordset** オブジェクトの **動的プロパティ** は、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="a31e5-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a31e5-261">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a31e5-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a31e5-262">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a31e5-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a31e5-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a31e5-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="a31e5-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="a31e5-266">(1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a31e5-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a31e5-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a31e5-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a31e5-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a31e5-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a31e5-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a31e5-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a31e5-274">(1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a31e5-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="a31e5-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="a31e5-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a31e5-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="a31e5-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="a31e5-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="a31e5-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="a31e5-282">(1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a31e5-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a31e5-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="a31e5-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="a31e5-286">(1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="a31e5-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="a31e5-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a31e5-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a31e5-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a31e5-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a31e5-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a31e5-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a31e5-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="a31e5-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="a31e5-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a31e5-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="a31e5-298">(1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a31e5-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a31e5-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a31e5-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a31e5-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="a31e5-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="a31e5-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a31e5-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="a31e5-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a31e5-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a31e5-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="a31e5-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="a31e5-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-311">IStream</span><span class="sxs-lookup"><span data-stu-id="a31e5-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="a31e5-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a31e5-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a31e5-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a31e5-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="a31e5-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a31e5-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a31e5-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="a31e5-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="a31e5-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="a31e5-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="a31e5-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="a31e5-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="a31e5-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="a31e5-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="a31e5-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="a31e5-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="a31e5-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="a31e5-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a31e5-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="a31e5-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="a31e5-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="a31e5-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="a31e5-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a31e5-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a31e5-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a31e5-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a31e5-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a31e5-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a31e5-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a31e5-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a31e5-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="a31e5-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="a31e5-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="a31e5-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a31e5-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="a31e5-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="a31e5-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="a31e5-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a31e5-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a31e5-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a31e5-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a31e5-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="a31e5-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="a31e5-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a31e5-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="a31e5-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="a31e5-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a31e5-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="a31e5-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="a31e5-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="a31e5-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="a31e5-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a31e5-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a31e5-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a31e5-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a31e5-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a31e5-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a31e5-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a31e5-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="a31e5-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="a31e5-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="a31e5-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="a31e5-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="a31e5-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="a31e5-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="a31e5-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="a31e5-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="a31e5-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="a31e5-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="a31e5-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a31e5-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a31e5-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a31e5-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a31e5-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a31e5-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a31e5-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="a31e5-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="a31e5-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="a31e5-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="a31e5-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="a31e5-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="a31e5-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a31e5-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a31e5-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a31e5-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a31e5-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a31e5-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a31e5-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a31e5-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a31e5-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a31e5-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a31e5-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a31e5-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a31e5-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a31e5-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a31e5-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a31e5-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a31e5-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a31e5-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a31e5-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a31e5-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a31e5-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a31e5-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a31e5-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a31e5-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a31e5-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a31e5-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a31e5-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-403">Private1</span><span class="sxs-lookup"><span data-stu-id="a31e5-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="a31e5-404">(5)</span><span class="sxs-lookup"><span data-stu-id="a31e5-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a31e5-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a31e5-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a31e5-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a31e5-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a31e5-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a31e5-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a31e5-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a31e5-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a31e5-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="a31e5-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="a31e5-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="a31e5-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="a31e5-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="a31e5-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a31e5-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a31e5-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a31e5-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a31e5-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a31e5-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a31e5-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a31e5-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a31e5-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a31e5-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a31e5-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a31e5-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a31e5-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a31e5-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a31e5-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a31e5-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a31e5-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a31e5-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a31e5-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a31e5-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a31e5-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a31e5-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a31e5-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a31e5-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="a31e5-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="a31e5-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="a31e5-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a31e5-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a31e5-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a31e5-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a31e5-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a31e5-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="a31e5-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="a31e5-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="a31e5-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="a31e5-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="a31e5-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="a31e5-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="a31e5-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="a31e5-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="a31e5-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="a31e5-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="a31e5-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="a31e5-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="a31e5-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a31e5-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a31e5-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="a31e5-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="a31e5-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="a31e5-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a31e5-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="a31e5-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="a31e5-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="a31e5-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a31e5-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a31e5-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a31e5-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a31e5-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

