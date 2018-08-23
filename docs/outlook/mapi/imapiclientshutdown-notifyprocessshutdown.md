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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 04a9b631c3a4f33282bce44e06d92e089349c76b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800438"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**適用対象**: Outlook 
  
続行するのには MAPI クライアントの意図をシャット ダウンを示します。
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI サブシステムは、MAPI プロバイダーが読み込まれている MAPI クライアントが高速シャット ダウンを実行しようとしていることを通知しようとしています。
    
## <a name="remarks"></a>注釈

MAPI クライアントの高速シャット ダウンからのデータの損失を避けるためには、MAPI クライアントが、MAPI サブシステムによって返される S_OK の結果に基づく**IMAPIClientShutdown::NotifyProcessShutdown**と[IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md)のメソッドを呼び出す必要があります。[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドです。 詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

