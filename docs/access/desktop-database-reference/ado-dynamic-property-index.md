---
title: ADO の動的プロパティ インデックス
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bfe788923d623300edac28f0f27534b3ffd8b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283402"
---
# <a name="ado-dynamic-property-index"></a>ADO の動的プロパティ インデックス

**適用先:** Access 2013、Office 2013

データ プロバイダー、サービス プロバイダー、およびサービス コンポーネントでは、開いていない **Connection** オブジェクトおよび [Recordset](connection-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションに動的プロパティを追加できます。これらのオブジェクトが開いている場合は、任意のプロバイダーでも追加プロパティを挿入できます。これらのプロパティの一部は、「 [ADO の動的プロパティ](ado-dynamic-properties.md)」の一覧に示されています。「[付録 A: プロバイダー](appendix-a-providers.md)」には、特定のプロバイダーごとに、さらに詳細な一覧が示されています。

以下の表は、標準的な OLE DB プロバイダーの動的プロパティの ADO 名と OLE DB 名の対応表です。プロバイダーによっては、さらに多くのプロパティをサポートしている場合があります。プロバイダーに固有の動的プロパティの詳細については、各プロバイダーのマニュアルを参照してください。

「OLE DB プログラマ リファレンス」では、ADO プロパティ名が "説明" 欄に示されています。標準的なプロパティの詳細については、「OLE DB プログラマ リファレンス」を参照してください。OLE DB プロパティ名をキーワードとして検索するか、次のトピックを参照してください。

- 「付録 C: プロパティ表」

- 「Supported Properties of the Cursor Service」 (英語)

- 「Supported Properties of the Persistence Provider」 (英語)

- 「Supported OLE DB Properties of the Remoting Provider」 （英語)

## <a name="remarks"></a>注釈

表中で使用されている番号の意味は、次のとおりです。

(1) このプロパティは、ブール型 (Boolean) のフラグで、指定したインターフェイスを使用するかどうかを示します。等価の OLE DB プロパティが存在する場合は、その名前を示します。

(2) "Bookmarkable" ADO プロパティは、下位互換性のために内部的に生成され、OLE DB プロパティの\_DBPROP IROWSETLOCATE にマップされます。 これは、ADO プロパティ IRowsetLocate に対応するプロパティと同じです。

(3) ADO プロパティ名 "Hidden Columns" は、OLE DB プロパティ名の "説明" 欄では "Hidden Columns Count" となっています。

