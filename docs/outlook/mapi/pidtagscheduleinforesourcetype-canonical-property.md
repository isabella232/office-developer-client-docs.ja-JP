---
title: PidTagScheduleInfoResourceType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoResourceType
api_type:
- COM
ms.assetid: 9f253378-0a2d-47e3-82d3-8055b5f776dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9cb149f2ba8c6cd328fcffb00172a1f3f904a24e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572334"
---
# <a name="pidtagscheduleinforesourcetype-canonical-property"></a><span data-ttu-id="1dd18-103">PidTagScheduleInfoResourceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1dd18-103">PidTagScheduleInfoResourceType Canonical Property</span></span>

  
  
<span data-ttu-id="1dd18-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dd18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dd18-105">値ゼロ (0) に設定する必要がありますが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1dd18-105">Contains a value that must be set to zero (0).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1dd18-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1dd18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1dd18-107">PR_SCHDINFO_RESOURCE_TYPE</span><span class="sxs-lookup"><span data-stu-id="1dd18-107">PR_SCHDINFO_RESOURCE_TYPE</span></span>  <br/> |
|<span data-ttu-id="1dd18-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1dd18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1dd18-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="1dd18-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="1dd18-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1dd18-110">Data type:</span></span>  <br/> |<span data-ttu-id="1dd18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1dd18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1dd18-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1dd18-112">Area:</span></span>  <br/> |<span data-ttu-id="1dd18-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="1dd18-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dd18-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1dd18-114">Remarks</span></span>

<span data-ttu-id="1dd18-115">ゼロ (0) に送信され、受信時に無視されると、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dd18-115">This property must be set to zero (0) when sent and ignored upon receipt.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1dd18-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1dd18-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1dd18-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1dd18-117">Protocol specifications</span></span>

<span data-ttu-id="1dd18-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dd18-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dd18-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1dd18-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1dd18-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dd18-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dd18-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="1dd18-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1dd18-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1dd18-122">Header files</span></span>

<span data-ttu-id="1dd18-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1dd18-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1dd18-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1dd18-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1dd18-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1dd18-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1dd18-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1dd18-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dd18-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1dd18-127">See also</span></span>



[<span data-ttu-id="1dd18-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1dd18-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1dd18-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1dd18-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1dd18-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1dd18-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1dd18-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1dd18-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

