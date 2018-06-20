---
title: 通知を強制します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800091"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="2e690-103">通知を強制します。</span><span class="sxs-lookup"><span data-stu-id="2e690-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="2e690-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e690-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e690-105">サービス プロバイダーの使用の場合、 [IMAPISupport: IUnknown](imapisupportiunknown.md)通知は、MAPI の方法が非表示のウィンドウとその対応するウィンドウ プロシージャを使用して通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e690-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="2e690-106">各プロセスが通知を受信するには、MAPI は、非表示のウィンドウに特別なメッセージを投稿します。</span><span class="sxs-lookup"><span data-stu-id="2e690-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="2e690-107">このメッセージは、MAPIDEFS で定義されている定数**szMAPINotificationMsg**と呼ばれます。H.</span><span class="sxs-lookup"><span data-stu-id="2e690-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="2e690-108">非表示のウィンドウのウィンドウ プロシージャは、 **szMAPINotificationMsg**メッセージを処理するとき、これらの通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e690-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="2e690-109">通知が配信されることを保証するには、待ってから、この**szMAPINotificationMsg**のメッセージをディスパッチする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e690-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="2e690-110">これを達成するためのロジックを実装することを行うだけでかなりが、MAPI は MAPI DLL にエントリ ポイントがさらに簡単な処理を行うには、 [HrDispatchNotifications](hrdispatchnotifications.md)と呼ばれるを提供します。</span><span class="sxs-lookup"><span data-stu-id="2e690-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="2e690-111">クライアントに通知を受信するには、次のように**HrDispatchNotifications**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e690-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


