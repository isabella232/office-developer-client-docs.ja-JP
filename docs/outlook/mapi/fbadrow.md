---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6edefa72e7410bbea1474c948c016f06c30d5f64
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576304"
---
# <a name="fbadrow"></a>FBadRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の行を検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>パラメーター

 _lprow_
  
> [in]検証する行を識別する [SRow](srow.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した行が無効です。
    
FALSE 
  
> 指定した行が有効です。
    
## <a name="see-also"></a>関連項目



[FBadRowSet](fbadrowset.md)

