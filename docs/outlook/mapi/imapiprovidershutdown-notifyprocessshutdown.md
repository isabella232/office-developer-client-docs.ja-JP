---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405248"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントが高速シャットダウンを実行し、プロバイダーがデータ損失を防止するアクションを実行できるよう、MAPI プロバイダーに対して示します。
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI プロバイダーは、MAPI クライアントがシャットダウンするときにデータ損失を防止するアクションを実行しています。
    
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

