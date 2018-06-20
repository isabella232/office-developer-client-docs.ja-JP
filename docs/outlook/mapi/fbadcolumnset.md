---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800043"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**適用されます**: Outlook 
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドへの後続の呼び出しにサービス ・ プロバイダーがテーブルの列の有効性の設定のテストを使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parameters

 _lpptaCols_
  
> [in]検証するテーブルの列を定義するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

TRUE 
  
> 指定された列セットを使用することはできません。 
    
FALSE 
  
> 指定した列のセットは、有効です。
    
## <a name="remarks"></a>備考

**FBadColumnSet**関数は、無効な型 PT_ERROR の列と列として有効な型 PT_NULL を扱います。 
  

