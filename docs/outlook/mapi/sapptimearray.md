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
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331697"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
時刻の値の配列を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lpat**メンバーが指す配列内の値の数。 
    
 **lpat**
  
> アプリケーション時間の値の配列へのポインター。 
    
## <a name="remarks"></a>解説

**SAppTimeArray**構造体は、PT_MV_APPTIME 型のプロパティを定義するために使用されます。 PT_MV_APPTIME の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

