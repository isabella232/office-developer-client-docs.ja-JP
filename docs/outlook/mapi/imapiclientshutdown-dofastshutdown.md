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
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800444"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**適用されます**: Outlook 
  
MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI クライアントは、すぐに終了して、MAPI プロバイダーは、クライアントの終了の準備ができて読み込まれている MAPI プロバイダーに、MAPI サブシステムを示しています。
    
MAPI_E_NO_SUPPORT
  
> MAPI サブシステムは、クライアントの高速シャット ダウンをサポートしていません。
    
## <a name="remarks"></a>備考

MAPI クライアントの高速シャット ダウンからのデータの損失を避けるためには、MAPI クライアントが、MAPI サブシステムによって返される S_OK の結果に基づく[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と**IMAPIClientShutdown::DoFastShutdown**のメソッドを呼び出す必要があります。[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドです。 詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

