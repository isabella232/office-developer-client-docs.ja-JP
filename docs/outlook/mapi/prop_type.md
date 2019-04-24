---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332761"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティタグのプロパティの種類を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 返されるプロパティの型を含む property タグ。
    
## <a name="remarks"></a>解説

**PROP_TYPE**マクロを使用して、プロパティの種類を調べることができます。 たとえば、PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) を呼び出すと、値 PT_BINARY が返されます。
  
すべてのプロパティタグには、下位ワード (ビット 0 ~ 15) のプロパティの種類と、上位ワード (ビット 16 ~ 31) のプロパティの識別子が含まれています。 **PROP_TYPE**マクロは、プロパティの型を抽出し、それをビット 0 ~ 15 の整数に設定して返します。 戻り値の残りのビットは0に設定されます。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

