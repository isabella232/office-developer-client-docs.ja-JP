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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570990"
---
# <a name="proptag"></a>PROP_TAG

**適用されます**: Outlook 2013 |Outlook 2016 
  
指定したプロパティの型と識別子を組み合わせることによって作成されたプロパティ タグを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>パラメーター

_ulPropType_
  
> 新しいプロパティ タグのプロパティの型。
    
_ulPropID_
  
> 新しいプロパティ タグのプロパティの識別子です。
    
## <a name="remarks"></a>注釈

**プロペラ\_タグ**マクロは型の_ulPropType_と_ulPropID_で指定されている識別子のプロパティのプロパティ タグを作成します。 たとえば、次のように、 **PROP_TAG**マクロを使用してエントリ識別子のプロパティ タグを作成できます。 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

PT_BINARY で、プロパティの型が返されるプロパティ タグの下位 16 ビットに含まれているし、上位 16 ビットが 0 xffff のプロパティ識別子を格納します。
  
プロパティ タグの詳細については、 [MAPI プロパティ タグ](mapi-property-tags.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [構造体に関連するマクロ](macros-related-to-structures.md)

