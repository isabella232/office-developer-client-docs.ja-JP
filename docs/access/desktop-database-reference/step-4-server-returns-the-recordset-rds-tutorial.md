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
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a><span data-ttu-id="1f985-102">手順 4: サーバーによりレコードセットが返される (RDS チュートリアル)</span><span class="sxs-lookup"><span data-stu-id="1f985-102">Step 4: Server Returns the Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="1f985-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1f985-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f985-104">RDS は、取得した**レコード セット**オブジェクトをクライアントに送信できるフォームに変換します (つまり、**レコード セット**の*マーシャ リング*)。</span><span class="sxs-lookup"><span data-stu-id="1f985-104">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="1f985-105">変換し、それを送信する方法の正確な形式は、サーバーがインターネットまたはイントラネット、ローカル エリア ネットワークでは、上またはダイナミック リンク ライブラリは、かどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1f985-105">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="1f985-106">ただし、この詳細重要ではありません。すべての問題が、RDS は、クライアントに**レコード セット**を送信します。</span><span class="sxs-lookup"><span data-stu-id="1f985-106">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="1f985-107">クライアント側では、 **Recordset** オブジェクトが返され、ローカル変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1f985-107">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

