---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb8c31f399c32b3e5ddeb16aa67efb94e2bcadce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600919"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ブックマークに関連付けられているメモリを解放します。
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>パラメーター

 _bkPosition_
  
> [in] [IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを呼び出して作成される、解放するブックマーク。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ブックマークが正常に解放されました。
    
MAPI_E_INVALID_BOOKMARK 
  
> 指定したブックマークが存在しません。
    
## <a name="remarks"></a>注釈

**IMAPITable::FreeBookmark** メソッドは、不要になったブックマークを解放します。 ブックマークは、この呼び出し後に無効になります。 テーブルがメモリから解放されると、関連付けられたブックマークもすべて解放されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

呼び出し元が  _bkPosition_ パラメーターで 3 つの定義済みのブックマークのいずれかを渡した場合は、要求を無視して、S_OK。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

