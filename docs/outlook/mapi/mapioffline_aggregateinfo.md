---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801504"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**適用されます**: Outlook 
  
[HrCreateOfflineObj](hrcreateofflineobj.md)構造体が使用されます。 
  
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
  
> 構造体のサイズです。
    
 **pOuterObj**
  
> 先この集約オブジェクトの IUnknown オブジェクトへのポインター。 こうと、作成したオブジェクトを通過するすべての QueryInterface 呼び出しができます。
    
 **pRefTrackRoot**
  
> NULL である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

