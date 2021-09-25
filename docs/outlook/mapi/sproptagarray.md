---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd6d8f44b3de487750c28ba5919ab5adda0020b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566550"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ タグの配列を含む。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>メンバー

 **cValues**
  
> **aulPropTag** メンバーによって示される配列内のプロパティ タグの数。 
    
 **aulPropTag**
  
> プロパティ タグの配列。
    
## <a name="remarks"></a>注釈

プロパティ タグは、2 つの部分で構成される 32 ビットの符号なし整数です。 
  
- 高次 16 ビットの識別子。
    
- 低次 16 ビットの型。
    
識別子は、特定の範囲の数値です。 MAPI では、プロパティの使用および管理の責任者を示す識別子の範囲を定義します。 MAPI は、Mapitags.h ヘッダー ファイルでサポートする各プロパティ タグの制約を定義します。
  
型は、プロパティの値の形式を示します。 MAPI は、Mapidefs.h ヘッダー ファイルでサポートする各プロパティの種類の定数を定義します。 
  
プロパティ タグとそのコンポーネントの詳細については、次のいずれかのトピックを参照してください。 
  
[MAPI プロパティ のタグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)
  
単一値および複数値プロパティの種類の完全な一覧については、付録「プロパティ識別子と型」 [を参照してください](property-identifiers-and-types.md)。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

