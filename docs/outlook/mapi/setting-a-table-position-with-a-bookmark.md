---
title: ブックマークによるテーブルの位置設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f43e3a7e3376cb437620204a29aed9fb732d3427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564095"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="9e4f5-103">ブックマークによるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="9e4f5-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="9e4f5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e4f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e4f5-105">ブックマークは、テーブル内の特定の場所を示すリソースです。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="9e4f5-106">ブックマークの設定は、後で、テーブルの操作のパフォーマンスを大幅に向上する機能の状態に戻します。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="9e4f5-107">MAPI には、標準的な 3 つのブックマークが定義されています。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e4f5-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="9e4f5-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="9e4f5-109">テーブルの現在の行へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="9e4f5-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="9e4f5-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="9e4f5-111">テーブルの最初の行へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="9e4f5-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="9e4f5-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="9e4f5-113">テーブルの最後の行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="9e4f5-114">テーブルの実装は、これらの標準的なブックマークをサポートする必要し、も他のユーザーをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="9e4f5-115">ただし、ブックマークは、リソースをリソースが限られたため、ブックマークのユーザーがそれらを解放、できるだけ早く。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="9e4f5-116">**テーブルの現在の位置にブックマークを設定するのには**</span><span class="sxs-lookup"><span data-stu-id="9e4f5-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="9e4f5-117">[IMAPITable::CreateBookmark](imapitable-createbookmark.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="9e4f5-118">場合によってはメモリ不足の原因で MAPI_E_UNABLE_TO_COMPLETE のエラー値を返す**CreateBookmark** 、新しいブックマークを割り当てることがあります。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="9e4f5-119">**ブックマークを解放するには**</span><span class="sxs-lookup"><span data-stu-id="9e4f5-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="9e4f5-120">[IMAPITable::FreeBookmark](imapitable-freebookmark.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="9e4f5-121">**ブックマークが設定された位置にカーソルを移動するのには**</span><span class="sxs-lookup"><span data-stu-id="9e4f5-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="9e4f5-122">[IMAPITable::SeekRow](imapitable-seekrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="9e4f5-123">**SeekRow**は、BOOKMARK_CURRENT の位置の新しい値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="9e4f5-124">**SeekRow**使用できます、たとえば、現在の位置から 10 個のテーブルの行を配置する、または先頭に最初からやり直す。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="9e4f5-125">クライアントまたはサービス プロバイダー以降では、現在、検索したり、最後のテーブル、または定義済みのブックマークに関連付けられている他の任意の位置。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="9e4f5-126">順方向または逆方向と操作の制限のいずれかで指定された行数に移動できます。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="9e4f5-127">原則として呼び出し元の**SeekRow**; で 50 文字以下の行をシークする必要があります。[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)は、多数の行を使用してください。</span><span class="sxs-lookup"><span data-stu-id="9e4f5-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9e4f5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e4f5-128">See also</span></span>



[<span data-ttu-id="9e4f5-129">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="9e4f5-129">MAPI Tables</span></span>](mapi-tables.md)

