---
title: 通知を強制する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328099"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="fb7db-103">通知を強制する</span><span class="sxs-lookup"><span data-stu-id="fb7db-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="fb7db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb7db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb7db-105">サービスプロバイダーが[imapisupport:](imapisupportiunknown.md) notification 用に IUnknown メソッドを使用すると、MAPI は非表示ウィンドウと対応するウィンドウプロシージャを使用して通知を配信します。</span><span class="sxs-lookup"><span data-stu-id="fb7db-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="fb7db-106">各プロセスが通知を受信するには、MAPI が非表示のウィンドウに特別なメッセージを投稿します。</span><span class="sxs-lookup"><span data-stu-id="fb7db-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="fb7db-107">このメッセージは、mapidefs.h で定義されている定数**szMAPINotificationMsg**を使用して名前が付けられます。H.</span><span class="sxs-lookup"><span data-stu-id="fb7db-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="fb7db-108">これらの通知は、非表示のウィンドウのウィンドウプロシージャが**szMAPINotificationMsg**メッセージを処理するときに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7db-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="fb7db-109">通知が配信されることを保証するには、この**szMAPINotificationMsg**メッセージを待機してディスパッチする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7db-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="fb7db-110">これを実現するためのロジックを実装することは非常に簡単ですが、mapi は[HrDispatchNotifications](hrdispatchnotifications.md)と呼ばれる mapi DLL にエントリポイントを提供して、処理をさらに簡単にします。</span><span class="sxs-lookup"><span data-stu-id="fb7db-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="fb7db-111">クライアントで通知を受信するには、次のように**HrDispatchNotifications**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fb7db-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


