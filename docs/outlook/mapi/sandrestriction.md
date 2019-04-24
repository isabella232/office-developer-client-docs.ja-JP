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
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344661"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
論理**and**演算を使用して制限のグループに参加するために使用される**and**制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cres**
  
> **lpres**メンバが指す、配列内の検索制限の数。 
    
 **lpres**
  
> 論理**AND**演算と組み合わせて使用される[srestriction](srestriction.md)構造体の配列へのポインター。 
    
## <a name="remarks"></a>解説

**SAndRestriction**の結果は、そのすべての子制限が true に評価された場合に true となります。 false と評価される子の制限がある場合は false です。 
  
制限の種類、それらを構築する方法、およびサンプルコードの詳細については、「[制限について](about-restrictions.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[SRestriction](srestriction.md)


[MAPI の構造](mapi-structures.md)

