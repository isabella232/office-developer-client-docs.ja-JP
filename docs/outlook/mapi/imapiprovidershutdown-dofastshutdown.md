---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563472"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
示します MAPI プロバイダーに MAPI クライアントが、すぐに終了している MAPI プロバイダーがデータの損失を防ぐために加えられた変更を永続化できるようにします。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI プロバイダーを即座に終了するのには MAPI クライアントの準備ができました。 
    
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

