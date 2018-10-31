---
title: Database メンバー (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58e36426360abf36d7fdf0cb026f6d8ff14b29b5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864024"
---
# <a name="database-members-dao"></a><span data-ttu-id="45184-102">Database メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="45184-102">Database Members (DAO)</span></span>


<span data-ttu-id="45184-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="45184-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45184-104">Database オブジェクトは、開いているデータベースを表します。</span><span class="sxs-lookup"><span data-stu-id="45184-104">A Database object represents an open database.</span></span>

## <a name="methods"></a><span data-ttu-id="45184-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="45184-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45184-106">名前</span><span class="sxs-lookup"><span data-stu-id="45184-106">Name</span></span></p></th>
<th><p><span data-ttu-id="45184-107">説明</span><span class="sxs-lookup"><span data-stu-id="45184-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45184-108"><strong><a href="database-close-method-dao.md">閉じる</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-108"><strong><a href="database-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-109">開いている <strong>Database</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="45184-109">Closes an open <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p101">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-p101">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-114">新しい <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="45184-114">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p102">新しい <strong><a href="relation-object-dao.md">Relation</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-p102">Creates a new <strong><a href="relation-object-dao.md">Relation</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p103">新しい <strong><a href="tabledef-object-dao.md">TableDef</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-p103">Creates a new <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-121"><strong><a href="database-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-121"><strong><a href="database-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-122">指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="45184-122">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-124">データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-124">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-126">既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-126">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-127"><strong><a href="database-openrecordset-method-dao.md">何らか</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-127"><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-128">新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="45184-128">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p104">部分レプリカ内の変更をフル レプリカと同期させ、部分レプリカ内のすべてのレコードを消去し、現在のレプリカ フィルターに基づいて部分レプリカのデータを再設定します (Microsoft Office Access データベース エンジンのデータベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-p104">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-132"><strong><a href="database-synchronize-method-dao.md">同期</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-132"><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p105">2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-p105">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="45184-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="45184-135">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45184-136">名前</span><span class="sxs-lookup"><span data-stu-id="45184-136">Name</span></span></p></th>
<th><p><span data-ttu-id="45184-137">説明</span><span class="sxs-lookup"><span data-stu-id="45184-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45184-138"><strong><a href="database-collatingorder-property-dao.md">照合順序</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-138"><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p106">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45184-p106">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p107">開いているデータベースのソースに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45184-p107">Sets or returns a value that provides information about the source an open database. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="45184-p108">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="45184-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="45184-147">データベースに対応する <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを返します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-147">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p109">指定したデータベースのすべての <strong>Container</strong> オブジェクトを表す <strong>Containers</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45184-p109">Returns a <strong>Containers</strong> collection that represents all of the <strong>Container</strong> objects in the specifed database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-152">レプリカ セットでデザイン マスターを一意に識別する 16 バイトの値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-152">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-153"><strong><a href="database-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-153"><strong><a href="database-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p110">指定したオブジェクトの名前を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45184-p110">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-156"><strong><a href="database-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-156"><strong><a href="database-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p111">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="45184-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-159"><strong><a href="database-querydefs-property-dao.md">クエリ定義</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-159"><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p112">指定したデータベースのすべての <strong>QueryDef</strong> オブジェクトを含む <strong>QueryDefs</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45184-p112">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-163">ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="45184-163">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-165">直前に呼び出された <strong><a href="connection-execute-method-dao.md">Execute</a></strong> メソッドの影響を受けるレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="45184-165">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p113">指定したデータベースの開いているレコードセットをすべて含む <strong>Recordsets</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45184-p113">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p114">指定したデータベースの、すべての保存された <strong>Relation</strong> オブジェクトを含む <strong>Relations</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45184-p114">Returns a <strong>Relations</strong> collection that contains all of the stored <strong>Relation</strong> objects for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-173">データベース レプリカを一意に識別する 16 バイトの値を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="45184-173">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-174"><strong><a href="database-tabledefs-property-dao.md">テーブル定義</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-174"><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p115">指定したデータベースに保存されたすべての <strong>TableDef</strong> オブジェクトを含む <strong>TableDefs</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="45184-p115">Returns a <strong>TableDefs</strong> collection that contains all of the <strong>TableDef</strong> objects stored in the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-177"><strong><a href="database-transactions-property-dao.md">トランザクション</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-177"><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p116">オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45184-p116">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45184-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p117">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="45184-p117">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45184-183"><strong><a href="database-version-property-dao.md">バージョン</a></strong></span><span class="sxs-lookup"><span data-stu-id="45184-183"><strong><a href="database-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="45184-p118">Microsoft Access ワークスペースで、データベースを作成した Microsoft Jet または Microsoft Office Access のデータベース エンジンのバージョンを取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="45184-p118">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

