---
title: Visual J では (デスクトップ データベース参照のアクセス)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d40a820b5ee3bd6e5c423cbb963a4514d4ff40e1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874546"
---
# <a name="visual-j"></a>Visual J++


**適用されます**Access 2013、Office 2013。

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

まず、クラス メソッド*onConnectionComplete*が新しい**ConnectionEventHandler**オブジェクトを作成し、 *onConnectComplete*関数をオブジェクトに割り当てることによって**ConnectionComplete**イベントに関連付けられています。

*Main*関数は、**接続**オブジェクトを作成し、 **addOnConnectComplete**メソッドを呼び出すと、*ハンドラー*関数のアドレスを渡すことによって処理するイベントを有効にします。

