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
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803986"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**適用対象**: Outlook 
  
プロパティ タグの配列が含まれています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md)、 [CbSPropTagArray](cbsproptagarray.md)、 [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **あう**
  
> **AulPropTag**メンバーで指定された配列内のプロパティ タグの数。 
    
 **aulPropTag**
  
> プロパティ タグの配列です。
    
## <a name="remarks"></a>注釈

プロパティ タグは、2 つの部分で構成される 32 ビット符号なし整数です。 
  
- 上位 16 ビットの識別子です。
    
- 下位 16 ビットのタイプです。
    
識別子は、特定の範囲内の数値です。 MAPI は、プロパティの使用および保守の責任者を記述する識別子の範囲を定義します。 MAPI では、Mapitags.h ヘッダー ファイルでサポートされているプロパティ タグのそれぞれの制約を定義します。
  
型は、プロパティの値の形式を示します。 MAPI では、Mapidefs.h ヘッダー ファイルでサポートされているプロパティの型のそれぞれの定数を定義します。 
  
プロパティ タグとそのコンポーネントの詳細については、次のトピックを参照してください。 
  
[MAPI プロパティ タグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの型の概要](mapi-property-type-overview.md)
  
単一値および複数値を持つプロパティの型の完全なリストは、[プロパティの識別子と型](property-identifiers-and-types.md)は、付録を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

