---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418485"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="0e444-103">並べ替えと分類</span><span class="sxs-lookup"><span data-stu-id="0e444-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="0e444-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e444-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e444-105">テーブルを並べ替えると、ビューワーに合った順序で行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="0e444-106">たとえば、ある閲覧者がメッセージの件名で並べ替えたフォルダーのコンテンツ テーブルを表示して、会話のすべてのスレッドが一緒に表示され、別のビューアーがメッセージを送信者の名前で並べ替えたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="0e444-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="0e444-107">新しくインスタンス化されたテーブルは、必ずしも特定の順序で並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e444-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="0e444-108">並べ替えには次の 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="0e444-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="0e444-109">標準の並べ替え</span><span class="sxs-lookup"><span data-stu-id="0e444-109">Standard sorting</span></span>
    
- <span data-ttu-id="0e444-110">分類された並べ替え</span><span class="sxs-lookup"><span data-stu-id="0e444-110">Categorized sorting</span></span> 
    
<span data-ttu-id="0e444-111">標準の並べ替えでは、1 つ以上の列を並べ替えキーとして使用して、すべての行がフラット リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="0e444-112">分類された並べ替えでは、1 つ以上の列を並べ替えキーとして階層的に表示します。</span><span class="sxs-lookup"><span data-stu-id="0e444-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="0e444-113">各カテゴリ内には、次の列を含む特別な見出し行があります。</span><span class="sxs-lookup"><span data-stu-id="0e444-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="0e444-114">並べ替えキーを作成する列または列</span><span class="sxs-lookup"><span data-stu-id="0e444-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="0e444-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e444-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="0e444-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e444-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="0e444-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e444-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="0e444-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e444-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="0e444-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0e444-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="0e444-120">見出し行の下にインデントは、並べ替えキーに一致する値を持つ列を含むテーブルのすべての行です。</span><span class="sxs-lookup"><span data-stu-id="0e444-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="0e444-121">これらの行はリーフ行と呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="0e444-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="0e444-122">リーフ行には、列セット内のすべての列から並べ替えキー列を差し引いた列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e444-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="0e444-123">多くの場合、フォルダーのコンテンツ テーブルでは、標準の並べ替えに加えて分類された並べ替えをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0e444-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="0e444-124">アドレス帳コンテナーのコンテンツ テーブルは、通常、標準の並べ替えのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0e444-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="0e444-125">カテゴリには、折りたたみと展開の 2 つの状態を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0e444-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="0e444-126">カテゴリが折りたたみ状態の場合 [、IMAPITable::QueryRows](imapitable-queryrows.md)から見出し行だけが返されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="0e444-127">カテゴリが展開状態の場合、そのカテゴリに関連する行すべてが返されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="0e444-128">これには、見出し行とリーフ行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e444-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="0e444-129">テーブル ビュー内の各カテゴリは、個別に展開または折りたたみできます。</span><span class="sxs-lookup"><span data-stu-id="0e444-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="0e444-130">つまり、すべてのカテゴリが同時に同じ状態である必要があります。一部のカテゴリは折りたたむ可能性があります。他のカテゴリは展開されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="0e444-131">分類されたテーブルのユーザーは、表示方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="0e444-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="0e444-132">一般的なオプションの 1 つは、ツリー ビュー コントロールと呼Windows SDK で提供されるコントロールを使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="0e444-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="0e444-133">Treeview コントロールは、ツリーのような構造の情報をサポートするリスト ボックスです。</span><span class="sxs-lookup"><span data-stu-id="0e444-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="0e444-134">展開された状態のカテゴリの見出し行にはマイナス記号が付き、折りたたみ状態のカテゴリの見出し行にはプラス記号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="0e444-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="0e444-135">展開されたカテゴリは、見出し行の下にインデントされたリーフ行で表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e444-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="0e444-136">カテゴリを折りたたみ、展開するには、クライアント アプリケーションまたはサービス プロバイダーが次の [IMAPITable : IUnknown](imapitableiunknown.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e444-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="0e444-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="0e444-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="0e444-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="0e444-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="0e444-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="0e444-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="0e444-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="0e444-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="0e444-141">スレッドのスレッドの並べ替えの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e444-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="0e444-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="0e444-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="0e444-143">PidTagSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e444-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="0e444-144">PidTagSubjectPrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e444-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="0e444-145">PidTagNormalizedSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e444-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="0e444-146">PidTagConversationTopic 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e444-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="0e444-147">PidTagConversationIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e444-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="0e444-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="0e444-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="0e444-149">列と制限の設定後のテーブルの並べ替え</span><span class="sxs-lookup"><span data-stu-id="0e444-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="0e444-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e444-150">See also</span></span>



[<span data-ttu-id="0e444-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="0e444-151">MAPI Tables</span></span>](mapi-tables.md)

