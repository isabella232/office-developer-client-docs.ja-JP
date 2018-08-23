---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568204"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オフライン オブジェクトの現在のオンラインまたはオフラインの状態を取得します。
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>パラメーター

 _pulState_
  
> [out]オンラインまたはオフラインの現在の状態がオフラインのオブジェクトです。 これら 2 つの値のいずれかを指定する必要があります。
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[MAPI �萔](mapi-constants.md)

