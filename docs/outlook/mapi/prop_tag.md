---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425884"
---
# <a name="proptag"></a>PROP_TAG

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティの種類と識別子を結合して作成されたプロパティタグを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>パラメーター

_ulproptype_
  
> 新しいプロパティタグのプロパティの種類。
    
_ulpropid_
  
> 新しいプロパティタグのプロパティ識別子。
    
## <a name="remarks"></a>注釈

**PROP\_タグ**マクロは、 _ulproptype_型のプロパティと_ulpropid_で指定された識別子のプロパティタグを作成します。 たとえば、エントリ識別子のプロパティタグは、次のように**PROP_TAG**マクロを使用して作成できます。 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

返される property タグの下位16ビットには、プロパティの型 PT_BINARY が含まれており、上位16ビットにはプロパティ識別子の0xffff が含まれています。
  
プロパティタグの詳細については、「 [MAPI プロパティタグ](mapi-property-tags.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [構造に関連するマクロ](macros-related-to-structures.md)

