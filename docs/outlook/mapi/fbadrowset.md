---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 241441c1aa516b366fdecd6c17f5d12cf12a2206
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630930"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一連のテーブル行に含まれるすべてのテーブル行を検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>パラメーター

 _lpRowSet_
  
> [in]検証する [行セットを識別する SRowSet](srowset.md) 構造体へのポインター。 ポインターが NULL の場合、構造は無効です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した行セットの行が無効であるか、行セット自体が無効です。 
    
FALSE 
  
> 指定した行セットと行セット自体の行はすべて有効です。
    
## <a name="see-also"></a>関連項目



[FBadRow](fbadrow.md)

