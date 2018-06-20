---
title: PidTagScheduleInfoDisallowOverlappingAppts の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3719c0d86b0f14324e65b963d2a81a27f6cd52ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803457"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="a7bbb-103">PidTagScheduleInfoDisallowOverlappingAppts の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a7bbb-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="a7bbb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7bbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7bbb-105">予定の重複が許可されていない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7bbb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7bbb-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="a7bbb-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="a7bbb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a7bbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7bbb-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="a7bbb-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="a7bbb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7bbb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a7bbb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a7bbb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a7bbb-112">Area:</span></span>  <br/> |<span data-ttu-id="a7bbb-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="a7bbb-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7bbb-114">備考</span><span class="sxs-lookup"><span data-stu-id="a7bbb-114">Remarks</span></span>

<span data-ttu-id="a7bbb-115">このプロパティは、 **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) プロパティの値が TRUE の場合にのみ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="a7bbb-116">値では、true の場合、自動的に会議出席依頼に応答するとき、クライアントまたはサーバーが必要があります拒否以前にスケジュールされたイベントが重複するインスタンスを示します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="a7bbb-117">値が FALSE の場合、またはこのプロパティがない場合は、インスタンスが重複している必要がありますが受け入れられることを示します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="a7bbb-118">必須プロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7bbb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a7bbb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7bbb-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a7bbb-120">Protocol specifications</span></span>

<span data-ttu-id="a7bbb-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7bbb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7bbb-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7bbb-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7bbb-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7bbb-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a7bbb-125">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7bbb-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7bbb-126">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7bbb-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a7bbb-127">Header files</span></span>

<span data-ttu-id="a7bbb-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7bbb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7bbb-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7bbb-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7bbb-130">Mapitags.h</span></span>
  
> <span data-ttu-id="a7bbb-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7bbb-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7bbb-132">See also</span></span>



[<span data-ttu-id="a7bbb-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7bbb-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7bbb-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7bbb-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7bbb-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a7bbb-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7bbb-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a7bbb-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

