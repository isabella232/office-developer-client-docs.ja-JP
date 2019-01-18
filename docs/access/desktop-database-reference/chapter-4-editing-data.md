---
title: '第 4 章: データの編集'
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b954cf8b730a74fb7e630fbafb96c046491c6f46
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701145"
---
# <a name="chapter-4-editing-data"></a>第 4 章: データの編集

**適用されます**Access 2013、Office 2013。

前の 2 つの章では、ADO を使用して、データ ソースへの接続、コマンドの実行、 **Recordset** オブジェクトへの結果の取得、および **Recordset** 内での移動を行う方法を説明しました。この章では、ADO のもう 1 つの基本的操作であるデータの編集について説明します。

この章でも、3 章で使用したサンプルの **Recordset** を引き続き使用しますが、重要な違いが 1 つあります。 **Recordset** を開くときには、次のコードを使用します。

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

コードの重要な変更点とは、GetNewConnection 関数の中で、 **Connection** オブジェクトの **CursorLocation** プロパティを **adUseClient** に設定することです (下記参照)。これは、クライアント カーソルを使用することを示します。クライアント側カーソルとサーバー側カーソルの違いの詳細については、「 [8 章: カーソルとロックの概要](chapter-8-understanding-cursors-and-locks.md)」を参照してください。

**CursorLocation** プロパティを **adUseClient** に設定すると、カーソルの位置がデータ ソース (この場合は SQL Server) からクライアント コードの場所 (デスクトップ ワークステーション) に移動します。この設定により、カーソルを作成および管理するため、ADO によってクライアント上に Client Cursor Engine for OLE DB が強制的に起動されます。

また、 **Open** メソッドの **LockType** パラメーターも **adLockBatchOptimistic** に変更されています。これにより、カーソルがバッチ モードで開かれます。このモードでは、プロバイダーが複数の変更をキャッシュに保存し、 **UpdateBatch** メソッドが呼び出されたときに初めてその変更を基になるデータ ソースに書き込みます。 **Recordset** に加えられた変更は、 **UpdateBatch** メソッドが呼び出されるまで、データベースに反映されません。

最後に、この章のコードでは、2 章で使用した GetNewConnection 関数を変更したものを使用します。変更後の関数は、クライアント側カーソルを返すようになっています。その関数は次のようになります。

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

この章では、次のトピックについて説明します。

- [既存のレコードの編集](editing-existing-records.md)
- [サポート内容の決定](determining-what-is-supported.md)
- [Delete メソッドによるレコードの削除](deleting-records-using-the-delete-method.md)
- [他の方法: SQL ステートメントを使用します。](alternatives-using-sql-statements.md)
- [(ADO) のレコードを追加します。](adding-records.md)
