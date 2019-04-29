---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424477"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビット単位の**and**演算を実行し、結果をテストするために使用されるビットマスク制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>メンバー

 **relbmr**
  
> **ulmask**メンバーで指定されたマスクを property タグに適用する方法を記述するリレーショナル演算子です。 可能な値は次のとおりです。 
    
BMR_EQZ 
  
> **ulPropTag**メンバーによって表されるプロパティを使用して、 **ulmask**メンバーのマスクのビット単位の**and**演算を実行し、0と等しいことをテストします。 
    
BMR_NEZ 
  
> **ulPropTag**メンバーによって表されるプロパティを使用して**ulmask**メンバーのマスクのビット単位の**and**演算を実行し、0と等しくないことをテストします。 
    
 **ulPropTag**
  
> ビットマスクを適用するプロパティのプロパティタグ。
    
 **ulmask**
  
> **ulPropTag**によって識別されるプロパティに適用するビットマスク。
    
## <a name="remarks"></a>注釈

**sbitmaskrestriction**構造体は、 **ulmask**メンバーで記述されたビットマスクと**ulPropTag**メンバーによって記述されたプロパティの値を使用して、ビット単位の**and**演算を実行します。 result が0の場合は、BMR_EQZ が満たされています。 0以外の場合、つまり、プロパティ値に**ulmask**として設定されている同じビットが少なくとも1つある場合、BMR_NEZ は満たされています。
  
一般的な**sbitmaskrestriction**構造体と制限事項の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

