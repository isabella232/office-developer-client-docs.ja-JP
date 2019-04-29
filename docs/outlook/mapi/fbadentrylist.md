---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427774"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI エントリ識別子の一覧を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>パラメーター

 _lペン trylist_
  
> 順番検証するエントリ識別子の配列を含む[entrylist](entrylist.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> リストされている1つ以上のエントリ識別子が無効です。 
    
FALSE 
  
> リストされているすべてのエントリ識別子が有効である。
    
## <a name="remarks"></a>注釈

**fbadentrylist**関数は、エントリ id の一覧が正しく生成されているかどうかを判断します。 無効な識別子の例としては、メモリが正しく割り当てられていないか、または間違ったサイズの識別子があります。 
  

