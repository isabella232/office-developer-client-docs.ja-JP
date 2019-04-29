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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433284"
---
# <a name="forcing-a-notification"></a>通知を強制する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーが[imapisupport:](imapisupportiunknown.md) notification 用に IUnknown メソッドを使用すると、MAPI は非表示ウィンドウと対応するウィンドウプロシージャを使用して通知を配信します。 各プロセスが通知を受信するには、MAPI が非表示のウィンドウに特別なメッセージを投稿します。 このメッセージは、mapidefs.h で定義されている定数**szMAPINotificationMsg**を使用して名前が付けられます。H. 
  
これらの通知は、非表示のウィンドウのウィンドウプロシージャが**szMAPINotificationMsg**メッセージを処理するときに表示されます。 通知が配信されることを保証するには、この**szMAPINotificationMsg**メッセージを待機してディスパッチする必要があります。 これを実現するためのロジックを実装することは非常に簡単ですが、mapi は[HrDispatchNotifications](hrdispatchnotifications.md)と呼ばれる mapi DLL にエントリポイントを提供して、処理をさらに簡単にします。 クライアントで通知を受信するには、次のように**HrDispatchNotifications**を呼び出します。 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


