---
title: ブックマークを使用してテーブルの位置を設定する
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
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="fb547-103">ブックマークを使用してテーブルの位置を設定する</span><span class="sxs-lookup"><span data-stu-id="fb547-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="fb547-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb547-105">ブックマークは、テーブル内の特定の場所を示すリソースです。</span><span class="sxs-lookup"><span data-stu-id="fb547-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="fb547-106">ブックマークを設定すると、後で位置に戻り、テーブル操作のパフォーマンスを大幅に向上させる機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="fb547-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="fb547-107">MAPI では、次の 3 つの標準ブックマークを定義します。</span><span class="sxs-lookup"><span data-stu-id="fb547-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb547-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="fb547-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="fb547-109">テーブル内の現在の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="fb547-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="fb547-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="fb547-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="fb547-111">テーブルの最初の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="fb547-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="fb547-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="fb547-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="fb547-113">テーブルの最後の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="fb547-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="fb547-114">テーブル実装者は、これらの標準ブックマークをサポートするために必要であり、他のユーザーもサポートできます。</span><span class="sxs-lookup"><span data-stu-id="fb547-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="fb547-115">ただし、ブックマークはリソースであり、リソースは限られているため、ブックマーク ユーザーはできるだけ早く解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb547-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="fb547-116">**現在のテーブル位置にブックマークを設定するには**</span><span class="sxs-lookup"><span data-stu-id="fb547-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="fb547-117">[IMAPITable::CreateBookmark を呼び出します](imapitable-createbookmark.md)。</span><span class="sxs-lookup"><span data-stu-id="fb547-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="fb547-118">新しいブックマークを割り当てるのに十分なメモリが不足し **、CreateBookmark** がエラー値を返MAPI_E_UNABLE_TO_COMPLETE場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb547-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="fb547-119">**ブックマークを解放するには**</span><span class="sxs-lookup"><span data-stu-id="fb547-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="fb547-120">[IMAPITable::FreeBookmark を呼び出します](imapitable-freebookmark.md)。</span><span class="sxs-lookup"><span data-stu-id="fb547-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="fb547-121">**カーソルをブックマーク位置に移動するには**</span><span class="sxs-lookup"><span data-stu-id="fb547-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="fb547-122">[IMAPITable::SeekRow を呼び出します](imapitable-seekrow.md)。</span><span class="sxs-lookup"><span data-stu-id="fb547-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="fb547-123">**SeekRow は** 、ユーザーの位置に新しい値BOOKMARK_CURRENTします。</span><span class="sxs-lookup"><span data-stu-id="fb547-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="fb547-124">**SeekRow** を使用すると、たとえば、現在の位置から 10 行のテーブルを配置したり、先頭から最初に行を開始したりできます。</span><span class="sxs-lookup"><span data-stu-id="fb547-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="fb547-125">クライアントまたはサービス プロバイダーは、テーブルの現在、開始、または終了、または定義済みのブックマークに関連付けられているその他の位置をシークできます。</span><span class="sxs-lookup"><span data-stu-id="fb547-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="fb547-126">順方向または後方方向に移動し、操作を指定した行数に制限できます。</span><span class="sxs-lookup"><span data-stu-id="fb547-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="fb547-127">原則として、発信者は SeekRow を使用して 50 行以下を **シークする必要があります**。 [IMAPITable::SeekRowApprox は](imapitable-seekrowapprox.md) 、より多くの行で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb547-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fb547-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb547-128">See also</span></span>



[<span data-ttu-id="fb547-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="fb547-129">MAPI Tables</span></span>](mapi-tables.md)

