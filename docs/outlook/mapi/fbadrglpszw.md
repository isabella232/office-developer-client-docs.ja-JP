---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d677c6d4e1eb416e5dabf466f24d9b77c48c03e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621116"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Unicode 文字列の配列内のすべての文字列を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>パラメーター

 _lppszW_
  
> [in]Null 終端 Unicode 文字列の配列へのポインター。 
    
 _cStrings_
  
> [in]lppszW パラメーターが指す配列  _内の文字列の_ 数。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した配列内の 1 つ以上の文字列が無効です。 
    
FALSE 
  
> 指定した配列内の文字列が有効です。
    

