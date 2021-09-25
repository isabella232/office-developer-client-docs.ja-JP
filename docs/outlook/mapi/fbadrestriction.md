---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b91c33e237af2dc5da3d24961192fff88e64223f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605000"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル ビューを制限するために使用される制限を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>パラメーター

 _lpres_
  
> [in]検証 [する制限を定義する SRestriction](srestriction.md) 構造。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定された制限、または 1 つ以上のサブ制限が無効です。 
    
FALSE 
  
> 指定された制限とそのすべてのサブ制限が有効です。
    
## <a name="remarks"></a>注釈

制限が検証された後 [、IMAPITable::Restrict](imapitable-restrict.md) メソッドへの呼び出しで渡して、テーブルを特定の行に制限し [、IMAPITable::FindRow](imapitable-findrow.md) メソッドでテーブル行を検索し [、IMAPIContainer](imapicontainerimapiprop.md) インターフェイスのメソッドに渡してコンテナー オブジェクトに対する制限を実行できます。 
  

