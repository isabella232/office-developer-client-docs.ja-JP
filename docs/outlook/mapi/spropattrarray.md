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
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358115"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトのプロパティの属性の一覧が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md)、 [cbspro trarray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **apropattr**メンバーのプロパティ属性の数。 
    
 **apropattr**
  
> プロパティ属性の配列。 属性の有効な値は次のとおりです。
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>解説

**sproな trarray**構造体は、 [ipropdata: imapiprop](ipropdataimapiprop.md)インターフェイスを実装するプロパティデータオブジェクトによって使用されます。 また、構造化ストレージに基づく[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)の MAPI 実装でも使用されます。 
  
## <a name="see-also"></a>関連項目



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI の構造](mapi-structures.md)

