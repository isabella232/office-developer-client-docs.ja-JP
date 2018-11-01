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
# <a name="visual-j"></a><span data-ttu-id="80bca-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="80bca-102">Visual J++</span></span>


<span data-ttu-id="80bca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="80bca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80bca-104">この短い Microsoft Visual J++ の例では、独自の関数を特定のイベントに関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="80bca-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

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

<span data-ttu-id="80bca-105">まず、クラス メソッド*onConnectionComplete*が新しい**ConnectionEventHandler**オブジェクトを作成し、 *onConnectComplete*関数をオブジェクトに割り当てることによって**ConnectionComplete**イベントに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="80bca-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="80bca-106">*Main*関数は、**接続**オブジェクトを作成し、 **addOnConnectComplete**メソッドを呼び出すと、*ハンドラー*関数のアドレスを渡すことによって処理するイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="80bca-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

