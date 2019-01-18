---
title: ワークスペースのメンバー (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a2105c13f5f7ce9a75e7e18e20477d8b283543a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719234"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="e5406-102">ワークスペースのメンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="e5406-102">Workspace members (DAO)</span></span>


<span data-ttu-id="e5406-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e5406-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5406-p101">Workspace オブジェクトは、ユーザー用に名前付きセッションを定義します。これには開いているデータベースが含まれ、同時実行トランザクションのメカニズムを提供し、Microsoft Access ワークスペースの場合は、セキュリティが設定されたワークグループをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e5406-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="e5406-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e5406-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5406-107">名前</span><span class="sxs-lookup"><span data-stu-id="e5406-107">Name</span></span></p></th>
<th><p><span data-ttu-id="e5406-108">説明</span><span class="sxs-lookup"><span data-stu-id="e5406-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5406-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p102">新しいトランザクションを開始します。値の取得および設定が可能です。データベース型 ( <strong>Database</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5406-p102">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-112"><strong><a href="workspace-close-method-dao.md">閉じる</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-113">開いている <strong>Workspace</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5406-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-115">現在のトランザクションを終了し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="e5406-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-116"><strong><a href="workspace-createdatabase-method-dao.md">データベース</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-117">新しい <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた <strong>Database</strong> オブジェクトとして返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e5406-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-119"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e5406-119"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e5406-120">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="e5406-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="e5406-121">ODBC データ ソースの <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを開きます (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e5406-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-123"><strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクト内で指定されたデータベースを開き、そのデータベースを表す <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="e5406-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-125">現在のトランザクションを終了し、 <strong>Workspace</strong> オブジェクト内のすべてのデータベースを、現在のトランザクションが開始される前の状態に戻します。</span><span class="sxs-lookup"><span data-stu-id="e5406-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="e5406-126">Properties</span><span class="sxs-lookup"><span data-stu-id="e5406-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5406-127">名前</span><span class="sxs-lookup"><span data-stu-id="e5406-127">Name</span></span></p></th>
<th><p><span data-ttu-id="e5406-128">説明</span><span class="sxs-lookup"><span data-stu-id="e5406-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5406-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p104">指定された <strong>Workspace</strong> の現在の接続を表す <strong>Connections</strong> コレクションを取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e5406-p104">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p105">指定された <strong>Workspace</strong> の開いているデータベースを表す <strong>Databases</strong> コレクションを取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e5406-p105">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-136"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e5406-136"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e5406-137">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="e5406-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="e5406-138"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> メソッドまたは <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> メソッドによって作成された接続で使用されるカーソル ドライバーの種類を設定または取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e5406-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-140">同じ Microsoft Access データベース エンジンに接続された ODBC データ ソースに関連する複数のトランザクションが分離されているかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e5406-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-142">ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="e5406-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p107">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5406-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5406-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p108">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="e5406-p108">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5406-150"><strong><a href="workspace-type-property-dao.md">型</a></strong></span><span class="sxs-lookup"><span data-stu-id="e5406-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e5406-p109">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5406-p109">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

