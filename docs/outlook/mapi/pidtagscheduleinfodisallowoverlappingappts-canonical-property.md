---
title: PidTagScheduleInfoDisallowOverlappingAppts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330087"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="0b85d-103">PidTagScheduleInfoDisallowOverlappingAppts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b85d-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="0b85d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b85d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b85d-105">重複する予定が許可されない場合は TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0b85d-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b85d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0b85d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b85d-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="0b85d-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="0b85d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0b85d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b85d-109">0x686f</span><span class="sxs-lookup"><span data-stu-id="0b85d-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="0b85d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0b85d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b85d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0b85d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0b85d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0b85d-112">Area:</span></span>  <br/> |<span data-ttu-id="0b85d-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="0b85d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b85d-114">解説</span><span class="sxs-lookup"><span data-stu-id="0b85d-114">Remarks</span></span>

<span data-ttu-id="0b85d-115">このプロパティは、 **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) プロパティの値が TRUE の場合にのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="0b85d-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="0b85d-116">値が TRUE の場合は、会議出席依頼に自動的に応答する場合、クライアントまたはサーバーは、以前にスケジュールされたイベントと重複するインスタンスを拒否する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="0b85d-117">値が FALSE の場合、またはこのプロパティが存在しない場合は、重複したインスタンスを受け付ける必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="0b85d-118">これは必須のプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="0b85d-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b85d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0b85d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b85d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0b85d-120">Protocol specifications</span></span>

<span data-ttu-id="0b85d-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b85d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b85d-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b85d-123">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b85d-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b85d-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0b85d-125">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b85d-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b85d-126">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b85d-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0b85d-127">Header files</span></span>

<span data-ttu-id="0b85d-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b85d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b85d-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b85d-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b85d-130">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0b85d-130">Mapitags.h</span></span>
  
> <span data-ttu-id="0b85d-131">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b85d-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b85d-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b85d-132">See also</span></span>



[<span data-ttu-id="0b85d-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0b85d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b85d-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b85d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b85d-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0b85d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b85d-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0b85d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

