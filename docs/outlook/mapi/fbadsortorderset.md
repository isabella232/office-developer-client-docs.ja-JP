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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800041"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lpsos_
  
> [in]設定を検証する並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

TRUE 
  
> 指定した並べ替え順序の設定が正しくありません。 
    
FALSE 
  
> 有効では、指定した並べ替え順序を設定します。
    
## <a name="remarks"></a>備考

**FBadSortOrderSet**関数は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドのような並べ替えメソッドへの呼び出しの準備に使用できます。 
  

