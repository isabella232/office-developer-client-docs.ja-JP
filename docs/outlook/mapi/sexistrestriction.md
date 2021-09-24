---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e2cf26b2e4388fac1432308df82ded911cf7501
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550037"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の列として特定のプロパティが存在するかどうかをテストするために使用される存在制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>メンバー

 **ulReserved1**
  
> 予約済み。は 0 である必要があります。 
    
 **ulPropTag**
  
> 各行に存在をテストする列を識別するプロパティ タグ。
    
 **ulReserved2**
  
> 予約済み。は 0 である必要があります。
    
## <a name="remarks"></a>注釈

存在制限は、プロパティやコンテンツ制限など、プロパティを含む他の種類の制限に対して意味のある結果を保証するために使用されます。 プロパティを含む制限が [IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow](imapitable-findrow.md) に渡され、プロパティが存在しない場合、制限の結果は未定義になります。 プロパティ制限と **存在** 制限を結合する AND 制限を作成することで、呼び出し元は正確な結果を保証できます。 
  
存在制限は、サブオブジェクトプロパティの種類が異なる場合はPT_OBJECT。 
  
**SExistRestriction** 構造の詳細については、「制限について [」を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

