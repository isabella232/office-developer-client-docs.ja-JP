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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575099"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

## <a name="parameters"></a>パラメーター

 _lpptaCols_
  
> [in]検証するテーブルの列を定義するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定された列セットを使用することはできません。 
    
FALSE 
  
> 指定した列のセットは、有効です。
    
## <a name="remarks"></a>注釈

**FBadColumnSet**関数は、無効な型 PT_ERROR の列と列として有効な型 PT_NULL を扱います。 
  

