---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328931"
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
  
> 順番、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを呼び出すことによって作成された、解放されるブックマーク。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ブックマークが正常に解放されました。
    
MAPI_E_INVALID_BOOKMARK 
  
> 指定したブックマークが存在しません。
    
## <a name="remarks"></a>解説

**IMAPITable:: freebookmark**メソッドは、不要になったブックマークを解放します。 この呼び出しの後、ブックマークは無効になりました。 テーブルがメモリから解放されると、それに関連付けられているすべてのブックマークも解放されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

発信者が3つの定義済みブックマークのいずれかを_bkPosition_パラメーターに渡した場合は、要求を無視し、S_OK を返します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

