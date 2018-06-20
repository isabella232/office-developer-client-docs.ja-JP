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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803682"
---
# <a name="proptag"></a>PROP_TAG

**適用されます**: Outlook 
  
指定したプロパティの型と識別子を組み合わせることによって作成されたプロパティ タグを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parameters

_ulPropType_
  
> 新しいプロパティ タグのプロパティの型。
    
_ulPropID_
  
> 新しいプロパティ タグのプロパティの識別子です。
    
## <a name="remarks"></a>備考

**プロペラ\_タグ**マクロは型の_ulPropType_と_ulPropID_で指定されている識別子のプロパティのプロパティ タグを作成します。 たとえば、次のように、 **PROP_TAG**マクロを使用してエントリ識別子のプロパティ タグを作成できます。 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

PT_BINARY で、プロパティの型が返されるプロパティ タグの下位 16 ビットに含まれているし、上位 16 ビットが 0 xffff のプロパティ識別子を格納します。
  
プロパティ タグの詳細については、 [MAPI プロパティ タグ](mapi-property-tags.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

