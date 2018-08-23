---
title: PidTagStartDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 14a077dfdb0f0781ab0d9f085c758c7a7d6285af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803578"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="ad437-103">PidTagStartDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad437-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="ad437-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad437-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad437-105">開始日時のスケジュール アプリケーションで管理されるように予定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad437-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad437-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ad437-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad437-107">単に PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="ad437-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="ad437-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ad437-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad437-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="ad437-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="ad437-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ad437-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad437-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ad437-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ad437-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ad437-112">Area:</span></span>  <br/> |<span data-ttu-id="ad437-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="ad437-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad437-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ad437-114">Remarks</span></span>

<span data-ttu-id="ad437-115">アプリケーションをスケジュール設定必要がありますこのプロパティおよび**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) のプロパティの両方の会議出席依頼を送信するときです。</span><span class="sxs-lookup"><span data-stu-id="ad437-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad437-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ad437-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad437-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ad437-117">Protocol specifications</span></span>

<span data-ttu-id="ad437-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad437-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad437-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad437-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad437-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad437-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad437-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad437-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad437-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ad437-122">Header files</span></span>

<span data-ttu-id="ad437-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad437-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad437-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad437-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad437-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad437-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ad437-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad437-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad437-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad437-127">See also</span></span>



[<span data-ttu-id="ad437-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad437-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad437-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad437-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad437-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ad437-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad437-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ad437-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

