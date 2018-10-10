---
title: ADO の動的プロパティ インデックス
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58e9029e7c78a6cbde97973ee7fc482fb116c3f2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476575"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="f8a8c-102">ADO の動的プロパティ インデックス</span><span class="sxs-lookup"><span data-stu-id="f8a8c-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="f8a8c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8a8c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8a8c-p101">データ プロバイダー、サービス プロバイダー、およびサービス コンポーネントでは、開いていない **Connection** オブジェクトおよび [Recordset](connection-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションに動的プロパティを追加できます。これらのオブジェクトが開いている場合は、任意のプロバイダーでも追加プロパティを挿入できます。これらのプロパティの一部は、「 [ADO の動的プロパティ](ado-dynamic-properties.md)」の一覧に示されています。「[付録 A: プロバイダー](appendix-a-providers.md)」には、特定のプロバイダーごとに、さらに詳細な一覧が示されています。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="f8a8c-p102">以下の表は、標準的な OLE DB プロバイダーの動的プロパティの ADO 名と OLE DB 名の対応表です。プロバイダーによっては、さらに多くのプロパティをサポートしている場合があります。プロバイダーに固有の動的プロパティの詳細については、各プロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="f8a8c-p103">「OLE DB プログラマ リファレンス」では、ADO プロパティ名が "説明" 欄に示されています。標準的なプロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="f8a8c-114">「付録 C: プロパティ表」</span><span class="sxs-lookup"><span data-stu-id="f8a8c-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="f8a8c-115">「Supported Properties of the Cursor Service」 (英語)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="f8a8c-116">「Supported Properties of the Persistence Provider」 (英語)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="f8a8c-117">「Supported OLE DB Properties of the Remoting Provider」 （英語)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a8c-118">解説</span><span class="sxs-lookup"><span data-stu-id="f8a8c-118">Remarks</span></span>

<span data-ttu-id="f8a8c-119">表中で使用されている番号の意味は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="f8a8c-p104">(1) このプロパティは、ブール型 (Boolean) のフラグで、指定したインターフェイスを使用するかどうかを示します。等価の OLE DB プロパティが存在する場合は、その名前を示します。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="f8a8c-122">(2)、ADO のブックマークを「設定」プロパティは、内部的に生成の下位互換性を維持して、DBPROP の OLE DB プロパティにマップされている\_クラス。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="f8a8c-123">これは、ADO プロパティ IRowsetLocate に対応するプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="f8a8c-124">(3) ADO プロパティ名 "Hidden Columns" は、OLE DB プロパティ名の "説明" 欄では "Hidden Columns Count" となっています。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="f8a8c-p106">(4) 階層レコードセットの場合、ADO プロパティ "Maximum Rows" はすべての子に適用されます。行が返される順序に応じて、結果セットには、各親のすべての子や一部の子が取得される場合、子が取得されない場合、孤立した子が取得される場合があります。したがって、階層レコードセットをリシェイプする場合、子の ID はそれぞれ一意である必要があります。一般的に、[Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーでは、親から継承できるプロパティと継承できないプロパティを区別できません。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="f8a8c-129">(5) 対応するものがありません。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-129">(5) Does not apply.</span></span>

<span data-ttu-id="f8a8c-130">**Connection の動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="f8a8c-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8a8c-131">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f8a8c-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="f8a8c-132">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f8a8c-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="f8a8c-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="f8a8c-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="f8a8c-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="f8a8c-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="f8a8c-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="f8a8c-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="f8a8c-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="f8a8c-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="f8a8c-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="f8a8c-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="f8a8c-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="f8a8c-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="f8a8c-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="f8a8c-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="f8a8c-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="f8a8c-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="f8a8c-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="f8a8c-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="f8a8c-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="f8a8c-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="f8a8c-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="f8a8c-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="f8a8c-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f8a8c-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="f8a8c-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="f8a8c-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="f8a8c-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="f8a8c-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="f8a8c-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-177">Location</span><span class="sxs-lookup"><span data-stu-id="f8a8c-177">Location</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="f8a8c-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="f8a8c-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="f8a8c-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="f8a8c-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="f8a8c-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-187">Mode</span><span class="sxs-lookup"><span data-stu-id="f8a8c-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="f8a8c-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="f8a8c-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="f8a8c-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="f8a8c-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="f8a8c-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="f8a8c-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="f8a8c-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f8a8c-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="f8a8c-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="f8a8c-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="f8a8c-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="f8a8c-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="f8a8c-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="f8a8c-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="f8a8c-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-215">Password</span><span class="sxs-lookup"><span data-stu-id="f8a8c-215">Password</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="f8a8c-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="f8a8c-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="f8a8c-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="f8a8c-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="f8a8c-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f8a8c-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="f8a8c-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="f8a8c-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="f8a8c-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="f8a8c-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="f8a8c-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="f8a8c-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="f8a8c-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="f8a8c-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="f8a8c-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="f8a8c-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="f8a8c-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="f8a8c-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="f8a8c-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="f8a8c-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="f8a8c-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="f8a8c-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="f8a8c-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="f8a8c-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="f8a8c-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="f8a8c-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-253">User ID</span><span class="sxs-lookup"><span data-stu-id="f8a8c-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="f8a8c-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-255">User Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="f8a8c-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="f8a8c-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f8a8c-259">**Recordset の動的プロパティ**</span><span class="sxs-lookup"><span data-stu-id="f8a8c-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="f8a8c-260">**Recordset** オブジェクトの **動的プロパティ** は、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="f8a8c-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8a8c-261">ADO プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f8a8c-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="f8a8c-262">OLE DB プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f8a8c-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="f8a8c-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="f8a8c-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-266">(1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="f8a8c-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="f8a8c-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="f8a8c-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="f8a8c-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-274">(1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="f8a8c-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="f8a8c-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="f8a8c-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="f8a8c-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-282">(1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="f8a8c-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="f8a8c-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-286">(1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="f8a8c-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="f8a8c-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="f8a8c-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="f8a8c-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="f8a8c-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="f8a8c-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-298">(1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="f8a8c-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="f8a8c-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="f8a8c-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="f8a8c-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="f8a8c-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="f8a8c-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-311">IStream</span><span class="sxs-lookup"><span data-stu-id="f8a8c-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f8a8c-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="f8a8c-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="f8a8c-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="f8a8c-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="f8a8c-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="f8a8c-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="f8a8c-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="f8a8c-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="f8a8c-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="f8a8c-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="f8a8c-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="f8a8c-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="f8a8c-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="f8a8c-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="f8a8c-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="f8a8c-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="f8a8c-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="f8a8c-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="f8a8c-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="f8a8c-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="f8a8c-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="f8a8c-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="f8a8c-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="f8a8c-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="f8a8c-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="f8a8c-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="f8a8c-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="f8a8c-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="f8a8c-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="f8a8c-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="f8a8c-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f8a8c-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="f8a8c-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="f8a8c-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="f8a8c-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="f8a8c-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="f8a8c-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="f8a8c-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="f8a8c-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="f8a8c-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="f8a8c-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="f8a8c-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="f8a8c-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="f8a8c-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="f8a8c-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-403">Private1</span><span class="sxs-lookup"><span data-stu-id="f8a8c-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-404">(5)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="f8a8c-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="f8a8c-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="f8a8c-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="f8a8c-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="f8a8c-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="f8a8c-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="f8a8c-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="f8a8c-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="f8a8c-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="f8a8c-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="f8a8c-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="f8a8c-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="f8a8c-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="f8a8c-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="f8a8c-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="f8a8c-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="f8a8c-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="f8a8c-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="f8a8c-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f8a8c-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="f8a8c-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="f8a8c-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="f8a8c-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="f8a8c-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="f8a8c-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="f8a8c-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="f8a8c-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="f8a8c-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="f8a8c-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="f8a8c-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="f8a8c-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="f8a8c-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8a8c-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="f8a8c-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="f8a8c-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8a8c-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="f8a8c-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="f8a8c-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="f8a8c-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

