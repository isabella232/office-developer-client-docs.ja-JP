---
title: imapiprovidershutdowndofastshutdown
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322422"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi プロバイダーに対して、mapi クライアントが直ちに終了していることを示します。したがって、データ損失を防止するために mapi プロバイダーは変更を保持します。
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> mapi プロバイダーは、mapi クライアントが直ちに終了する準備ができています。 
    
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

