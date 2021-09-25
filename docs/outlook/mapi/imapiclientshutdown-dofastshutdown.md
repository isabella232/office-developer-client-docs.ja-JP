---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 531653f794b38fec68fac206963df04b55af20d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580028"
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

