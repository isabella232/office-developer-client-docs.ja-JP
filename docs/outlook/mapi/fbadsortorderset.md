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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578578"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メモリの割り当てを確認し、設定の並べ替え順序を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>パラメーター

 _lpsos_
  
> [in]設定を検証する並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した並べ替え順序の設定が正しくありません。 
    
FALSE 
  
> 有効では、指定した並べ替え順序を設定します。
    
## <a name="remarks"></a>注釈

**FBadSortOrderSet**関数は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドのような並べ替えメソッドへの呼び出しの準備に使用できます。 
  

