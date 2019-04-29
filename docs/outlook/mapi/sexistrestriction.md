---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418940"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のプロパティがテーブル内の列として存在するかどうかをテストするために使用される存在制限を記述します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
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
  
> 予約語0である必要があります。 
    
 **ulPropTag**
  
> 各行に存在するかどうかをテストする列を識別するプロパティタグ。
    
 **ulReserved2**
  
> 予約語0である必要があります。
    
## <a name="remarks"></a>注釈

存在する制限は、プロパティやコンテンツの制限など、プロパティに関連する他の種類の制限について有意義な結果を保証するために使用されます。 プロパティを含む制限が[IMAPITable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)に渡され、プロパティが存在しない場合、制限の結果は未定義となります。 プロパティ制限に参加する**と**制限が存在し、制限が存在することにより、発信者が正確な結果を保証できます。 
  
存在する制限は、PT_OBJECT 型のサブオブジェクトのプロパティでは使用できません。 
  
**sexistrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

