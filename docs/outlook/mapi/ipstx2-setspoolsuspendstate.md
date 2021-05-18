---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407516"
---
# <a name="ipstx2setspoolsuspendstate"></a>IPSTX2::SetSpoolSuspendState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
スプーラーの中断状態を設定します。
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a>パラメーター

 _ulState_
  
> [in]スプーラーを設定する状態。 これは、次のいずれかの値である必要があります。
    
 **SS_ACTIVE**
  
> 
    
 **SS_SUSPENDED**
  
> 
    
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)

