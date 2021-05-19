---
title: 通知の送信を行う
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433284"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="b0513-103">通知の送信を行う</span><span class="sxs-lookup"><span data-stu-id="b0513-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="b0513-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0513-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0513-105">サービス プロバイダーが [IMAPISupport : IUnknown](imapisupportiunknown.md) メソッドを通知に使用する場合、MAPI は非表示ウィンドウとそれに対応するウィンドウ プロシージャを使用して通知を配信します。</span><span class="sxs-lookup"><span data-stu-id="b0513-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="b0513-106">通知を受信するプロセスごとに、MAPI は非表示ウィンドウに特別なメッセージを投稿します。</span><span class="sxs-lookup"><span data-stu-id="b0513-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="b0513-107">このメッセージの名前は、MAPIDEFS.H で定義されている定数 **szMAPINotificationMsg** です。</span><span class="sxs-lookup"><span data-stu-id="b0513-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="b0513-108">これらの通知は、非表示ウィンドウのウィンドウ プロシージャが **szMAPINotificationMsg メッセージを処理するときに受け取** ります。</span><span class="sxs-lookup"><span data-stu-id="b0513-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="b0513-109">通知が配信されるのを保証するには、この **szMAPINotificationMsg** メッセージを待機してディスパッチする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0513-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="b0513-110">これを実現するためのロジックを実装する場合は、かなり単純に実行できますが、MAPI には、処理をさらに簡単にする [HrDispatchNotifications](hrdispatchnotifications.md) と呼ばれる MAPI DLL へのエントリ ポイントが提供されます。</span><span class="sxs-lookup"><span data-stu-id="b0513-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="b0513-111">クライアント **で通知を受信するには、次のように HrDispatchNotifications** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b0513-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


