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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340958"
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
  
> 順番検証する行を識別する[srow](srow.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した行は無効です。
    
FALSE 
  
> 指定した行は有効です。
    
## <a name="see-also"></a>関連項目



[FBadRowSet](fbadrowset.md)

