---
title: PidTagConflictItems 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338018"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="8b4d7-103">PidTagConflictItems 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b4d7-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="8b4d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b4d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b4d7-105">自動競合解決に関与したアイテムの 1 つ以上のエントリの ID を含む。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="8b4d7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8b4d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b4d7-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="8b4d7-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="8b4d7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8b4d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b4d7-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="8b4d7-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="8b4d7-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="8b4d7-110">Property type:</span></span>  <br/> |<span data-ttu-id="8b4d7-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8b4d7-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8b4d7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8b4d7-112">Area:</span></span>  <br/> |<span data-ttu-id="8b4d7-113">ICS</span><span class="sxs-lookup"><span data-stu-id="8b4d7-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b4d7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8b4d7-114">Remarks</span></span>

<span data-ttu-id="8b4d7-115">自動競合解決をサポートする標準の Microsoft Outlook アイテムの種類には、予定アイテム、連絡先アイテム、ジャーナル アイテム、メール アイテム、会議アイテム、付箋アイテム、タスク アイテムの標準アイテムの種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="8b4d7-116">これらの標準アイテムの種類の 1 つから派生するメッセージ クラスに属するアイテムは、自動競合解決もサポートします。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="8b4d7-117">Microsoft Outlook 2003 および Microsoft Office Outlook 2007 では、Outlook がアイテムを同期し、結果のコピーにすべての重要なデータが含まれている可能性があると考える場合、Outlook は競合するコピーを [同期の問題] フォルダーの[競合] フォルダーに格納します。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b4d7-118">**[移動] メニューの**[フォルダー一覧]をクリックするまで、同期の問題とそのサブフォルダー **は非表示** になります。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="8b4d7-119">自動競合解決をサポートするアイテムの種類の 1 つ、競合解決で勝ったアイテム、または競合解決のために **Conflicts** フォルダーに配置されている場合、アイテムは **PR_CONFLICT_ITEMS** プロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="8b4d7-120">アイテムを配置するフォルダーによって、アイテムのコンテンツが **PR_CONFLICT_ITEMS。**</span><span class="sxs-lookup"><span data-stu-id="8b4d7-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="8b4d7-121">アイテムが **Conflicts** フォルダー以外の一部のフォルダーにあり、 **そのアイテム** が PR_CONFLICT_ITEMS プロパティを公開している場合、そのアイテムは競合解決に勝っている必要があります **。PR_CONFLICT_ITEMS** には、競合解決で失われたアイテムの 1 つ以上のエントリの ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="8b4d7-122">アイテムが **Conflicts** フォルダーにあり、アイテムが **PR_CONFLICT_ITEMS** プロパティを公開している場合、このアイテムは競合解決を失い **、PR_CONFLICT_ITEMS** には競合解決で勝ったアイテムのエントリ ID が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b4d7-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8b4d7-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b4d7-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8b4d7-124">Protocol specifications</span></span>

<span data-ttu-id="8b4d7-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b4d7-126">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b4d7-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b4d7-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b4d7-128">サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b4d7-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8b4d7-129">Header files</span></span>

<span data-ttu-id="8b4d7-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b4d7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b4d7-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b4d7-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b4d7-132">Mapitags.h</span></span>
  
> <span data-ttu-id="8b4d7-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8b4d7-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b4d7-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b4d7-134">See also</span></span>



[<span data-ttu-id="8b4d7-135">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="8b4d7-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="8b4d7-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8b4d7-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b4d7-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b4d7-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b4d7-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8b4d7-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b4d7-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8b4d7-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

