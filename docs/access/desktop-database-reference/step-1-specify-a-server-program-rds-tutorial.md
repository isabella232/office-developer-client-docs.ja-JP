---
title: '手順 1: サーバー プログラムを指定する (RDS チュートリアル)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5bd5e8edc17eb482177d97cb82611a8b6b12d0a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946056"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="d2fd1-102">手順 1: サーバー プログラム (RDS チュートリアル) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2fd1-102">Step 1: Specify a server program (RDS Tutorial)</span></span>

<span data-ttu-id="d2fd1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d2fd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2fd1-104">最も一般的には、使用して[rds.インスタンス](dataspace-object-rds.md)オブジェクトの[CreateObject](createobject-method-rds.md)メソッドを既定のサーバー プログラム、 [RDSServer.DataFactory](datafactory-object-rdsserver.md)、または独自のカスタム サーバー プログラム (ビジネス オブジェクト) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2fd1-104">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="d2fd1-105">サーバー プログラムは、サーバーとサーバーのプログラム、または*プロキシ*への参照がインスタンス化されるが返されます。</span><span class="sxs-lookup"><span data-stu-id="d2fd1-105">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="d2fd1-106">このチュートリアルでは、既定のサーバー プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="d2fd1-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

