---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438884"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
論理 AND 操作 **を使用** して制限のグループに参加するために使用される AND 制限について **説明** します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> **lpRes** メンバーが指す配列内の検索制限の数。 
    
 **lpRes**
  
> 論理 **AND** 操作と組み合わせる [SRestriction](srestriction.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

すべての子制限が TRUE に評価される場合 **、SAndRestriction** の結果は TRUE です。 子制限が FALSE と評価される場合は FALSE です。 
  
制限の種類、それらをビルドする方法、およびサンプル コードの説明については、「制限について [」を参照してください](about-restrictions.md)。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

