---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8459e21becc85e3bee0603d5d8ade7f44ddee712
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550135"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビットワイズ AND 操作を実行し、結果をテストするために使用されるビットマスク制限について説明します。 
  
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

## <a name="members"></a>メンバー

 **relBMR**
  
> **ulMask** メンバーで指定されたマスクをプロパティ タグに適用する方法を説明する関係演算子。 指定できる値は次のとおりです。 
    
BMR_EQZ 
  
> **ulPropTag** メンバーで表されるプロパティを使用して **、ulMask** メンバー内のマスクのビット分割 **AND** 操作を実行し、ゼロに等しいかテストします。 
    
BMR_NEZ 
  
> **ulPropTag** メンバーで表されるプロパティを使用して **、ulMask** メンバー内のマスクのビット分割 **AND** 操作を実行し、ゼロに等しくないかテストします。 
    
 **ulPropTag**
  
> ビットマスクが適用されるプロパティのプロパティ タグ。
    
 **ulMask**
  
> ulPropTag で識別されるプロパティに適用する **ビットマスク**。
    
## <a name="remarks"></a>注釈

**SBitMaskRestriction** 構造体は、ulMaskメンバーで説明されているビットマスクと **、ulPropTag** メンバーによって記述されるプロパティの値を使用してビット演算を実行します。  結果が 0 の場合は、BMR_EQZが満たされます。 0 以外の場合、つまり、プロパティ値に少なくとも 1 つの同じビットが **ulMask** として設定されている場合、BMR_NEZ満たされます。
  
**SBitMaskRestriction** 構造と制限全般の詳細については、「制限について [」を参照してください](about-restrictions.md)。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

