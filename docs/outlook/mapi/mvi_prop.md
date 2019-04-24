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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326293"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティの MVI_FLAG を設定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連する構造:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>パラメーター

 _マーク_
  
> 変更するプロパティタグを指定します。
    
## <a name="remarks"></a>解説

MVI_FLAG は、MV_FLAG の設定を結合し、プロパティを複数値として識別し、MV_INSTANCE を複数の行のテーブルに複数値のプロパティを表示することを要求します。 影響を受けるプロパティのプロパティの種類は変更されますが、識別子は変更されません。 
  
たとえば、MVI_PROP マクロが PT_FLOAT 型のプロパティに適用されている場合、その型は PT_MV_FLOAT に変更されます。 テーブルに含まれている場合は、値ごとに1行のプロパティを表すために複数の行が使用されます。 その他の列のプロパティが繰り返されます。 
  
これらのフラグの詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」および「[複数値を持つ列の処理](working-with-multivalued-columns.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造に関連するマクロ](macros-related-to-structures.md)

