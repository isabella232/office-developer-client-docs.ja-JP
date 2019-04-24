---
title: DBEngine メンバー (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294282"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="fa570-102">DBEngine メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa570-102">DBEngine members (DAO)</span></span>


<span data-ttu-id="fa570-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa570-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa570-104">DBEngine オブジェクトは、DAO オブジェクト モデル内のトップ レベル オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="fa570-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="fa570-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="fa570-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa570-106">名前</span><span class="sxs-lookup"><span data-stu-id="fa570-106">Name</span></span></p></th>
<th><p><span data-ttu-id="fa570-107">説明</span><span class="sxs-lookup"><span data-stu-id="fa570-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa570-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-109">新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="fa570-109">Begins a new transaction.</span></span> <span data-ttu-id="fa570-110">読み取り/書き込みの<strong>データベース</strong>です。</span><span class="sxs-lookup"><span data-stu-id="fa570-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-112">現在のトランザクションを終了し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="fa570-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-114">閉じられたデータベースをコピーして最適化し、そのデータベースのバージョン、照合順序、暗号化を変更するオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa570-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="fa570-115">(Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="fa570-116">.</span><span class="sxs-lookup"><span data-stu-id="fa570-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-118">新しい <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた <strong>Database</strong> オブジェクトとして返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="fa570-119">.</span><span class="sxs-lookup"><span data-stu-id="fa570-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-121">新しい <strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fa570-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-122"><strong><a href="dbengine-idle-method-dao.md">アイドル</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-123">データの処理を中断し、Microsoft Access データベース エンジンでメモリの最適化やページのタイムアウトなどのタスクを完了できるようにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-125"><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong>値の1つ。</span><span class="sxs-lookup"><span data-stu-id="fa570-125">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="fa570-126"><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fa570-126"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="fa570-127">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="fa570-127">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="fa570-128">ODBC データ ソースの <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを開きます (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-128">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-130">指定されたデータベースを開き、そのデータベースを表す <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa570-130">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-p105">ODBC データ ソースの接続情報を Windows レジストリに追加します。ODBC ドライバーでは、セッション中に ODBC データ ソースが開かれるときに、接続情報が必要になります。</span><span class="sxs-lookup"><span data-stu-id="fa570-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-135">現在のトランザクションを終了し、 <strong>Workspace</strong> オブジェクト内のデータベースを現在のトランザクションが開始された時点の状態に戻します。</span><span class="sxs-lookup"><span data-stu-id="fa570-135">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-137">Windows レジストリに登録されている Microsoft Access データベース エンジンのキーの値を一時的に上書きします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-137">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="fa570-138">プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa570-138">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa570-139">名前</span><span class="sxs-lookup"><span data-stu-id="fa570-139">Name</span></span></p></th>
<th><p><span data-ttu-id="fa570-140">説明</span><span class="sxs-lookup"><span data-stu-id="fa570-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa570-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-142">初期化されたときに、既定の<strong>Workspace</strong>オブジェクトを作成するために使用するパスワードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa570-142">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="fa570-143">値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</span><span class="sxs-lookup"><span data-stu-id="fa570-143">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-145">次に作成される <strong><a href="workspace-object-dao.md">Workspace</a></strong> オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="fa570-145">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-147">初期化されたときに、既定の<strong>Workspace</strong>オブジェクトを作成するために使用されるユーザー名を設定します。</span><span class="sxs-lookup"><span data-stu-id="fa570-147">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="fa570-148">値の取得と設定が可能な文字列型 (<strong>String</strong>) の値です。</span><span class="sxs-lookup"><span data-stu-id="fa570-148">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-149"><strong><a href="dbengine-errors-property-dao.md">エラー</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-149"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-150">指定したオブジェクトの、すべての保存された <strong>Error</strong> オブジェクトを含む <strong>Errors</strong> コレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="fa570-150">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="fa570-151">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fa570-151">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-153">Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="fa570-153">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-155">ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="fa570-155">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-p109">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="fa570-p109">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa570-159"><strong><a href="dbengine-version-property-dao.md">バージョン</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-160">rreturns 現在使用されている DAO のバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="fa570-160">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="fa570-161">読み取りのみ可能な <strong>String</strong> 値です。</span><span class="sxs-lookup"><span data-stu-id="fa570-161">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa570-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa570-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa570-163">アクティブな、隠されていない <strong>Workspace</strong> オブジェクトをすべて含む <strong>Workspaces</strong> コレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="fa570-163">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="fa570-164">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fa570-164">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

