---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567140"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オフライン オブジェクトをオンラインまたはオフラインの現在の状態を設定します。
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]この呼び出しの動作を変更します。 サポートされている値は次のとおりです。
    
MAPIOFFLINE_FLAG_BLOCK
  
> _UlFlags_をこの値に設定する場合は、状態の変更が完了するまで、 **SetCurrentState**の呼び出しがブロックされます。 トランジションは、既定で非同期的に配置します。 移行は、非同期的に発生している、 **SetCurrentState**のすべての呼び出しは、変更が完了するまでには**E_PENDING**を返します。 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> ブロックすることがなく現在の状態を設定します。
    
 _ulMask_
  
> [in]変更の状態の一部です。 唯一のサポートされている値は、MAPIOFFLINE_STATE_OFFLINE_MASK です。
    
 _ulState_
  
> [in]状態に変更します。 これら 2 つの値のいずれかを指定する必要があります。
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _保持_
  
> このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> オフラインのオブジェクトの状態が正常に変更されました。
    
E_PENDING
  
> これは、オフラインのオブジェクトの状態が非同期的に変化していることを示します。 _UlFlags_は、呼び出しでは、以前**SetCurrentState** MAPIOFFLINE_FLAG_BLOCK に設定されており、非同期状態の変更が完了するまで、後続の**SetCurrentState**呼び出しでこの値を返すが場合です。 
    
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[MAPI �萔](mapi-constants.md)

