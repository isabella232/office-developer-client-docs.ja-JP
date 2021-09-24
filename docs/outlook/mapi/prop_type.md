---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5c31622e99079dc7c27d28d95aa26ecd5ac5689f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550184"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティ タグのプロパティの種類を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 返されるプロパティの種類を含むプロパティ タグ。
    
## <a name="remarks"></a>注釈

プロパティ **PROP_TYPE** マクロを使用して、プロパティの種類を特定できます。 たとえば、呼び出PROP_TYPE **(** PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md))) は、返される値PT_BINARYします。
  
すべてのプロパティ タグには、低次ワード (ビット 0 ~ 15) のプロパティ型と、高次ワード (ビット 16 ~ 31) のプロパティ識別子が含まれる。 この **PROP_TYPE** は、プロパティの種類を抽出し、返される整数のビット 0 ~ 15 に格納します。 戻り値の残りのビットは 0 に設定されます。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

