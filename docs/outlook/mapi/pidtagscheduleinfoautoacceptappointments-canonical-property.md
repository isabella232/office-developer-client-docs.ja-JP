---
title: PidTagScheduleInfoAutoAcceptAppointments の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803448"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="15768-103">PidTagScheduleInfoAutoAcceptAppointments の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="15768-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="15768-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15768-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15768-105">クライアントまたはサーバーに自動的に応答すべての会議出席依頼に出席者またはリソースの場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="15768-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15768-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="15768-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15768-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="15768-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="15768-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="15768-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15768-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="15768-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="15768-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="15768-110">Data type:</span></span>  <br/> |<span data-ttu-id="15768-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="15768-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="15768-112">領域:</span><span class="sxs-lookup"><span data-stu-id="15768-112">Area:</span></span>  <br/> |<span data-ttu-id="15768-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="15768-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15768-114">備考</span><span class="sxs-lookup"><span data-stu-id="15768-114">Remarks</span></span>

<span data-ttu-id="15768-115">応答、応答する必要がある場合は、受け入れ、 **PR_SCHDINFO_DISALLOW_ と**PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) で指定されている制約の場合を除き、OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) のプロパティが満たされています。</span><span class="sxs-lookup"><span data-stu-id="15768-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="15768-116">値が FALSE の場合、またはこのプロパティがない場合は、クライアントまたはサーバーする必要があります自動的に受け付けないこと会議出席依頼を示します。</span><span class="sxs-lookup"><span data-stu-id="15768-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="15768-117">必須プロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="15768-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15768-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="15768-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15768-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="15768-119">Protocol specifications</span></span>

<span data-ttu-id="15768-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15768-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15768-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="15768-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15768-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15768-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15768-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="15768-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="15768-124">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15768-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15768-125">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="15768-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15768-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="15768-126">Header files</span></span>

<span data-ttu-id="15768-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15768-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="15768-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="15768-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="15768-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15768-129">Mapitags.h</span></span>
  
> <span data-ttu-id="15768-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15768-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15768-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="15768-131">See also</span></span>



[<span data-ttu-id="15768-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15768-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15768-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="15768-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15768-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="15768-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15768-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="15768-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

