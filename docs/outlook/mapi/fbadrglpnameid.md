---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434831"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前付きプロパティを記述する構造体の配列を検証し、割り当てを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>パラメーター

 _lppNameId_
  
> [in]名前付きプロパティを記述 [する MAPINAMEID](mapinameid.md) 構造体の配列へのポインター。 
    
 _cNames_
  
> [in]  _lppNameId_ パラメーターが指す配列内の名前付きプロパティ構造の数。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティ名構造体の 1 つ以上が無効です。 
    
FALSE 
  
> 指定したプロパティ名の構造はすべて有効です。
    
## <a name="remarks"></a>注釈

**FBadRglpNameID** 関数は [、IMAPIProp:::GetIDsFromNames](imapiprop-getidsfromnames.md)または [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)への呼び出しを設定するときに使用できます。 
  

