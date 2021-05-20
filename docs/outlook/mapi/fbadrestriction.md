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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432241"
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
  

