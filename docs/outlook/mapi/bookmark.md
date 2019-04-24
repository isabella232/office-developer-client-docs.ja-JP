---
title: BOOKMARK
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318040"
---
# <a name="bookmark"></a><span data-ttu-id="a0ece-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="a0ece-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="a0ece-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ece-105">テーブル内の位置を記憶するためのブックマークデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="a0ece-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0ece-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a0ece-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0ece-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0ece-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0ece-108">関連するメソッド:</span><span class="sxs-lookup"><span data-stu-id="a0ece-108">Related methods:</span></span>  <br/> |<span data-ttu-id="a0ece-109">[IMAPITable:: createbookmark](imapitable-createbookmark.md)[IMAPITable:: freebookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="a0ece-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="a0ece-110">解説</span><span class="sxs-lookup"><span data-stu-id="a0ece-110">Remarks</span></span>

<span data-ttu-id="a0ece-111">MAPI では、次のように3つのブックマークが定義されています。</span><span class="sxs-lookup"><span data-stu-id="a0ece-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="a0ece-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="a0ece-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="a0ece-113">表の開始位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="a0ece-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="a0ece-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="a0ece-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="a0ece-115">表の現在の位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="a0ece-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="a0ece-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="a0ece-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="a0ece-117">表の終了位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="a0ece-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="a0ece-118">クライアントは、他のテーブルの位置を記憶するためのブックマークを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a0ece-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="a0ece-119">ブックマークは、テーブルを開いている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="a0ece-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="a0ece-120">クライアントは、関連付けられたテーブルを閉じる前に、作成したすべてのブックマークを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0ece-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0ece-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0ece-121">See also</span></span>



[<span data-ttu-id="a0ece-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a0ece-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a0ece-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="a0ece-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="a0ece-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="a0ece-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="a0ece-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="a0ece-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="a0ece-126">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="a0ece-126">MAPI Data Types</span></span>](mapi-data-types.md)

