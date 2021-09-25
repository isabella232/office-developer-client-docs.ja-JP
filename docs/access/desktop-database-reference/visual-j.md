---
title: Visual J++ (Access デスクトップ データベース リファレンス)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 93952438594d87e9985d44f22ca4e071a974e5f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572530"
---
# <a name="visual-j"></a>Visual J++


**適用先:** Access 2013、Office 2013

この短い Microsoft Visual J++ の例では、独自の関数を特定のイベントに関連付ける方法を示します。

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

まず、新しい **ConnectionEventHandler** オブジェクトを作成し、*onConnectComplete* 関数をこのオブジェクトに割り当てることにより、クラス メソッド *onConnectionComplete* が **ConnectionComplete** イベントに関連付けられます。

その後、*main* 関数で **Connection** オブジェクトが作成され、**addOnConnectComplete** メソッドを呼び出して *handler* 関数のアドレスを渡すことにより、イベントの処理が有効になります。

