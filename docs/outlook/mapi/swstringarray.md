---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68a90d4bcc0b52cfa312fcaa60add644ea835ce0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609488"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列型のプロパティを記述するために使用される文字列の配列をPT_MV_UNICODE。 
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> lppszW メンバーが指す配列 **内の文字列の** 数。 
    
 **lppszW**
  
> Null で終了した Unicode 文字文字列の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「プロパティPT_MV_UNICODE」 [を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

