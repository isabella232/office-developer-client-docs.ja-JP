---
title: RDS チュートリアル (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b01809cd17c9c1a5c1a73a5765bb8808692e4c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877920"
---
# <a name="rds-tutorial-visual-j"></a>RDS チュートリアル (Visual J++)


**適用されます**Access 2013、Office 2013。

ADO/WFC は、[DataControl (RDS)](datacontrol-object-rds.md) オブジェクトを実装していないという点で、RDS オブジェクト モデルに完全には準拠していません。ADO/WFC は、クライアント側のクラスの [DataSpace (RDS)](dataspace-object-rds.md) のみを実装しています。

**DataSpace** クラスは、 [ObjectProxy](createobject-method-rds.md) オブジェクトを返す [CreateObject](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) メソッドを実装しています。 **DataSpace** クラスは、 [InternetTimeout](internettimeout-property-rds.md) プロパティも実装しています。

**ObjectProxy** クラスは、サーバー側の任意のビジネス オブジェクトを呼び出すことができる call メソッドを実装しています。

**ここからチュートリアルを開始します。**

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

**これでチュートリアルを終了します。**

