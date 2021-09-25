---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 79ef39504d118ac7577fed789360a08bca043d3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624175"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトのプロパティの属性の一覧を含む。 
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> **aPropAttr メンバーのプロパティ属性の** 数。 
    
 **aPropAttr**
  
> プロパティ属性の配列。 属性の有効な値は次のとおりです。
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>注釈

**SPropAttrArray** 構造体は [、IPropData : IMAPIProp](ipropdataimapiprop.md)インターフェイスを実装するプロパティ データ オブジェクトによって使用されます。 また、MAPI の [IMAPIMessageSite : 構造化](imapimessagesiteiunknown.md) ストレージに基づく IUnknown の実装でも使用されます。 
  
## <a name="see-also"></a>関連項目



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI の構造](mapi-structures.md)

