---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410680"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティMVI_FLAGを設定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>パラメーター

 _tag_
  
> 変更するプロパティ タグ。
    
## <a name="remarks"></a>注釈

MVI_FLAGは、MV_FLAG の設定を組み合わせ、プロパティを複数値として識別し、MV_INSTANCE を組み合わせ、複数の値を持つプロパティを複数行のテーブルに表示します。 影響を受けるプロパティのプロパティの種類は変更されますが、識別子は変更されません。 
  
たとえば、MVI_PROP マクロが PT_FLOAT 型のプロパティに適用されると、その型は PT_MV_FLOAT に変更PT_MV_FLOAT。 テーブルに含まれる場合は、値ごとに 1 行のプロパティを表す複数の行が使用されます。 他の列のプロパティが繰り返されます。 
  
これらのフラグの詳細については [、「MAPI プロパティの種類](mapi-property-type-overview.md) の概要」および「複数値列の [操作」を参照してください](working-with-multivalued-columns.md)。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

