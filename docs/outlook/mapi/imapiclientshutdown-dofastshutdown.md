---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 41c4ee65ce6ae8f2e0d978f1e2bd95adb4f5872a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575176"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI クライアントは、すぐに終了して、MAPI プロバイダーは、クライアントの終了の準備ができて読み込まれている MAPI プロバイダーに、MAPI サブシステムを示しています。
    
MAPI_E_NO_SUPPORT
  
> MAPI サブシステムは、クライアントの高速シャット ダウンをサポートしていません。
    
## <a name="remarks"></a>注釈

MAPI クライアントの高速シャット ダウンからのデータの損失を避けるためには、MAPI クライアントが、MAPI サブシステムによって返される S_OK の結果に基づく[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と**IMAPIClientShutdown::DoFastShutdown**のメソッドを呼び出す必要があります。[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドです。 詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

