---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800060"
---
# <a name="fbadrow"></a>FBadRow

  
  
**適用対象**: Outlook 
  
テーブル内の行を検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>パラメーター

 _lprow_
  
> [in]検証する行を識別する[SRow](srow.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定された行が有効ではありません。
    
FALSE 
  
> 指定した行が無効です。
    
## <a name="see-also"></a>関連項目



[FBadRowSet](fbadrowset.md)

