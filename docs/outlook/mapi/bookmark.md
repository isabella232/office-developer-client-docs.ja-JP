---
title: ブックマーク
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799906"
---
# <a name="bookmark"></a>ブックマーク

  
  
**適用されます**: Outlook 
  
テーブル内の位置を記憶するためのブックマークのデータを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連する方法があります。  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>備考

MAPI には、以下のとおり、3 つのブックマークが定義されています。
  
BOOKMARK_BEGINNING 
  
> テーブルの開始位置を記憶します。 
    
BOOKMARK_CURRENT 
  
> テーブルの現在の位置を記憶します。
    
BOOKMARK_END 
  
> テーブルの末尾の位置を記憶します。
    
クライアントは、他のテーブルの位置を記憶するための他のブックマークを作成できます。 ブックマークは、テーブルが開いているときのみ有効です。 クライアントは、関連するテーブルを閉じる前に、作成したすべてのブックマークを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI データ型](mapi-data-types.md)

