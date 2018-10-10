---
title: '他の方法: SQL ステートメントを使用する'
TOCTitle: 'Alternatives: Using SQL Statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9451dfef969120e6ffc4835263a7ad02881748d2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477253"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="23e61-102">他の方法: SQL ステートメントを使用する</span><span class="sxs-lookup"><span data-stu-id="23e61-102">Alternatives: Using SQL Statements</span></span>


<span data-ttu-id="23e61-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="23e61-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23e61-p101">ADO では、組み込みのプロパティおよびメソッドの代わりに、コマンドを使用してデータを編集することもできます。プロバイダーによっては、この章で説明しているすべての操作を、データ ソースにコマンドを渡すことによって実行することもできます。たとえば、 **Field** の **Value** プロパティを使用せずに、SQL の UPDATE ステートメントを使用して、データを変更できます。また、ADO の **AddNew** メソッドではなく、SQL の INSERT ステートメントを使用して、新しいレコードをデータ ソースに追加できます。SQL またはプロバイダーで使用されるデータ操作言語の詳細については、使用しているデータ ソースのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23e61-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="23e61-109">たとえば、次のコードのように、DELETE ステートメントを含む SQL の構文をデータベースに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="23e61-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

