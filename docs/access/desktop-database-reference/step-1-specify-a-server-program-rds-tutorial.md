---
title: '手順 1: サーバー プログラムを指定する (RDS チュートリアル)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fe85853b013caf8610e7706f3d836551ce8801c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871879"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>手順 1: サーバー プログラムの指定 (RDS チュートリアル)


**適用されます**Access 2013、Office 2013。

最も一般的には、使用して[rds.インスタンス](dataspace-object-rds.md)オブジェクトの[CreateObject](createobject-method-rds.md)メソッドを既定のサーバー プログラム、 [RDSServer.DataFactory](datafactory-object-rdsserver.md)、または独自のカスタム サーバー プログラム (ビジネス オブジェクト) を指定します。 サーバー プログラムは、サーバーとサーバーのプログラム、または*プロキシ*への参照がインスタンス化されるが返されます。

このチュートリアルでは、既定のサーバー プログラムを使用します。

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

