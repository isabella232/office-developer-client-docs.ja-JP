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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803812"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**適用対象**: Outlook 
  
論理**AND**演算を使用して制限のグループに参加するために使用、**および**制限について説明します。 
  
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
  
> **LpRes**メンバーが指す配列内の検索制限の数です。 
    
 **lpRes**
  
> 論理**AND**演算では、結合されている[SRestriction](srestriction.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

**SAndRestriction**の結果は、その子のすべての制約が TRUE と評価される場合は TRUE です。 子の制限は、FALSE に評価された場合は FALSE になります。 
  
制限の種類の説明については、ビルドし、および方法のサンプル コード[についての制限](about-restrictions.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

