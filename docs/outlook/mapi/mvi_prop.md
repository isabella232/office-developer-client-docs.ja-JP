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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801687"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**適用されます**: Outlook 
  
指定したプロパティの MVI_FLAG を設定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連の構造体。  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameters

 _タグ_
  
> 変更するプロパティ タグです。
    
## <a name="remarks"></a>備考

MVI_FLAG として、複数値を持つプロパティを識別する、MV_FLAG、MV_INSTANCE、複数の行のテーブルに、複数値を持つプロパティが表示されることを要求するの設定を結合します。 影響を受けるプロパティのプロパティの型が変更されたが、識別子は変更されません。 
  
などの PT_FLOAT の種類のプロパティには、MVI_PROP マクロを適用するときは、その型が PT_MV_FLOAT に変更されます。 、テーブルに含まれるときは、複数の行を使用して値ごとに 1 つの行のプロパティを表します。 他の列のプロパティが繰り返されます。 
  
これらのフラグの詳細については、 [MAPI プロパティの型の概要](mapi-property-type-overview.md)」および「[複数値を持つ列の使用](working-with-multivalued-columns.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)


[構造体に関連するマクロ](macros-related-to-structures.md)

