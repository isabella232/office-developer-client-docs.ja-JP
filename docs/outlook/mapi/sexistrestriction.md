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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803901"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**適用対象**: Outlook 
  
テーブル内の列として、特定のプロパティが存在するかどうかをテストするために既存の制限について説明します。 
  
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

## <a name="members"></a>Members

 **ulReserved1**
  
> 予約されています。0 にする必要があります。 
    
 **ulPropTag**
  
> プロパティ タグが各行の存在をテストするのには、列を識別します。
    
 **ulReserved2**
  
> 予約されています。0 にする必要があります。
    
## <a name="remarks"></a>注釈

既存の制限は、他の種類のプロパティとコンテンツの制限などのプロパティに関連する制限の意味のある結果を保証するために使用されます。 プロパティが含まれている制限が[IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)に渡され、プロパティが存在しない、制限の結果は定義されていません。 既存の制限のプロパティの制限を結合して**** 制限を作成すると、呼び出し元を正確な結果保証することができます。 
  
存在タイプ PT_OBJECT サブオブジェクトのプロパティを使用して制限を使用することはできません。 
  
**SExistRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

