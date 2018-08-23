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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803794"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**適用対象**: Outlook 
  
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

