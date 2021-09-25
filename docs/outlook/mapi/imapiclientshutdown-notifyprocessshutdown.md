---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 88512a6e55bc550e717dae4fda0ca41fce09d221
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571823"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
シャットダウンを続行する MAPI クライアントの意図を示します。
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI サブシステムは、読み込まれた MAPI プロバイダーに対して、MAPI クライアントが高速シャットダウンを実行する場合に通知を試みた。
    
## <a name="remarks"></a>注釈

MAPI クライアントの高速シャットダウンによるデータ損失を回避するために、MAPI クライアントは **IMAPIClientShutdown::NotifyProcessShutdown** メソッドと IMAPIClientShutdown::D oFastShutdown メソッドを [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドの MAPI サブシステムによって返される S_OK 結果に基づいて呼び出す必要があります。 [](imapiclientshutdown-dofastshutdown.md) 詳細については、「高速シャットダウン [のベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

