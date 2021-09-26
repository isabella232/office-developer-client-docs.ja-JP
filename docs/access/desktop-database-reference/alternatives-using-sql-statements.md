---
title: '他の方法: SQL ステートメントの使用'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8dccb7c4d3f7d8e0ddb74c8c05dee8f2d0438f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607410"
---
# <a name="alternatives-using-sql-statements"></a>他の方法: SQL ステートメントの使用


**適用先**: Access 2013、Office 2013

ADO では、組み込みのプロパティおよびメソッドの代わりに、コマンドを使用してデータを編集することもできます。プロバイダーによっては、この章で説明しているすべての操作を、データ ソースにコマンドを渡すことによって実行することもできます。たとえば、 **Field** の **Value** プロパティを使用せずに、SQL の UPDATE ステートメントを使用して、データを変更できます。また、ADO の **AddNew** メソッドではなく、SQL の INSERT ステートメントを使用して、新しいレコードをデータ ソースに追加できます。SQL またはプロバイダーで使用されるデータ操作言語の詳細については、使用しているデータ ソースのドキュメントを参照してください。

たとえば、次のコードのように、DELETE ステートメントを含む SQL の構文をデータベースに渡すことができます。

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

