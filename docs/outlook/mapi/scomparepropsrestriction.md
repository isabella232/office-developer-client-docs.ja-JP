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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803832"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**適用対象**: Outlook 
  
リレーショナル演算子を使用して 2 つのプロパティをテストする比較プロパティの制限について説明します。 
  
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
  
> 2 つのプロパティを比較に使用する関係演算子です。 使用可能な値は次のとおりです。
    
  - RELOP_GE: 比較を行うベースの最初の値が大きいか等しい。
      
  - RELOP_GT: 比較を行うベースの最初の値が大きい。
      
  - RELOP_LE: 比較を行うに基づいて最初の値が同等またはそれ以下にします。
      
  - RELOP_LT: 比較を行うベースの最初の値が小さい方です。
      
  - RELOP_NE: 比較を行うベースの値が等しくないです。
      
  - RELOP_RE: 比較を (正規表現) の値などを基に行われます。
      
  - RELOP_EQ: 比較で行われるベースの値に等しい。
    
**ulPropTag1**
  
> 比較する最初のプロパティのプロパティ タグです。 
    
**ulPropTag2**
  
> 比較する 2 番目のプロパティのプロパティ タグです。
    
## <a name="remarks"></a>注釈

比較の順序は、 _(1) (関係演算子) のプロパティ タグ (プロパティ タグ 2)_。 比較するプロパティは、同じ型でなければなりません。 構造体はパラメーターとして渡す[IMAPITable](imapitableiunknown.md)メソッドからエラー値 MAPI_E_TOO_COMPLEX を取得するには、MAPI またはサービス プロバイダーは、さまざまな種類のプロパティを比較しようとしています。 
  
プロパティの一方または両方が存在しない場合、比較のプロパティ値の制限の結果は定義されていません。 クライアントなどの制限について明確に定義された動作を必要とし、ないときことを確認して、プロパティが存在するかどうか (たとえばは必要なテーブルの列) と、既存の比較プロパティの制限に参加する**と**制限を作成する必要があります制限です。 [SExistRestriction](sexistrestriction.md)構造体を使用すると、既存の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。 
  
**UlPropTag1**と**ulPropTag2**のメンバーで指定されたプロパティは、サービス プロバイダーがサポートしている場合、複数値を持つことができます。 
  
**SComparePropsRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

