---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344437"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティタグの配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md)、 [CbSPropTagArray](cbsproptagarray.md)、 [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cvalues**
  
> **aulPropTag**メンバーによって示される、配列内のプロパティタグの数。 
    
 **aulPropTag**
  
> プロパティタグの配列。
    
## <a name="remarks"></a>解説

property タグは、2つの部分で構成される32ビットの符号なし整数です。 
  
- 上位16ビットの識別子。
    
- ローオーダー16ビットの型。
    
識別子は、特定の範囲の数値です。 MAPI は、識別子の範囲を定義して、プロパティがどのように使用され、保持する責任者を示します。 MAPI は、Mapitags ヘッダーファイルでサポートされている各プロパティタグに対する制約を定義します。
  
この型は、プロパティの値の形式を示します。 MAPI は、mapidefs.h ヘッダーファイルでサポートされている各プロパティの種類に対して定数を定義します。 
  
プロパティタグとそのコンポーネントの詳細については、以下のいずれかのトピックを参照してください。 
  
[MAPI プロパティタグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)
  
単一値および複数値のプロパティの種類の完全な一覧については、付録、[プロパティの識別子と型](property-identifiers-and-types.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

