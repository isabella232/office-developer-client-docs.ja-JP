---
title: '手順 6: サーバーに変更を送信する (RDS チュートリアル)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d26ca621ba7102dc0f9c6219ba3a16b28138770f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477685"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>手順 6: サーバーに変更を送信する (RDS チュートリアル)


**適用されます**Access 2013 |。Office 2013

**Recordset** オブジェクトが編集された場合、あらゆる変更内容 (つまり、追加、変更、または削除された行) をサーバーに返送できます。


> [!NOTE]
> <P>ADO オブジェクトおよび Microsoft OLE DB Remoting Provider を使用して、RDS の既定の動作を暗黙的に呼び出すことができます。クエリは <STRONG>Recordset</STRONG> を返すことができ、編集された <STRONG>Recordset</STRONG> はデータ ソースを更新できます。このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。</P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**部品 A** 

この場合にだけ rds. の[を使っていること前提としています。DataControl](datacontrol-object-rds.md) **rds. 関連付けし、**レコード セット**オブジェクトであるようになりましたDataControl**。 [Server](submitchanges-method-rds.md) プロパティと **Connect** プロパティが引き続き設定されていれば、 [SubmitChanges](server-property-rds.md) メソッドによって [Recordset](connect-property-rds.md) オブジェクトへの変更がデータ ソースに反映されます。

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

**パート 2** 

または、更新することがサーバー [RDSServer.DataFactory](datafactory-object-rdsserver.md)オブジェクトが、接続と**レコード セット**オブジェクトを指定します。

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

**これでチュートリアルを終了します。**

