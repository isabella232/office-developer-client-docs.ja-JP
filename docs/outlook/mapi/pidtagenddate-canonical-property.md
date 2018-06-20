---
title: PidTagEndDate の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1749c155693529836b20194f9c60763fdd466357
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802726"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="e2f14-103">PidTagEndDate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e2f14-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="e2f14-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2f14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2f14-105">終了日と終了スケジュールのアプリケーションによって管理されるように予定の時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2f14-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f14-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e2f14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2f14-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="e2f14-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="e2f14-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e2f14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2f14-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="e2f14-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="e2f14-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e2f14-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2f14-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e2f14-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e2f14-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e2f14-112">Area:</span></span>  <br/> |<span data-ttu-id="e2f14-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="e2f14-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2f14-114">備考</span><span class="sxs-lookup"><span data-stu-id="e2f14-114">Remarks</span></span>

<span data-ttu-id="e2f14-115">アプリケーションをスケジュール設定必要があります ([PidTagStartDate](pidtagstartdate-canonical-property.md))、**単に PR_START_DATE**およびこのプロパティの両方の会議出席依頼を送信するときです。</span><span class="sxs-lookup"><span data-stu-id="e2f14-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e2f14-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e2f14-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2f14-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e2f14-117">Protocol specifications</span></span>

<span data-ttu-id="e2f14-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2f14-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2f14-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2f14-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2f14-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2f14-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2f14-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2f14-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2f14-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e2f14-122">Header files</span></span>

<span data-ttu-id="e2f14-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2f14-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2f14-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2f14-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2f14-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2f14-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e2f14-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2f14-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2f14-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2f14-127">See also</span></span>



[<span data-ttu-id="e2f14-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2f14-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2f14-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2f14-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2f14-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e2f14-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2f14-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e2f14-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

