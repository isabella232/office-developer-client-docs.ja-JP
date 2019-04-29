---
title: ブックマークによるテーブルの位置設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422461"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="69535-103">ブックマークによるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="69535-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="69535-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69535-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69535-105">ブックマークは、テーブル内の特定の位置を示すリソースです。</span><span class="sxs-lookup"><span data-stu-id="69535-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="69535-106">ブックマークを設定すると、後で位置に戻ることができるようになります。この機能を使用すると、テーブル操作のパフォーマンスを大幅に向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="69535-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="69535-107">MAPI は、3つの標準のブックマークを定義します。</span><span class="sxs-lookup"><span data-stu-id="69535-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69535-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="69535-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="69535-109">表の現在の行を指します。</span><span class="sxs-lookup"><span data-stu-id="69535-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="69535-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="69535-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="69535-111">表の最初の行を指します。</span><span class="sxs-lookup"><span data-stu-id="69535-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="69535-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="69535-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="69535-113">表の最後の行を指します。</span><span class="sxs-lookup"><span data-stu-id="69535-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="69535-114">表の実装者は、これらの標準のブックマークをサポートする必要があります。また、他のユーザーをサポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="69535-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="69535-115">ただし、ブックマークはリソースで、リソースは限られているので、ブックマークユーザーはできるだけ早く解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69535-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="69535-116">**現在の表の位置にブックマークを設定するには**</span><span class="sxs-lookup"><span data-stu-id="69535-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="69535-117">Call [IMAPITable:: createbookmark](imapitable-createbookmark.md)</span><span class="sxs-lookup"><span data-stu-id="69535-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="69535-118">場合によっては、新しいブックマークの割り当てに使用できるメモリが不足することがあり、 **createbookmark**が MAPI_E_UNABLE_TO_COMPLETE エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="69535-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="69535-119">**ブックマークを解放するには**</span><span class="sxs-lookup"><span data-stu-id="69535-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="69535-120">関数 Call [IMAPITable:: freebookmark](imapitable-freebookmark.md)。</span><span class="sxs-lookup"><span data-stu-id="69535-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="69535-121">**ブックマーク位置にカーソルを移動するには**</span><span class="sxs-lookup"><span data-stu-id="69535-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="69535-122">Call [IMAPITable:: seekrow](imapitable-seekrow.md)。</span><span class="sxs-lookup"><span data-stu-id="69535-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="69535-123">**seekrow**は BOOKMARK_CURRENT position の新しい値を確立します。</span><span class="sxs-lookup"><span data-stu-id="69535-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="69535-124">**seekrow**を使用すると、たとえばテーブルを現在の位置から10行分移動したり、先頭からやり直すことができます。</span><span class="sxs-lookup"><span data-stu-id="69535-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="69535-125">クライアントまたはサービスプロバイダーは、テーブルのカレント、先頭、または末尾、あるいは定義済みのブックマークに関連付けられているその他の位置までシークできます。</span><span class="sxs-lookup"><span data-stu-id="69535-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="69535-126">前方または後方のどちらかの方向に移動し、操作を指定した行数に制限できます。</span><span class="sxs-lookup"><span data-stu-id="69535-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="69535-127">原則として、発信者は**seekrow**で50行以内をシークする必要があります。[IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)は、より多くの行で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69535-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="69535-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="69535-128">See also</span></span>



[<span data-ttu-id="69535-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="69535-129">MAPI Tables</span></span>](mapi-tables.md)

