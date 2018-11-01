---
title: '第 4 章: データの編集'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a484cef1e04ce84c30d823a2ac7783008651e77d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875792"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="52098-102">第 4 章: データの編集</span><span class="sxs-lookup"><span data-stu-id="52098-102">Chapter 4: Editing Data</span></span>


<span data-ttu-id="52098-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="52098-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52098-p101">前の 2 つの章では、ADO を使用して、データ ソースへの接続、コマンドの実行、 **Recordset** オブジェクトへの結果の取得、および **Recordset** 内での移動を行う方法を説明しました。この章では、ADO のもう 1 つの基本的操作であるデータの編集について説明します。</span><span class="sxs-lookup"><span data-stu-id="52098-p101">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**. This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="52098-p102">この章でも、3 章で使用したサンプルの **Recordset** を引き続き使用しますが、重要な違いが 1 つあります。 **Recordset** を開くときには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="52098-p102">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change. The following code is used to open the **Recordset**:</span></span>

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

<span data-ttu-id="52098-p103">コードの重要な変更点とは、GetNewConnection 関数の中で、 **Connection** オブジェクトの **CursorLocation** プロパティを **adUseClient** に設定することです (下記参照)。これは、クライアント カーソルを使用することを示します。クライアント側カーソルとサーバー側カーソルの違いの詳細については、「 [8 章: カーソルとロックの概要](chapter-8-understanding-cursors-and-locks.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52098-p103">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor. For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="52098-p104">**CursorLocation** プロパティを **adUseClient** に設定すると、カーソルの位置がデータ ソース (この場合は SQL Server) からクライアント コードの場所 (デスクトップ ワークステーション) に移動します。この設定により、カーソルを作成および管理するため、ADO によってクライアント上に Client Cursor Engine for OLE DB が強制的に起動されます。</span><span class="sxs-lookup"><span data-stu-id="52098-p104">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation). This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="52098-p105">また、 **Open** メソッドの **LockType** パラメーターも **adLockBatchOptimistic** に変更されています。これにより、カーソルがバッチ モードで開かれます。このモードでは、プロバイダーが複数の変更をキャッシュに保存し、 **UpdateBatch** メソッドが呼び出されたときに初めてその変更を基になるデータ ソースに書き込みます。 **Recordset** に加えられた変更は、 **UpdateBatch** メソッドが呼び出されるまで、データベースに反映されません。</span><span class="sxs-lookup"><span data-stu-id="52098-p105">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**. This opens the cursor in batch mode. (The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="52098-p106">最後に、この章のコードでは、2 章で使用した GetNewConnection 関数を変更したものを使用します。変更後の関数は、クライアント側カーソルを返すようになっています。その関数は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="52098-p106">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2. This version of the function now returns a client-side cursor. The function looks like this:</span></span>

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

<span data-ttu-id="52098-118">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="52098-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="52098-119">既存のレコードを編集する</span><span class="sxs-lookup"><span data-stu-id="52098-119">Editing Existing Records</span></span>](editing-existing-records.md)

- [<span data-ttu-id="52098-120">サポートされている内容を確認する</span><span class="sxs-lookup"><span data-stu-id="52098-120">Determining What is Supported</span></span>](determining-what-is-supported.md)

- [<span data-ttu-id="52098-121">Delete メソッドを使ってレコードを削除する</span><span class="sxs-lookup"><span data-stu-id="52098-121">Deleting Records Using the Delete Method</span></span>](deleting-records-using-the-delete-method.md)

- [<span data-ttu-id="52098-122">他の方法: SQL ステートメントを使用する</span><span class="sxs-lookup"><span data-stu-id="52098-122">Alternatives: Using SQL Statements</span></span>](alternatives-using-sql-statements.md)

- [<span data-ttu-id="52098-123">レコードを追加する (ADO)</span><span class="sxs-lookup"><span data-stu-id="52098-123">Adding Records (ADO)</span></span>](adding-records.md)