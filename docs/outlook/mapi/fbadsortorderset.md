---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336975"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリの割り当てを確認して、設定された並べ替え順序を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>パラメーター

 _lpsos_
  
> 順番検証するように設定されている並べ替え順序を識別する、 [ssortorderset](ssortorderset.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定された並べ替え順序セットが無効です。 
    
FALSE 
  
> 指定された並べ替え順序の設定は有効です。
    
## <a name="remarks"></a>解説

**fbadsortorderset**関数を使用して、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドなどの sort メソッドの呼び出しを準備できます。 
  

