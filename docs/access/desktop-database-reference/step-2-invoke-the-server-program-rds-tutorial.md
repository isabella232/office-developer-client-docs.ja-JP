---
title: '手順 2: サーバー プログラムを呼び出す (RDS チュートリアル)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edd9f8561e6275e3b8eb33e86be745345d7c797a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479240"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>手順 2: サーバー プログラムを呼び出す (RDS チュートリアル)


**適用されます**Access 2013 |。Office 2013

クライアント*プロキシ*のメソッドを呼び出すと、サーバー上の実際のプログラムは、メソッドを実行します。 この手順では、サーバー上でクエリを実行します。

**部品 A**この手順を実行する最も便利な方法[rds. を使用することをこのチュートリアルで[RDSServer.DataFactory](datafactory-object-rdsserver.md)を使用していない場合DataControl](datacontrol-object-rds.md)オブジェクトです。 **RDS.DataControl** によって、プロキシを作成する前の手順が、クエリを発行するこの手順と結合されます。

サーバー プログラムのインスタンスを作成する場所を識別するために **RDS.DataControl** オブジェクトの [Server](server-property-rds.md) プロパティを、データ ソースにアクセスする接続文字列を指定するために [Connect](connect-property-rds.md) プロパティを、クエリ コマンド テキストを指定するために [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) プロパティをそれぞれ設定します。次に [Refresh](refresh-method-rds.md) メソッドを発行して、サーバー プログラムがデータ ソースに接続してクエリで指定された行を取得し、 **Recordset** オブジェクトをクライアントに返すようにします。

このチュートリアルでは **RDS.DataControl** を使用しませんが、使用する場合は次のようになります。

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

また、このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**パート 2**この手順を実行するための一般的な方法では、 **RDSServer.DataFactory**オブジェクトの[Query](query-method-rds.md)メソッドを呼び出します。 このメソッドは、データ ソースへの接続に使用される接続文字列と、データ ソースから返される行の指定に使用されるコマンド テキストを取得します。

このチュートリアルでは、 **DataFactory** オブジェクトの **Query** メソッドを使用します。

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

