---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349554"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_UNICODE 型のプロパティを記述するために使用される文字列の配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lppszw**メンバーによって示される配列内の文字列の数。 
    
 **lppszw**
  
> null で終了する Unicode 文字列の配列へのポインター。
    
## <a name="remarks"></a>解説

PT_MV_UNICODE の詳細については、「[プロパティの種類](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

