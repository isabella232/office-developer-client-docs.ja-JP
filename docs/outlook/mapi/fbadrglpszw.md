---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436441"
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
    

