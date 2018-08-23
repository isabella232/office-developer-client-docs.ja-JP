---
title: PidTagParentDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 910a62a660ea17992aa391d7453919d9fbb53c86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580433"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="dda0a-103">PidTagParentDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dda0a-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="dda0a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dda0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dda0a-105">検索時にメッセージがあるフォルダーの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dda0a-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dda0a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dda0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dda0a-107">PR_PARENT_DISPLAY、PR_PARENT_DISPLAY_A、PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="dda0a-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="dda0a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dda0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dda0a-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="dda0a-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="dda0a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dda0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="dda0a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dda0a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dda0a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="dda0a-112">Area:</span></span>  <br/> |<span data-ttu-id="dda0a-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="dda0a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dda0a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dda0a-114">Remarks</span></span>

<span data-ttu-id="dda0a-115">これらのプロパティは、任意のオブジェクトではありません。</span><span class="sxs-lookup"><span data-stu-id="dda0a-115">These properties is not on any object.</span></span> <span data-ttu-id="dda0a-116">のみ検索結果フォルダーの内容の表に表示されることができます。</span><span class="sxs-lookup"><span data-stu-id="dda0a-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="dda0a-117">これらのプロパティおよびプロパティの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) は、互いに関係ありません。</span><span class="sxs-lookup"><span data-stu-id="dda0a-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="dda0a-118">まったく異なるコンテキストに属しているとします。</span><span class="sxs-lookup"><span data-stu-id="dda0a-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dda0a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dda0a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dda0a-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dda0a-120">Header files</span></span>

<span data-ttu-id="dda0a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dda0a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="dda0a-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dda0a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="dda0a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dda0a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dda0a-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dda0a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dda0a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="dda0a-125">See also</span></span>



[<span data-ttu-id="dda0a-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dda0a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dda0a-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dda0a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dda0a-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dda0a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dda0a-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dda0a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

