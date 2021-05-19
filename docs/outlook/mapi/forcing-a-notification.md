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
# <a name="forcing-a-notification"></a>通知の送信を行う

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーが [IMAPISupport : IUnknown](imapisupportiunknown.md) メソッドを通知に使用する場合、MAPI は非表示ウィンドウとそれに対応するウィンドウ プロシージャを使用して通知を配信します。 通知を受信するプロセスごとに、MAPI は非表示ウィンドウに特別なメッセージを投稿します。 このメッセージの名前は、MAPIDEFS.H で定義されている定数 **szMAPINotificationMsg** です。 
  
これらの通知は、非表示ウィンドウのウィンドウ プロシージャが **szMAPINotificationMsg メッセージを処理するときに受け取** ります。 通知が配信されるのを保証するには、この **szMAPINotificationMsg** メッセージを待機してディスパッチする必要があります。 これを実現するためのロジックを実装する場合は、かなり単純に実行できますが、MAPI には、処理をさらに簡単にする [HrDispatchNotifications](hrdispatchnotifications.md) と呼ばれる MAPI DLL へのエントリ ポイントが提供されます。 クライアント **で通知を受信するには、次のように HrDispatchNotifications** を呼び出します。 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


