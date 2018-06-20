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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803684"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**適用されます**: Outlook 
  
指定されたプロパティ タグのプロパティの型を返します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> プロパティ タグを取得するプロパティの型が含まれています。
    
## <a name="remarks"></a>備考

プロパティの種類を調べるには、 **PROP_TYPE**マクロを使用できます。 PT_BINARY が返される値の PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) の結果を呼び出すなどです。
  
プロパティのすべてのタグには、下位ワード (ビット 0 ~ 15) のプロパティの型と、上位ワード (16 ~ 31 のビット) のプロパティの識別子が含まれています。 **PROP_TYPE**マクロは、プロパティの型を抽出し返される整数の 15 からビット 0 に配置します。 戻り値の残りのビットは、0 に設定されます。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造体に関連するマクロ](macros-related-to-structures.md)

