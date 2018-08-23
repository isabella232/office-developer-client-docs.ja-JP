---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581224"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
時刻の値の配列が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **あう**
  
> **Lpat**のメンバーが指す配列内の値の数です。 
    
 **lpat**
  
> アプリケーションの時刻の値の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SAppTimeArray**構造体を使用して、PT_MV_APPTIME の種類のプロパティを定義します。 PT_MV_APPTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

