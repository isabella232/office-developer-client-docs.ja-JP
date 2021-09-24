---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5bc772a997b71a8adda3c11a1ac43ce1b7cee03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549995"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
型のプロパティを記述するために使用される文字列値の配列が含PT_MV_STRING8。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>メンバー

 **cValues**
  
> lppszA メンバーが指す配列 **内の値の** 数。 
    
 **lppszA**
  
> null-ended 8 ビット文字文字列の配列へのポインター。
    
## <a name="remarks"></a>注釈

プロパティの詳細については、「PT_MV_STRING8の [種類」を参照してください](property-types.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

