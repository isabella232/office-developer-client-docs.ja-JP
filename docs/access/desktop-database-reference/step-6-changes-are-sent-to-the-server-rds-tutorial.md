---
title: '手順 6: サーバーに変更を送信する (RDS チュートリアル)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998995"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="29bfa-102">手順 6: 変更内容がサーバーに送信される、(RDS チュートリアル)</span><span class="sxs-lookup"><span data-stu-id="29bfa-102">Step 6: Changes are sent to the server (RDS Tutorial)</span></span>

<span data-ttu-id="29bfa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="29bfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29bfa-104">**Recordset** オブジェクトが編集された場合、あらゆる変更内容 (つまり、追加、変更、または削除された行) をサーバーに返送できます。</span><span class="sxs-lookup"><span data-stu-id="29bfa-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="29bfa-105">[!メモ] ADO オブジェクトおよび Microsoft OLE DB Remoting Provider を使用して、RDS の既定の動作を暗黙的に呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="29bfa-105">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="29bfa-106">クエリは**レコード セット**を返すことができ、編集した**レコード セット**は、データ ソースを更新できます。</span><span class="sxs-lookup"><span data-stu-id="29bfa-106">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="29bfa-107">このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="29bfa-107">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="29bfa-108">**部品 A**</span><span class="sxs-lookup"><span data-stu-id="29bfa-108">**Part A**</span></span> 

<span data-ttu-id="29bfa-109">この場合にだけ rds. の[を使っていること前提としています。DataControl](datacontrol-object-rds.md) **rds. 関連付けし、**レコード セット**オブジェクトであるようになりましたDataControl**。</span><span class="sxs-lookup"><span data-stu-id="29bfa-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="29bfa-110">[Server](submitchanges-method-rds.md) プロパティと **Connect** プロパティが引き続き設定されていれば、 [SubmitChanges](server-property-rds.md) メソッドによって [Recordset](connect-property-rds.md) オブジェクトへの変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="29bfa-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

<span data-ttu-id="29bfa-111">**パート 2**</span><span class="sxs-lookup"><span data-stu-id="29bfa-111">**Part B**</span></span> 

<span data-ttu-id="29bfa-112">または、更新することがサーバー [RDSServer.DataFactory](datafactory-object-rdsserver.md)オブジェクトが、接続と**レコード セット**オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="29bfa-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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

<span data-ttu-id="29bfa-113">**これでチュートリアルを終了します。**</span><span class="sxs-lookup"><span data-stu-id="29bfa-113">**This is the end of the tutorial.**</span></span>

