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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418135"
---
# <a name="bookmark"></a><span data-ttu-id="ae75e-103">BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="ae75e-103">BOOKMARK</span></span>

  
  
<span data-ttu-id="ae75e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae75e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae75e-105">テーブル内の位置を記憶するブックマーク データを定義します。</span><span class="sxs-lookup"><span data-stu-id="ae75e-105">Defines bookmarks data for remembering a position in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae75e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ae75e-106">Header file:</span></span>  <br/> |<span data-ttu-id="ae75e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae75e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ae75e-108">関連するメソッド:</span><span class="sxs-lookup"><span data-stu-id="ae75e-108">Related methods:</span></span>  <br/> |<span data-ttu-id="ae75e-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="ae75e-109">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md)</span></span> <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a><span data-ttu-id="ae75e-110">注釈</span><span class="sxs-lookup"><span data-stu-id="ae75e-110">Remarks</span></span>

<span data-ttu-id="ae75e-111">MAPI では、次に示す 3 つのブックマークを定義します。</span><span class="sxs-lookup"><span data-stu-id="ae75e-111">MAPI defines three bookmarks, listed as follows:</span></span>
  
<span data-ttu-id="ae75e-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="ae75e-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="ae75e-113">テーブルの開始位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="ae75e-113">Remembers the starting position of the table.</span></span> 
    
<span data-ttu-id="ae75e-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="ae75e-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="ae75e-115">テーブルの現在の位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="ae75e-115">Remembers the current position of the table.</span></span>
    
<span data-ttu-id="ae75e-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="ae75e-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="ae75e-117">テーブルの終了位置を記憶します。</span><span class="sxs-lookup"><span data-stu-id="ae75e-117">Remembers the ending position of the table.</span></span>
    
<span data-ttu-id="ae75e-118">クライアントは、他のテーブル位置を記憶するために他のブックマークを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ae75e-118">Clients can create other bookmarks for remembering other table positions.</span></span> <span data-ttu-id="ae75e-119">ブックマークは、テーブルが開いている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ae75e-119">Bookmarks are valid only when the table is open.</span></span> <span data-ttu-id="ae75e-120">クライアントは、関連付けられたテーブルを閉じる前に、作成したブックマークを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae75e-120">Clients must free any bookmarks that they have created before closing the associated table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae75e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae75e-121">See also</span></span>



[<span data-ttu-id="ae75e-122">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ae75e-122">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ae75e-123">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="ae75e-123">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="ae75e-124">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ae75e-124">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="ae75e-125">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="ae75e-125">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)


[<span data-ttu-id="ae75e-126">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="ae75e-126">MAPI Data Types</span></span>](mapi-data-types.md)

