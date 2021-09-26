---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5fc5914f6af792bb59d8063e87ceb29ca0ccf8ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620941"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントが直ちに終了し、MAPI プロバイダーがデータ損失を防ぐために変更を保持する MAPI プロバイダーを示します。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI プロバイダーは、MAPI クライアントが直ちに終了する準備が整いました。 
    
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

