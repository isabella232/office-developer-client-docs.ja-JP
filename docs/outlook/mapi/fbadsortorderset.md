---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f051996cf6beb8b9a02889c9917eafa66e15c7d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567649"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メモリ割り当てを確認して並べ替え順序セットを検証します。 
  
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
  
> [in]検証する [並べ替え順序セットを識別する SSortOrderSet](ssortorderset.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した並べ替え順序セットが無効です。 
    
FALSE 
  
> 指定した並べ替え順序セットが有効です。
    
## <a name="remarks"></a>注釈

**FBadSortOrderSet** 関数を使用して [、IMAPITable::SortTable](imapitable-sorttable.md)メソッドなどの並べ替えメソッドの呼び出しを準備できます。 
  

