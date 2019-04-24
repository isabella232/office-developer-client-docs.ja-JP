---
title: 並べ替えと分類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344507"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="e0d3f-103">並べ替えと分類</span><span class="sxs-lookup"><span data-stu-id="e0d3f-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="e0d3f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0d3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0d3f-105">テーブルを並べ替えると、表示されるのがわかりやすい順序で行が配置されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="e0d3f-106">たとえば、ある閲覧者は、メッセージの件名で並べ替えたフォルダーの内容テーブルを表示して、会話のすべてのスレッドが一緒に表示されるようにしたり、別の閲覧者が送信者の名前で並べ替えられたメッセージを表示したりできるようにしたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="e0d3f-107">新たにインスタンス化されたテーブルは、必ずしも特定の順序で並べ替えられるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="e0d3f-108">並べ替えには、次の2種類があります。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="e0d3f-109">標準の並べ替え</span><span class="sxs-lookup"><span data-stu-id="e0d3f-109">Standard sorting</span></span>
    
- <span data-ttu-id="e0d3f-110">分類された並べ替え</span><span class="sxs-lookup"><span data-stu-id="e0d3f-110">Categorized sorting</span></span> 
    
<span data-ttu-id="e0d3f-111">標準の並べ替えでは、1つまたは複数の列を並べ替えキーとして使用して、すべての行がフラットリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="e0d3f-112">分類された並べ替えの場合、行は、並べ替えキーとして1つまたは複数の列と共に階層的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="e0d3f-113">各カテゴリ内には、次の列を含む特別な見出し行があります。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="e0d3f-114">並べ替えキーを構成する列 (複数の場合があります)</span><span class="sxs-lookup"><span data-stu-id="e0d3f-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="e0d3f-115">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0d3f-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0d3f-116">**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0d3f-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0d3f-117">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0d3f-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0d3f-118">**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0d3f-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0d3f-119">**PR_ROW_TYPE**([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0d3f-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="e0d3f-120">見出し行の下のインデントは、並べ替えキーと一致する値を持つ列を含むテーブルのすべての行です。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="e0d3f-121">これらの行はリーフ行と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="e0d3f-122">リーフ行には、列セットのすべての列と並べ替えキー列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="e0d3f-123">フォルダーの内容の表は、通常、標準の並べ替えに加えて、分類された並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="e0d3f-124">通常、アドレス帳コンテナーのコンテンツテーブルは標準の並べ替えのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="e0d3f-125">カテゴリには、折りたたまれて展開される2つの状態があります。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="e0d3f-126">カテゴリが折りたたまれた状態の場合は、見出し行のみが[IMAPITable:: QueryRows](imapitable-queryrows.md)から返されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e0d3f-127">カテゴリが展開された状態になると、そのカテゴリに関連するすべての行が返されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="e0d3f-128">これには、見出し行とリーフ行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="e0d3f-129">テーブルビューの各カテゴリは個別に展開または折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="e0d3f-130">つまり、すべてのカテゴリが同時に同じ状態である必要はありません。一部のカテゴリは折りたたむことができ、他のカテゴリは展開されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="e0d3f-131">分類されたテーブルのユーザーが、表示方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="e0d3f-132">1つの一般的なオプションは、treeview コントロールと呼ばれる Windows SDK で提供されるコントロールを使用することです。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="e0d3f-133">Treeview コントロールは、ツリーに似た構造の情報をサポートするリストボックスです。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="e0d3f-134">展開された状態のカテゴリの見出し行には、マイナス記号が付いています。折りたたまれた状態のカテゴリの見出し行には、プラス記号が付いています。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="e0d3f-135">展開されたカテゴリは、列見出しの下にあるリーフ行と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="e0d3f-136">カテゴリを折りたたむと展開するために、クライアントアプリケーションまたはサービスプロバイダーは、次の[IMAPITable: IUnknown](imapitableiunknown.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="e0d3f-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="e0d3f-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="e0d3f-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="e0d3f-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="e0d3f-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="e0d3f-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="e0d3f-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="e0d3f-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="e0d3f-141">会話のスレッドの並べ替えの詳細については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0d3f-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="e0d3f-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e0d3f-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="e0d3f-143">PidTagSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0d3f-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="e0d3f-144">PidTagSubjectPrefix 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0d3f-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="e0d3f-145">PidTagNormalizedSubject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0d3f-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="e0d3f-146">PidTagConversationTopic 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0d3f-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="e0d3f-147">PidTagConversationIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0d3f-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="e0d3f-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="e0d3f-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="e0d3f-149">列と制限の設定後のテーブルの並べ替え</span><span class="sxs-lookup"><span data-stu-id="e0d3f-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="e0d3f-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0d3f-150">See also</span></span>



[<span data-ttu-id="e0d3f-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e0d3f-151">MAPI Tables</span></span>](mapi-tables.md)

