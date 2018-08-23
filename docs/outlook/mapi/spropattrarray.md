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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577682"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

