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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338018"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="e57dc-103">PidTagConflictItems 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e57dc-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="e57dc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e57dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e57dc-105">競合の自動解決に関係しているアイテムの1つ以上のエントリ id を含みます。</span><span class="sxs-lookup"><span data-stu-id="e57dc-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e57dc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e57dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e57dc-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="e57dc-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="e57dc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e57dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e57dc-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="e57dc-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="e57dc-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="e57dc-110">Property type:</span></span>  <br/> |<span data-ttu-id="e57dc-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e57dc-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e57dc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e57dc-112">Area:</span></span>  <br/> |<span data-ttu-id="e57dc-113">ICS</span><span class="sxs-lookup"><span data-stu-id="e57dc-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e57dc-114">解説</span><span class="sxs-lookup"><span data-stu-id="e57dc-114">Remarks</span></span>

<span data-ttu-id="e57dc-115">自動競合解決をサポートする標準の Microsoft Outlook アイテムの種類には、予定アイテム、連絡先アイテム、ジャーナルアイテム、メールアイテム、会議アイテム、付箋アイテム、およびタスクアイテムの標準のアイテムの種類があります。</span><span class="sxs-lookup"><span data-stu-id="e57dc-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="e57dc-116">このような標準アイテムの種類のいずれかから派生するメッセージクラスに属するアイテムは、競合の自動解決もサポートします。</span><span class="sxs-lookup"><span data-stu-id="e57dc-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="e57dc-117">microsoft outlook 2003 および microsoft Office outlook 2007 では、outlook がアイテムを同期し、結果コピーに重要なデータがまったく含まれていない可能性があると判断した場合、**競合**するコピーを outlook に格納します。フォルダーを、[**同期の失敗**] フォルダーにします。</span><span class="sxs-lookup"><span data-stu-id="e57dc-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e57dc-118">**同期の問題**とそのサブフォルダーは、[**移動**] メニューの [**フォルダー一覧**] をクリックするまで表示されません。</span><span class="sxs-lookup"><span data-stu-id="e57dc-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="e57dc-119">アイテムは、自動競合解決をサポートしているアイテムの種類のいずれか、競合の解決に勝ち、競合の解決によって [**競合**] フォルダーに配置されたアイテムの**PR_CONFLICT_ITEMS**プロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="e57dc-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="e57dc-120">**PR_CONFLICT_ITEMS**のコンテンツは、アイテムが配置されるフォルダーによって決まります。</span><span class="sxs-lookup"><span data-stu-id="e57dc-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="e57dc-121">アイテムが**競合**フォルダー以外のフォルダーに配置されていて、アイテムが**PR_CONFLICT_ITEMS**プロパティを公開している場合、アイテムは競合の解決を獲得する必要があり、 **PR_CONFLICT_ITEMS**には1つ以上のエントリ id が含まれます。競合の解決で失われたアイテム。</span><span class="sxs-lookup"><span data-stu-id="e57dc-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="e57dc-122">アイテムが conflict フォルダーに配置さ\*\*\*\* れていて、アイテムが**PR_CONFLICT_ITEMS**プロパティを公開している場合、このアイテムは競合の解決を失い、 **PR_CONFLICT_ITEMS**には競合に勝ったアイテムのエントリ ID が格納されます。画質.</span><span class="sxs-lookup"><span data-stu-id="e57dc-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e57dc-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e57dc-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e57dc-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e57dc-124">Protocol specifications</span></span>

<span data-ttu-id="e57dc-125">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e57dc-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e57dc-126">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e57dc-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e57dc-127">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e57dc-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e57dc-128">サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="e57dc-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e57dc-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e57dc-129">Header files</span></span>

<span data-ttu-id="e57dc-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e57dc-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e57dc-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e57dc-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="e57dc-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e57dc-132">Mapitags.h</span></span>
  
> <span data-ttu-id="e57dc-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e57dc-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e57dc-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e57dc-134">See also</span></span>



[<span data-ttu-id="e57dc-135">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="e57dc-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="e57dc-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e57dc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e57dc-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e57dc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e57dc-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e57dc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e57dc-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e57dc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

