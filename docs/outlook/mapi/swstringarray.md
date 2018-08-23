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
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581357"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PT_MV_UNICODE の種類のプロパティを説明するために使用する文字の文字列の配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **あう**
  
> **LppszW**メンバーが指す配列内の文字列の数です。 
    
 **lppszW**
  
> Unicode 文字の null 終了文字列の配列へのポインター。
    
## <a name="remarks"></a>注釈

PT_MV_UNICODE の詳細については、[プロパティの型](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

