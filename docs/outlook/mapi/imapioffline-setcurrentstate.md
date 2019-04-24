---
title: imapiofflinesetlevel
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321211"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフラインオブジェクトの現在の状態をオンラインまたはオフラインに設定します。
  
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
  
> 順番この呼び出しの動作を変更します。 サポートされている値を次に示します。
    
MAPIOFFLINE_FLAG_BLOCK
  
> _ulflags_をこの値に設定すると**** 、状態の変更が完了するまで setlevelcall がブロックされます。 既定では、移行は非同期的に行われます。 遷移が非同期で発生している**** 場合、すべての setcurrentstate 呼び出しは、変更が完了するまで**** を返します。 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> ブロックせずに現在の状態を設定します。
    
 _ulmask_
  
> 順番変更する状態の部分。 サポートされている値は MAPIOFFLINE_STATE_OFFLINE_MASK のみです。
    
 _ulstate_
  
> 順番変更後の状態。 次の2つの値のいずれかである必要があります。
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _保持され_
  
> このパラメーターは、Outlook の内部使用のために予約されており、サポートされていません。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> オフラインオブジェクトの状態が正常に変更されました。
    
E_PENDING
  
> これは、オフラインオブジェクトの状態が非同期に変化していることを示します。 これは、 _ulflags_が以前の setcurrentstate に設定**** されている場合に発生し、以降の**setcurrentstate**変更が完了するまでこの値が返されます。 
    
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[MAPI 定数](mapi-constants.md)

