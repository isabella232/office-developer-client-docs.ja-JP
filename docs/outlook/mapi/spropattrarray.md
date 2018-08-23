---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803985"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**適用対象**: Outlook 
  
オブジェクトのプロパティの属性の一覧が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md)、 [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **あう**
  
> **APropAttr**メンバーのプロパティの属性の数。 
    
 **aPropAttr**
  
> プロパティの属性の配列。 属性の有効な値は次のとおりです。
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>注釈

**SPropAttrArray**構造体を使用して実装されているデータ オブジェクトのプロパティで、 [IPropData: IMAPIProp](ipropdataimapiprop.md)インタ フェースです。 MAPI の実装で使用されても[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)に基づいて構造化ストレージは。 
  
## <a name="see-also"></a>関連項目



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI の構造](mapi-structures.md)