(4) 階層レコードセットの場合、ADO プロパティ "Maximum Rows" はすべての子に適用されます。行が返される順序に応じて、結果セットには、各親のすべての子や一部の子が取得される場合、子が取得されない場合、孤立した子が取得される場合があります。したがって、階層レコードセットをリシェイプする場合、子の ID はそれぞれ一意である必要があります。一般的に、[Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーでは、親から継承できるプロパティと継承できないプロパティを区別できません。

(5) 対応するものがありません。

**Connection の動的プロパティ**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO プロパティ名</p></th>
<th><p>OLE DB プロパティ名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Connect Timeout</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Extended Properties</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Initial Catalog</p></td>
<td><p>DBPROP_INIT_CATALOG</p></td>
</tr>
<tr class="even">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>場所</p></td>
<td><p>DBPROP_INIT_LOCATION</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Services</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="even">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="odd">
<td><p>Persist Security Info</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


**Recordset の動的プロパティ**

**Recordset** オブジェクトの **動的プロパティ** は、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO プロパティ名</p></th>
<th><p>OLE DB プロパティ名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IACCESSOR (1)</p></td>
</tr>
<tr class="even">
<td><p>IChapteredRowset</p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_ICOLUMNSINFO (1)</p></td>
</tr>
<tr class="even">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_ICOLUMNSROWSET (1)</p></td>
</tr>
<tr class="odd">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_ICONNECTIONPOINTCONTAINER (1)</p></td>
</tr>
<tr class="even">
<td><p>iconverttype</p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILOCKBYTES (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IROWSET (1)</p></td>
</tr>
<tr class="odd">
<td><p>idbas/chstatus</p></td>
<td><p>DBPROP_IDBASYNCHSTATUS (1)</p></td>
</tr>
<tr class="even">
<td><p>iparentrowset</p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IROWSETCHANGE (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetExactScroll</p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetFind</p></td>
<td><p>DBPROP_IROWSETFIND (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IROWSETIDENTITY (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IROWSETINFO (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IROWSETLOCATE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetRefresh</p></td>
<td><p>DBPROP_IROWSETREFRESH (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IROWSETSCROLL (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IROWSETUPDATE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetView</p></td>
<td><p>DBPROP_IROWSETVIEW (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IROWSETINDEX (1)</p></td>
</tr>
<tr class="odd">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISEQUENTIALSTREAM (1)</p></td>
</tr>
<tr class="even">
<td><p>IStorage</p></td>
<td><p>DBPROP_ISTORAGE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_ISTREAM (1)</p></td>
</tr>
<tr class="even">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISUPPORTERRORINFO (1)</p></td>
</tr>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Asynchronous Rowset Processing</p></td>
<td><p>DBPROP_ROWSET_ASYNCH</p></td>
</tr>
<tr class="even">
<td><p>Auto Recalc</p></td>
<td><p>DBPROP_ADC_AUTORECALC</p></td>
</tr>
<tr class="odd">
<td><p>Background Fetch Size</p></td>
<td><p>DBPROP_ASYNCHFETCHSIZE</p></td>
</tr>
<tr class="even">
<td><p>Background Thread Priority</p></td>
<td><p>DBPROP_ASYNCHTHREADPRIORITY</p></td>
</tr>
<tr class="odd">
<td><p>Batch Size</p></td>
<td><p>DBPROP_ADC_BATCHSIZE</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE (2)</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarks Ordered</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Cache Child Rows</p></td>
<td><p>DBPROP_ADC_CACHECHILDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Cache Deferred Columns</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Column Writable</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Command Time Out</p></td>
<td><p>DBPROP_COMMANDTIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Cursor Engine Version</p></td>
<td><p>DBPROP_ADC_CEVER</p></td>
</tr>
<tr class="even">
<td><p>Defer Column</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="odd">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Filter Operations</p></td>
<td><p>DBPROP_FILTERCOMPAREOPS</p></td>
</tr>
<tr class="even">
<td><p>Find Operations</p></td>
<td><p>DBPROP_FINDCOMPAREOPS</p></td>
</tr>
<tr class="odd">
<td><p>Hidden Columns (Count)</p></td>
<td><p>DBPROP_HIDDENCOLUMNS (3)</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>Initial Fetch Size</p></td>
<td><p>DBPROP_ASYNCHPREFETCHSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status</p></td>
<td><p>DBPROP_ADC_MAINTAINCHANGESTATUS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS (4)</p></td>
</tr>
<tr class="odd">
<td><p>Memory Usage</p></td>
<td><p>DBPROP_MEMORYUSAGE</p></td>
</tr>
<tr class="even">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Others' Changes Visible</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Others' Inserts Visible</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Private1</p></td>
<td><p>5</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Reshape Name</p></td>
<td><p>DBPROP_ADC_RESHAPENAME</p></td>
</tr>
<tr class="odd">
<td><p>Resync Command</p></td>
<td><p>DBPROP_ADC_CUSTOMRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Server Cursor</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="odd">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Unique Catalog</p></td>
<td><p>DBPROP_ADC_UNIQUECATALOG</p></td>
</tr>
<tr class="even">
<td><p>Unique Rows</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Unique Schema</p></td>
<td><p>DBPROP_ADC_UNIQUESCHEMA</p></td>
</tr>
<tr class="even">
<td><p>Unique Table</p></td>
<td><p>DBPROP_ADC_UNIQUETABLE</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria</p></td>
<td><p>DBPROP_ADC_UPDATECRITERIA</p></td>
</tr>
<tr class="odd">
<td><p>Update Resync</p></td>
<td><p>DBPROP_ADC_UPDATERESYNC</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>

