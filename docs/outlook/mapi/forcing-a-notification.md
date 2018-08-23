---
title: 通知の強制
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578774"
---
# <a name="forcing-a-notification"></a>通知の強制

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーの使用の場合、 [IMAPISupport: IUnknown](imapisupportiunknown.md)通知は、MAPI の方法が非表示のウィンドウとその対応するウィンドウ プロシージャを使用して通知を提供します。 各プロセスが通知を受信するには、MAPI は、非表示のウィンドウに特別なメッセージを投稿します。 このメッセージは、MAPIDEFS で定義されている定数**szMAPINotificationMsg**と呼ばれます。H. 
  
非表示のウィンドウのウィンドウ プロシージャは、 **szMAPINotificationMsg**メッセージを処理するとき、これらの通知が表示されます。 通知が配信されることを保証するには、待ってから、この**szMAPINotificationMsg**のメッセージをディスパッチする必要があります。 これを達成するためのロジックを実装することを行うだけでかなりが、MAPI は MAPI DLL にエントリ ポイントがさらに簡単な処理を行うには、 [HrDispatchNotifications](hrdispatchnotifications.md)と呼ばれるを提供します。 クライアントに通知を受信するには、次のように**HrDispatchNotifications**を呼び出します。 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


