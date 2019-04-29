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
  
リレーションシップ演算子を使用して2つのプロパティをテストする compare プロパティ制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>メンバー

**relop**
  
> 2つのプロパティを比較するために使用するリレーショナル演算子です。 可能な値は次のとおりです。
    
  - RELOP_GE: 比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。
      
  - RELOP_GT: 比較は、より大きな最初の値に基づいて行われます。
      
  - RELOP_LE: 比較は、最初の値よりも小さいか等しいかに基づいて行われます。
      
  - RELOP_LT: 比較は、小さい方の値に基づいて行われます。
      
  - RELOP_NE: 比較は、等しくない値に基づいて行われます。
      
  - RELOP_RE: 比較は、LIKE (正規表現) の値に基づいて行われます。
      
  - RELOP_EQ: 比較は同じ値に基づいて行われます。
    
**ulPropTag1**
  
> 比較する最初のプロパティのプロパティタグ。 
    
**ulPropTag2**
  
> 比較する2番目のプロパティのプロパティタグ。
    
## <a name="remarks"></a>注釈

比較順序は _(プロパティタグ 1) (リレーショナル演算子) (プロパティタグ 2)_ です。 比較するプロパティは同じ型でなければなりません。 さまざまな種類のプロパティを比較しようとすると、MAPI またはサービスプロバイダーは、構造体がパラメーターとして渡される[IMAPITable](imapitableiunknown.md)メソッドからエラー値 MAPI_E_TOO_COMPLEX を返します。 
  
プロパティの一方または両方が存在しない場合、比較プロパティ値の制限の結果は未定義です。 クライアントでこのような制限に対して適切に定義された動作が必要であり、プロパティが存在するかどうかがわからない (たとえば、テーブルの必須の列**** ではない) 場合は、compare プロパティ制限を既存の値で結合するための制限を作成する必要があります。条件. [sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、存在制限と[SAndRestriction](sandrestriction.md)構造を定義します。 
  
サービスプロバイダーがサポートしている場合、 **ulPropTag1**メンバーと**ulPropTag2**メンバーで指定されたプロパティは複数値になることができます。 
  
**scomparepropsrestriction**構造と一般的な制限事項の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。
  
## <a name="see-also"></a>関連項目

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

