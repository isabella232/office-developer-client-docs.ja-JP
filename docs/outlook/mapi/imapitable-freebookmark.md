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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800838"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**適用されます**: Outlook 
  
ブックマークに関連付けられているメモリを解放します。
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameters

 _bkPosition_
  
> [in]解放するには、ブックマークは、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを呼び出すことによって作成されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ブックマークが正常に解放されました。
    
MAPI_E_INVALID_BOOKMARK 
  
> 指定されたブックマークは存在しません。
    
## <a name="remarks"></a>備考

**IMAPITable::FreeBookmark**メソッドでは、不要になったブックマークを解放します。 ブックマークは、この呼び出しの後は有効ではありません。 テーブルがメモリからリリースされる、すべての関連付けられているブックマークのも解放されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

呼び出し元では、 _bkPosition_パラメーターで次の 3 つの定義済みのブックマークの 1 つが成功した場合は、要求を無視して、S_OK を返します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

