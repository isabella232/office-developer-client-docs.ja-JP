---
title: Connection メンバー (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 001cb1372acf4a4a55b3841a3f4ca8d6598f55e8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476985"
---
# <a name="connection-members-dao"></a><span data-ttu-id="70313-102">Connection メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="70313-102">Connection Members (DAO)</span></span>


<span data-ttu-id="70313-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="70313-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="70313-p101">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。 Connection オブジェクトは、ODBC データベースへの接続を表します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70313-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span></P>



## <a name="methods"></a><span data-ttu-id="70313-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="70313-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70313-107">名前</span><span class="sxs-lookup"><span data-stu-id="70313-107">Name</span></span></p></th>
<th><p><span data-ttu-id="70313-108">説明</span><span class="sxs-lookup"><span data-stu-id="70313-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70313-109"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-109"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="70313-p102">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="70313-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="70313-112">保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70313-112">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-113"><strong><a href="connection-close-method-dao.md">閉じる</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-113"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-114">開いている <strong>Connection</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="70313-114">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-116">新しい <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="70313-116">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-118">指定したオブジェクトのアクション クエリまたは SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="70313-118">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-119"><strong><a href="connection-openrecordset-method-dao.md">何らか</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-119"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-120">新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成して <strong>Recordsets</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="70313-120">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="70313-121">プロパティ</span><span class="sxs-lookup"><span data-stu-id="70313-121">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70313-122">名前</span><span class="sxs-lookup"><span data-stu-id="70313-122">Name</span></span></p></th>
<th><p><span data-ttu-id="70313-123">説明</span><span class="sxs-lookup"><span data-stu-id="70313-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70313-124"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-124"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-p103">開いている接続のソースに関する情報を提供する値を設定または取得します。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="70313-p103">Sets or returns a value that provides information about the source of an open connection. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-127"><strong><a href="connection-database-property-dao.md">データベース</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-127"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="70313-p104">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="70313-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="70313-130">この接続に対応する <strong><a href="database-object-dao.md">Database</a></strong> オブジェクトを返します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70313-130">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-131"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-131"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-132"><strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="70313-132">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-133"><strong><a href="connection-querydefs-property-dao.md">クエリ定義</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-133"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-p105">指定した接続のすべての <strong>QueryDef</strong> オブジェクトを含む <strong>QueryDefs</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="70313-p105">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-137">ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="70313-137">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-139">直前に呼び出された <strong><a href="connection-execute-method-dao.md">Execute</a></strong> メソッドの影響を受けるレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="70313-139">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-p106">指定した接続の開いているレコードセットをすべて含む <strong>Recordsets</strong> コレクションを返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="70313-p106">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="70313-p107">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="70313-p107">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="70313-146">非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="70313-146">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70313-147"><strong><a href="connection-transactions-property-dao.md">トランザクション</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-147"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-p108">オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="70313-p108">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70313-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="70313-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="70313-p109">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="70313-p109">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

