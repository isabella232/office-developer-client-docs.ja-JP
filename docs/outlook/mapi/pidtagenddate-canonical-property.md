---
title: PidTagEndDate 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382716"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="31a06-103">PidTagEndDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="31a06-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="31a06-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31a06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31a06-105">終了日と終了スケジュールのアプリケーションによって管理されるように予定の時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31a06-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31a06-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="31a06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31a06-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="31a06-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="31a06-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="31a06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31a06-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="31a06-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="31a06-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="31a06-110">Data type:</span></span>  <br/> |<span data-ttu-id="31a06-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="31a06-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="31a06-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="31a06-112">Area:</span></span>  <br/> |<span data-ttu-id="31a06-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="31a06-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31a06-114">備考</span><span class="sxs-lookup"><span data-stu-id="31a06-114">Remarks</span></span>

<span data-ttu-id="31a06-115">アプリケーションをスケジュール設定必要があります ([PidTagStartDate](pidtagstartdate-canonical-property.md))、**単に PR_START_DATE**およびこのプロパティの両方の会議出席依頼を送信するときです。</span><span class="sxs-lookup"><span data-stu-id="31a06-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31a06-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="31a06-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31a06-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="31a06-117">Protocol specifications</span></span>

<span data-ttu-id="31a06-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31a06-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31a06-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="31a06-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31a06-120">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31a06-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31a06-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="31a06-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31a06-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="31a06-122">Header files</span></span>

<span data-ttu-id="31a06-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31a06-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="31a06-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="31a06-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="31a06-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31a06-125">Mapitags.h</span></span>
  
> <span data-ttu-id="31a06-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31a06-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31a06-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="31a06-127">See also</span></span>



[<span data-ttu-id="31a06-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31a06-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31a06-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31a06-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31a06-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="31a06-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31a06-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="31a06-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

