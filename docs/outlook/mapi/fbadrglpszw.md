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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800036"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**適用対象**: Outlook 
  
Unicode 文字列の配列内のすべての文字列を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>パラメーター

 _lppszW_
  
> [in]Null で終わる Unicode 文字列の配列へのポインター。 
    
 _cStrings_
  
> [in]_LppszW_パラメーターが指す配列内の文字列の数です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 1 つ以上の指定した配列内の文字列が有効ではありません。 
    
FALSE 
  
> 指定した配列内の文字列は、有効です。
    

