---
title: '手順 1: サーバー プログラムを指定する (RDS チュートリアル)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89aa87aa63a3d8bfdeb291f78d6525f51c4262b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476179"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>手順 1: サーバー プログラムを指定する (RDS チュートリアル)


**適用されます**Access 2013 |。Office 2013

最も一般的には、使用して[rds.インスタンス](dataspace-object-rds.md)オブジェクトの[CreateObject](createobject-method-rds.md)メソッドを既定のサーバー プログラム、 [RDSServer.DataFactory](datafactory-object-rdsserver.md)、または独自のカスタム サーバー プログラム (ビジネス オブジェクト) を指定します。 サーバー プログラムは、サーバーとサーバーのプログラム、または*プロキシ*への参照がインスタンス化されるが返されます。

このチュートリアルでは、既定のサーバー プログラムを使用します。

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

