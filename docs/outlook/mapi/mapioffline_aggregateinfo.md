---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438163"
---
# <a name="mapioffline_aggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構造は [HrCreateOfflineObj で使用されます](hrcreateofflineobj.md)。 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> 構造体のサイズ。
    
 **pOuterObj**
  
> このオブジェクトが集計される IUnknown オブジェクトへのポインター。 これにより、QueryInterface 呼び出しが作成されたオブジェクトに渡されます。
    
 **pRefTrackRoot**
  
> NULL である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

