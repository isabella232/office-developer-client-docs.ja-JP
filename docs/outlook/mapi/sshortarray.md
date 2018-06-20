---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804010"
---
# <a name="sshortarray"></a>SShortArray

  
  
**適用されます**: Outlook 
  
PT_MV_SHORT の種類のプロパティを説明するために使用する符号なし整数値の配列が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>メンバー

 **あう**
  
> **Lpi**のメンバーが指す配列内の値の数です。 
    
 **lpi**
  
> 符号なし整数値の配列へのポインター。
    
## <a name="remarks"></a>備考

PT_MV_SHORT およびその他のプロパティの種類の詳細については、[プロパティの型](property-types.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

