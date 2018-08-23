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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c9197201388530bd7755eb1987ecc863220e3847
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566608"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ビットごとの**AND**演算を実行し、結果をテストするために使用されるビットマスクの制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Members

 **relBMR**
  
> プロパティ タグに**ulMask**のメンバーで指定されたマスクを適用する方法を説明する関係演算子です。 使用可能な値は次のとおりです。 
    
BMR_EQZ 
  
> 0 のテストと**ulPropTag**のメンバーによって表されるプロパティを使用して、 **ulMask**のメンバーで、マスクのビットごとの**AND**演算を実行します。 
    
BMR_NEZ 
  
> **UlMask**メンバーが 0 のテストと**ulPropTag**のメンバーによって表されるプロパティを使用してマスクのビットごとの**AND**演算を実行します。 
    
 **ulPropTag**
  
> ビット マスクを適用するプロパティのプロパティ タグです。
    
 **ulMask**
  
> **UlPropTag**によって識別されるプロパティに適用するビットマスクです。
    
## <a name="remarks"></a>注釈

**SBitMaskRestriction**構造体は、 **ulMask**のメンバーと**ulPropTag**のメンバーによって記述されたプロパティの値で説明するビットマスクを使用してビットごとの**AND**演算を実行します。 結果がゼロの場合は、BMR_EQZ が満たされます。 0 以外の場合は、プロパティの値を持つ**ulMask**、としてセットされている同じビットが少なくとも 1 つの場合、BMR_NEZ、満たされます。
  
**SBitMaskRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

