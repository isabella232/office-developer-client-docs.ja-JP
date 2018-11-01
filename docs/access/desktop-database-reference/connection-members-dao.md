---
title: Connection メンバー (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d2c2af4dcf1cf8661d7cac170e8aa5b679ab083
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886922"
---
# <a name="connection-members-dao"></a><span data-ttu-id="99ffd-102">Connection メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="99ffd-102">Connection Members (DAO)</span></span>

<span data-ttu-id="99ffd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="99ffd-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="99ffd-104">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="99ffd-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="99ffd-105">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="99ffd-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="99ffd-106">Connection オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="99ffd-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 

## <a name="methods"></a><span data-ttu-id="99ffd-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="99ffd-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99ffd-108">名前</span><span class="sxs-lookup"><span data-stu-id="99ffd-108">Name</span></span></p></th>
<th><p><span data-ttu-id="99ffd-109">説明</span><span class="sxs-lookup"><span data-stu-id="99ffd-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="99ffd-111">保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="99ffd-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-112"><strong><a href="connection-close-method-dao.md">閉じる</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-113">開いている <strong>Connection</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="99ffd-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-115">新しい <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-117">指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-118"><strong><a href="connection-openrecordset-method-dao.md">何らか</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-119">新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="99ffd-120">プロパティ</span><span class="sxs-lookup"><span data-stu-id="99ffd-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99ffd-121">名前</span><span class="sxs-lookup"><span data-stu-id="99ffd-121">Name</span></span></p></th>
<th><p><span data-ttu-id="99ffd-122">説明</span><span class="sxs-lookup"><span data-stu-id="99ffd-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-p102">開いている接続のソースに関する情報を提供する値を設定または取得します。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-p102">Sets or returns a value that provides information about the source of an open connection. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-126"><strong><a href="connection-database-property-dao.md">データベース</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="99ffd-127">この接続に対応する <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを返します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="99ffd-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-129"><strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-130"><strong><a href="connection-querydefs-property-dao.md">クエリ定義</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-p103">指定した接続のすべての <strong>QueryDef</strong> オブジェクトを含む <strong>QueryDefs</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="99ffd-p103">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-134">ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-136">直前に呼び出された <strong><a href="connection-execute-method-dao.md">Execute</a></strong> メソッドの影響を受けるレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-p104">指定した接続の開いているレコードセットをすべて含む <strong>Recordsets</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="99ffd-p104">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="99ffd-141">非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="99ffd-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ffd-142"><strong><a href="connection-transactions-property-dao.md">トランザクション</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-p105">オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-p105">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ffd-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="99ffd-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="99ffd-p106">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="99ffd-p106">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

