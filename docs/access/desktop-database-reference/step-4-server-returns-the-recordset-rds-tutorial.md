---
title: '手順 4: サーバーからレコードセットを返す (RDS チュートリアル)'
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c7aaaa556d11fc3c457c89a35edb1240628aa9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868624"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a>手順 4: サーバーによりレコードセットが返される (RDS チュートリアル)


**適用されます**Access 2013、Office 2013。

RDS は、取得した**レコード セット**オブジェクトをクライアントに送信できるフォームに変換します (つまり、**レコード セット**の*マーシャ リング*)。 変換し、それを送信する方法の正確な形式は、サーバーがインターネットまたはイントラネット、ローカル エリア ネットワークでは、上またはダイナミック リンク ライブラリは、かどうかによって異なります。 ただし、この詳細重要ではありません。すべての問題が、RDS は、クライアントに**レコード セット**を送信します。

クライアント側では、 **Recordset** オブジェクトが返され、ローカル変数に割り当てられます。

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

