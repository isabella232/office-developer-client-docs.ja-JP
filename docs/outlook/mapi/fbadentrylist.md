---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 333cbf047ebefd13c6da39f4d05ab349318d6ccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576297"
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

 _lpEntryList_
  
> [in]検証するエントリ識別子の配列を含む [ENTRYLIST](entrylist.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> リストされているエントリ識別子の 1 つ以上が無効です。 
    
FALSE 
  
> リストされているエントリ識別子はすべて有効です。
    
## <a name="remarks"></a>注釈

**FBadEntryList** 関数は、エントリ識別子リストが正しく生成されたかどうかを判断します。 無効な識別子の例は、メモリが正しく割り当てられていない識別子、または正しくないサイズの識別子です。 
  

