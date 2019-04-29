---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438870"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
シャットダウンを続行する MAPI クライアントの意図を示します。
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> mapi サブシステムは、読み込み済みの mapi プロバイダーに、mapi クライアントが高速シャットダウンを行うことになることを通知しようとしました。
    
## <a name="remarks"></a>注釈

mapi クライアントの高速シャットダウンからのデータ損失を回避するために、mapi クライアントは、 **IMAPIClientShutdown:: notifyprocessshutdown**および[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出す必要があります。これは、次の mapi サブシステムによって返される S_OK 結果に基づいています。[IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッド。 詳細については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

