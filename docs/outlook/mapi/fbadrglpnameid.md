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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588147"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
名前付きプロパティを記述する構造体の配列を検証し、その割り当てを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>パラメーター

 _lppNameId_
  
> [in]名前付きプロパティを記述する[MAPINAMEID](mapinameid.md)構造体の配列へのポインター。 
    
 _Cname_
  
> [in]_LppNameId_パラメーターが指す配列内の名前付きプロパティの構造体の数です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 1 つ以上の指定したプロパティの名前の構造体が有効ではありません。 
    
FALSE 
  
> 指定したプロパティの名前の構造体は、すべて有効です。
    
## <a name="remarks"></a>注釈

[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)または[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)への呼び出しをセットアップするとき、 **FBadRglpNameID**関数を使用できます。 
  

