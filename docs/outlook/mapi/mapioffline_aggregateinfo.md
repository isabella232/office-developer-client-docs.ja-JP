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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357135"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造体は、 [hrcreateofflineobj](hrcreateofflineobj.md)と共に使用されます。 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulsize**
  
> 構造体のサイズ。
    
 **pouterobj**
  
> このオブジェクトの集約先の IUnknown オブジェクトへのポインター。 これにより、作成されたオブジェクトに QueryInterface 呼び出しをパススルーすることができます。
    
 **pRefTrackRoot**
  
> NULL である必要があります。
    
## <a name="see-also"></a>関連項目



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

