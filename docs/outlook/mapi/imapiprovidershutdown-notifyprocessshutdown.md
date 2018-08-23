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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592053"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI プロバイダーをプロバイダーは、データ損失を防ぐための処置を行うことができるように、高速シャット ダウンを行う MAPI クライアントを送信することを示します。
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI プロバイダーがアクションを実行して、MAPI クライアントのシャット ダウン時にデータ損失を防止します。
    
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

