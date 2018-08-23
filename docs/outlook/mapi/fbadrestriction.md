---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800040"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**適用対象**: Outlook 
  
テーブルのビューを制限するために使用制限を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>パラメーター

 _lpres_
  
> [in]検証する制限を定義する[SRestriction](srestriction.md)構造体です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した制限、または 1 つ以上の subrestrictions では、が有効ではありません。 
    
FALSE 
  
> 指定された制限とそのすべての subrestrictions は、有効です。
    
## <a name="remarks"></a>注釈

制限を確認すると、特定の行、テーブルの行を検索する[IMAPITable::FindRow](imapitable-findrow.md)メソッドおよび[IMAPIContainer](imapicontainerimapiprop.md)のメソッドは、テーブルを制限するのには、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドの呼び出しで渡すことができます。コンテナー オブジェクトの制限を実行するインターフェイスです。 
  

