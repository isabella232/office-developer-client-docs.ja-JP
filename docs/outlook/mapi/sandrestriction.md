---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c31fb0a70dc2458f4db62135d6b371996e2b5dab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599103"
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

## <a name="members"></a>メンバー

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

