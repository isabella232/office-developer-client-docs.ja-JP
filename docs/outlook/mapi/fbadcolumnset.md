---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1498705c0459798f1ae8c49586423603500c6e8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601003"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドへの後続の呼び出しで、サービス プロバイダーが使用するテーブル列セットの有効性をテストします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>パラメーター

 _lpptaCols_
  
> [in]検証するテーブル列を定義するプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した列セットが無効です。 
    
FALSE 
  
> 指定した列セットが有効です。
    
## <a name="remarks"></a>注釈

**FBadColumnSet** 関数は、データ型の列を無効PT_ERROR、型の列が有効PT_NULL扱います。 
  

