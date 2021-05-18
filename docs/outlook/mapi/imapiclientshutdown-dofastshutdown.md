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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408685"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントがクライアント プロセスを直ちに終了する意図を示します。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI サブシステムは、MAPI クライアントが直ちに終了し、MAPI プロバイダーがクライアント出口の準備ができていることを読み込んだ MAPI プロバイダーに示しています。
    
MAPI_E_NO_SUPPORT
  
> MAPI サブシステムでは、クライアントの高速シャットダウンはサポートされていません。
    
## <a name="remarks"></a>注釈

MAPI クライアントの高速シャットダウンによるデータ損失を回避するために、MAPI クライアントは[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドと IMAPIClientShutdown::D oFastShutdown メソッドを[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドの MAPI サブシステムによって返される S_OK 結果に基づいて呼び出す必要があります。  詳細については、「高速シャットダウン [のベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

