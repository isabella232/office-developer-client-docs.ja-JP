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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421740"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン オブジェクトの現在の状態をオンラインまたはオフラインに設定します。
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]この呼び出しの動作を変更します。 サポートされている値を次に示します。
    
MAPIOFFLINE_FLAG_BLOCK
  
> _ulFlags をこの_ 値に設定すると、状態の変更が完了するまで **SetCurrentState** 呼び出しがブロックされます。 既定では、移行は非同期的に行います。 移行が非同期的に発生すると、変更が完了するまで、 **すべての SetCurrentState** 呼び **E_PENDINGが返** されます。 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> ブロックせずに現在の状態を設定します。
    
 _ulMask_
  
> [in]変更する状態の部分。 サポートされている唯一の値は、MAPIOFFLINE_STATE_OFFLINE_MASK。
    
 _ulState_
  
> [in]に変更する状態。 この値は、次の 2 つの値の 1 つである必要があります。
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _pReserved_
  
> このパラメーターは、内部Outlook使用するために予約され、サポートされていません。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> オフライン オブジェクトの状態が正常に変更されました。
    
E_PENDING
  
> これは、オフライン オブジェクトの状態が非同期的に変化している状態を示します。 これは、以前の **SetCurrentState** 呼び出しで _ulFlags_ が MAPIOFFLINE_FLAG_BLOCK に設定され、それ以降の **SetCurrentState** 呼び出しが非同期状態の変更が完了するまでこの値を返す場合に発生します。 
    
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[MAPI 定数](mapi-constants.md)

