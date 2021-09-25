---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e1d1f759989ae7c241317b7488ce0d8f53180e9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609636"
---
# <a name="prop_tag"></a>PROP_TAG

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティの種類と識別子を組み合わせて作成されたプロパティ タグを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>パラメーター

_ulPropType_
  
> 新しいプロパティ タグのプロパティの種類。
    
_ulPropID_
  
> 新しいプロパティ タグのプロパティ識別子。
    
## <a name="remarks"></a>注釈

**PROP \_ TAG マクロ** は、ulPropType 型のプロパティと _、ulPropID_ で指定された識別子のプロパティ タグ _を作成します_。 たとえば、エントリ識別子のプロパティ タグを作成するには、次のように、PROP_TAG **マクロを** 使用します。 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

返されるプロパティ タグの低次 16 ビットには、プロパティの種類 PT_BINARY、および高次 16 ビットにはプロパティ識別子 0xFFFF が含0xFFFF。
  
プロパティ タグの詳細については、「MAPI プロパティ タグ [」を参照してください](mapi-property-tags.md)。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

