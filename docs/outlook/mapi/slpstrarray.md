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
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361153"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PT_MV_STRING8 型のプロパティを記述するために使用される文字列値の配列を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **lppszA**メンバーが指す配列内の値の数。 
    
 **lppszA**
  
> null で終了した8ビット文字の文字列の配列へのポインター。
    
## <a name="remarks"></a>解説

PT_MV_STRING8 の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

