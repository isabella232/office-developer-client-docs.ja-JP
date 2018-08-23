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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568267"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

