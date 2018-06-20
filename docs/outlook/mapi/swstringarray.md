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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804061"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **あう**
  
> **LppszW**メンバーが指す配列内の文字列の数です。 
    
 **lppszW**
  
> Unicode 文字の null 終了文字列の配列へのポインター。
    
## <a name="remarks"></a>備考

PT_MV_UNICODE の詳細については、[プロパティの型](property-types.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

