---
title: PidTagConflictItems の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802543"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="365e8-103">PidTagConflictItems の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="365e8-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="365e8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="365e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="365e8-105">1 つまたは複数のエントリが自動競合解決に関係している項目の Id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="365e8-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="365e8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="365e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="365e8-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="365e8-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="365e8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="365e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="365e8-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="365e8-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="365e8-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="365e8-110">Property type:</span></span>  <br/> |<span data-ttu-id="365e8-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="365e8-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="365e8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="365e8-112">Area:</span></span>  <br/> |<span data-ttu-id="365e8-113">ICS</span><span class="sxs-lookup"><span data-stu-id="365e8-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="365e8-114">備考</span><span class="sxs-lookup"><span data-stu-id="365e8-114">Remarks</span></span>

<span data-ttu-id="365e8-115">自動競合の解決をサポートする標準の Outlook アイテムの種類には、次の標準的な項目の種類が含まれます: 予定表アイテム、連絡先アイテム、履歴項目、メール アイテム、会議アイテム、付箋項目、および作業項目です。</span><span class="sxs-lookup"><span data-stu-id="365e8-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="365e8-116">これらの標準的な項目の種類のいずれかから派生したメッセージ クラスに属するアイテムが自動競合の解決をサポートします。</span><span class="sxs-lookup"><span data-stu-id="365e8-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="365e8-117">Microsoft Outlook 2003 と Microsoft Office Outlook 2007 では、Outlook がアイテムを同期し、結果のコピーにすべての重要なデータが含まれていない可能性があります可能性があることを考慮すると Outlook コピーが格納されて、競合している**競合****同期の失敗**フォルダーの下のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="365e8-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="365e8-118">[**移動**] メニューの**フォルダー一覧**をクリックするまで、**同期の問題**とそのサブフォルダーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="365e8-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="365e8-119">自動競合解決をサポートしている項目の種類の 1 つ、競合の解決では、受注、または、競合の解決のため、[**競合**] フォルダーに格納された場合、アイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="365e8-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="365e8-120">アイテムが置かれているフォルダーでは、 **PR_CONFLICT_ITEMS**の内容を決定します。</span><span class="sxs-lookup"><span data-stu-id="365e8-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="365e8-121">アイテムに競合の解決を獲得する必要がありますが、 **PR_CONFLICT_ITEMS**の 1 つまたは複数のエントリ Id が含まれることの項目は、[**競合**] フォルダー以外のフォルダー内にあるアイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開する場合は、競合の解決で失われたそれらのアイテムです。</span><span class="sxs-lookup"><span data-stu-id="365e8-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="365e8-122">項目は、[**競合**] フォルダー内にあるアイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開する場合は、この項目が競合の解決、失われている必要があり、競合に勝利するアイテムのエントリ ID に含まれることには、 **PR_CONFLICT_ITEMS**解像度です。</span><span class="sxs-lookup"><span data-stu-id="365e8-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="365e8-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="365e8-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="365e8-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="365e8-124">Protocol specifications</span></span>

<span data-ttu-id="365e8-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="365e8-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="365e8-126">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="365e8-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="365e8-127">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="365e8-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="365e8-128">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="365e8-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="365e8-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="365e8-129">Header files</span></span>

<span data-ttu-id="365e8-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="365e8-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="365e8-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="365e8-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="365e8-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="365e8-132">Mapitags.h</span></span>
  
> <span data-ttu-id="365e8-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="365e8-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="365e8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="365e8-134">See also</span></span>



[<span data-ttu-id="365e8-135">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="365e8-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="365e8-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="365e8-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="365e8-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="365e8-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="365e8-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="365e8-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="365e8-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="365e8-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

