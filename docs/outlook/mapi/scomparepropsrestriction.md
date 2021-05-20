---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440004"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**適用対象**: Outlook 2013 | Outlook 2016 
  
リレーショナル 演算子を使用して 2 つのプロパティをテストする比較プロパティ制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**relop**
  
> 2 つのプロパティを比較するために使用する関係演算子。 指定できる値は次のとおりです。
    
  - RELOP_GE: 比較は、大きいまたは等しい最初の値に基づいて行います。
      
  - RELOP_GT: 比較は、より大きい最初の値に基づいて行います。
      
  - RELOP_LE: 比較は、より小さいか等しい最初の値に基づいて行います。
      
  - RELOP_LT: 比較は、より小さい最初の値に基づいて行います。
      
  - RELOP_NE: 比較は、等しくない値に基づいて行います。
      
  - RELOP_RE: 比較は LIKE (正規表現) の値に基づいて行います。
      
  - RELOP_EQ: 比較は、等しい値に基づいて行います。
    
**ulPropTag1**
  
> 比較する最初のプロパティのプロパティ タグ。 
    
**ulPropTag2**
  
> 比較する 2 番目のプロパティのプロパティ タグ。
    
## <a name="remarks"></a>注釈

比較順序は  _(プロパティ タグ 1) (関係演算子) (プロパティ タグ 2) です_。 比較するプロパティは、同じ種類である必要があります。 さまざまな種類のプロパティを比較しようとすると、MAPI またはサービス プロバイダーは、構造がパラメーターとして渡される [IMAPITable](imapitableiunknown.md) メソッドからエラー値 MAPI_E_TOO_COMPLEX を返します。 
  
プロパティ値の比較の制限の結果は、プロパティの 1 つまたは両方が存在しない場合は未定義です。 クライアントがこのような制限に対して十分に定義された動作を必要とし、プロパティが存在するかどうかが分からない場合 (たとえば、テーブルの必須の列ではありません)、比較プロパティ制限に存在する制限を結合する **AND** 制限を作成する必要があります。 [SExistRestriction](sexistrestriction.md)構造体を使用して、存在制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。 
  
ulPropTag1 および **ulPropTag2** メンバーで指定されたプロパティは、サービス プロバイダーがサポートしている場合、複数値を指定できます。  
  
**SComparePropsRestriction** の構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。
  
## <a name="see-also"></a>関連項目

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

