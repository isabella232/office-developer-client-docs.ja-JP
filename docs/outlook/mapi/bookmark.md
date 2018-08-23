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
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799906"
---
# <a name="bookmark"></a><span data-ttu-id="09ac8-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="09ac8-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="09ac8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09ac8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09ac8-105">テーブル内の位置を記憶するためのブックマークのデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="09ac8-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09ac8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="09ac8-106">Header file:</span></span>  <br/> |<span data-ttu-id="09ac8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09ac8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="09ac8-108">関連する方法があります。</span><span class="sxs-lookup"><span data-stu-id="09ac8-108">Related methods:</span></span>  <br/> |<span data-ttu-id="09ac8-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="09ac8-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="09ac8-110">注釈</span><span class="sxs-lookup"><span data-stu-id="09ac8-110">Remarks</span></span>

<span data-ttu-id="09ac8-111">MAPI には、以下のとおり、3 つのブックマークが定義されています。</span><span class="sxs-lookup"><span data-stu-id="09ac8-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="09ac8-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="09ac8-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="09ac8-113">テーブルの開始位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="09ac8-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="09ac8-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="09ac8-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="09ac8-115">テーブルの現在の位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="09ac8-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="09ac8-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="09ac8-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="09ac8-117">テーブルの末尾の位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="09ac8-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="09ac8-118">クライアントは、他のテーブルの位置を記憶するための他のブックマークを作成できます。</span><span class="sxs-lookup"><span data-stu-id="09ac8-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="09ac8-119">ブックマークは、テーブルが開いているときのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="09ac8-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="09ac8-120">クライアントは、関連するテーブルを閉じる前に、作成したすべてのブックマークを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09ac8-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="09ac8-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="09ac8-121">See also</span></span>



[<span data-ttu-id="09ac8-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="09ac8-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="09ac8-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="09ac8-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="09ac8-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="09ac8-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="09ac8-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="09ac8-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="09ac8-126">MAPI データ型</span><span class="sxs-lookup"><span data-stu-id="09ac8-126">MAPI Data Types</span></span>](mapi-data-types.md)

