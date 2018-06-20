---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803963"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="76c5b-103">並べ替えと分類</span><span class="sxs-lookup"><span data-stu-id="76c5b-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="76c5b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76c5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76c5b-105">テーブルを並べ替えると、そのビューアーに意味のある順序で行が配置されます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="76c5b-106">たとえば、1 つのビューアー会話のすべてのスレッドはまとめて別のビューアーはメッセージの送信者の名前で並べ替える必要がありますように、メッセージの件名でソートするフォルダーの内容を表示する方がよい。</span><span class="sxs-lookup"><span data-stu-id="76c5b-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="76c5b-107">必ずしも、新しくインスタンス化されたテーブルは、特定の順序では並べ替えられません。</span><span class="sxs-lookup"><span data-stu-id="76c5b-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="76c5b-108">並べ替えの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="76c5b-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="76c5b-109">標準の並べ替え</span><span class="sxs-lookup"><span data-stu-id="76c5b-109">Standard sorting</span></span>
    
- <span data-ttu-id="76c5b-110">並べ替えの分類</span><span class="sxs-lookup"><span data-stu-id="76c5b-110">Categorized sorting</span></span> 
    
<span data-ttu-id="76c5b-111">標準的な並べ替え順が、すべての行が並べ替えキーとして 1 つまたは複数の列を使用する単純なリストで表示されます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="76c5b-112">分類された並べ替え順では、行が階層で表示される 1 つまたは複数の列の並べ替えキーとして。</span><span class="sxs-lookup"><span data-stu-id="76c5b-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="76c5b-113">カテゴリごとに、次の列を含む特別な見出し行があります。</span><span class="sxs-lookup"><span data-stu-id="76c5b-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="76c5b-114">列または列の並べ替えキーを構成します。</span><span class="sxs-lookup"><span data-stu-id="76c5b-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="76c5b-115">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76c5b-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="76c5b-116">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76c5b-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="76c5b-117">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76c5b-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="76c5b-118">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76c5b-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="76c5b-119">**PR_ROW_TYPE**([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76c5b-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="76c5b-120">並べ替えキーに一致する値を持つ列を含むテーブルからすべての行は、見出し行の下にインデントします。</span><span class="sxs-lookup"><span data-stu-id="76c5b-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="76c5b-121">これらの行は、リーフ行と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="76c5b-122">リーフ行には、マイナス キー列の並べ替えを設定する列のすべての列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76c5b-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="76c5b-123">フォルダーの内容のテーブルは多くの場合、標準の並べ替えだけでなくカテゴリ別に並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="76c5b-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="76c5b-124">アドレス帳コンテナーの内容のテーブルは通常、標準的な並べ替えのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="76c5b-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="76c5b-125">カテゴリが 2 つの状態を持つことができます: が折りたたまれているし、展開します。</span><span class="sxs-lookup"><span data-stu-id="76c5b-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="76c5b-126">カテゴリが折りたたまれた状態のときは、 [IMAPITable::QueryRows](imapitable-queryrows.md)から見出し行のみが返されます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="76c5b-127">カテゴリが展開状態にすると、すべてのカテゴリに関連する行が返されます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="76c5b-128">これには、見出し行とリーフ行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="76c5b-129">表形式ビュー内の各カテゴリを展開または個別に折りたたまれています。</span><span class="sxs-lookup"><span data-stu-id="76c5b-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="76c5b-130">は同時に、すべてのカテゴリと同じ状態にする必要がありますは、他のユーザーが展開されている間は、いくつかのカテゴリを折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="76c5b-131">分類されたテーブルのユーザーは、表示方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="76c5b-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="76c5b-132">1 つの一般的なオプションでは、ツリー ビュー コントロールと呼ばれる Windows SDK で提供されているコントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c5b-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="76c5b-133">Treeview コントロールは、ツリーのような構造で情報をサポートするリスト ボックスです。</span><span class="sxs-lookup"><span data-stu-id="76c5b-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="76c5b-134">折りたたまれた状態のカテゴリの見出し行にはプラス記号が付いている間、展開した状態でのカテゴリの見出し行にはマイナス記号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="76c5b-135">展開されているカテゴリは、リーフ行が見出し行の下にインデントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="76c5b-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="76c5b-136">カテゴリを展開し、クライアント アプリケーションまたはサービス プロバイダーを使用して次[IMAPITable: IUnknown](imapitableiunknown.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="76c5b-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="76c5b-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76c5b-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="76c5b-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76c5b-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="76c5b-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="76c5b-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="76c5b-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="76c5b-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="76c5b-141">並べ替えの詳細については、会話のスレッドでは、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c5b-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="76c5b-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="76c5b-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="76c5b-143">PidTagSubject の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76c5b-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="76c5b-144">PidTagSubjectPrefix の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76c5b-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="76c5b-145">PidTagNormalizedSubject の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76c5b-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="76c5b-146">PidTagConversationTopic の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76c5b-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="76c5b-147">PidTagConversationIndex の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76c5b-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="76c5b-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="76c5b-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="76c5b-149">列と制約を設定した後のテーブルの並べ替え</span><span class="sxs-lookup"><span data-stu-id="76c5b-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="76c5b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="76c5b-150">See also</span></span>



[<span data-ttu-id="76c5b-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="76c5b-151">MAPI Tables</span></span>](mapi-tables.md)

