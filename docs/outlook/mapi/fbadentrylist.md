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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800029"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**適用対象**: Outlook 
  
MAPI エントリの識別子の一覧を検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>パラメーター

 _lpEntryList_
  
> [in]検証するエントリの識別子の配列を含む[ENTRYLIST](entrylist.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 表示されたエントリの識別子の 1 つ以上が有効ではありません。 
    
FALSE 
  
> すべてのエントリが一覧表示されている識別子は、有効です。
    
## <a name="remarks"></a>注釈

**FBadEntryList**関数では、エントリの識別子] ボックスの一覧が正しく生成されたかどうかを判断します。 無効な識別子の例は、メモリが正しく割り当てられていないか、不適切なサイズの識別子のいずれかです。 
  

