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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428460"
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
  

