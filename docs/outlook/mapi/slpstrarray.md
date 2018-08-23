---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572873"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PT_MV_STRING8 の種類のプロパティを説明するために使用する文字列値の配列が含まれています。
  
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

## <a name="members"></a>Members

 **あう**
  
> **LppszA**メンバーが指す配列内の値の数です。 
    
 **lppszA**
  
> 8 ビット文字の null 終了文字列の配列へのポインター。
    
## <a name="remarks"></a>注釈

PT_MV_STRING8 の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

