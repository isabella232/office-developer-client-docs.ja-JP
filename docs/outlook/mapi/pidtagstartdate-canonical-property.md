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
ms.openlocfilehash: fd799a3dc5ba91d388285f649cccfeec188b6143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278821"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="c7c1b-103">PidTagStartDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7c1b-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="c7c1b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7c1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7c1b-105">スケジュールアプリケーションによって管理される予定の開始日時が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7c1b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c7c1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7c1b-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="c7c1b-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="c7c1b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c7c1b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7c1b-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="c7c1b-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="c7c1b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c7c1b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7c1b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c7c1b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c7c1b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c7c1b-112">Area:</span></span>  <br/> |<span data-ttu-id="c7c1b-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="c7c1b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7c1b-114">解説</span><span class="sxs-lookup"><span data-stu-id="c7c1b-114">Remarks</span></span>

<span data-ttu-id="c7c1b-115">スケジュールアプリケーションでは、会議出席依頼を送信するときに、このプロパティと**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) プロパティの両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7c1b-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c7c1b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7c1b-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c7c1b-117">Protocol specifications</span></span>

<span data-ttu-id="c7c1b-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c1b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c1b-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7c1b-120">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c1b-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c1b-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7c1b-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c7c1b-122">Header files</span></span>

<span data-ttu-id="c7c1b-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7c1b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7c1b-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7c1b-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c7c1b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c7c1b-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7c1b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7c1b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7c1b-127">See also</span></span>



[<span data-ttu-id="c7c1b-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c7c1b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7c1b-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7c1b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7c1b-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7c1b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7c1b-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7c1b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

