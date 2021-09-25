---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: df8b5dd061613b75627e6c1c9208efb81a531cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616755"
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

## <a name="members"></a>メンバー

 **ulSize**
  
> 構造体のサイズ。
    
 **pOuterObj**
  
> このオブジェクトが集計される IUnknown オブジェクトへのポインター。 これにより、QueryInterface 呼び出しが作成されたオブジェクトに渡されます。
    
 **pRefTrackRoot**
  
> NULL である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

