---
title: PidLidAppointmentProposedStartWhole 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedStartWhole
api_type:
- COM
ms.assetid: acc96b0a-bffb-46ef-8c46-b831d165a346
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bdf810ee71f5b79435bb706f8f60f5d4054c7f75
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591702"
---
# <a name="pidlidappointmentproposedstartwhole-canonical-property"></a><span data-ttu-id="5c046-103">PidLidAppointmentProposedStartWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c046-103">PidLidAppointmentProposedStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="5c046-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c046-105">**DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) の新しい日時の指定の提案値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c046-105">Specifies the proposed value for **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c046-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5c046-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c046-107">dispidApptProposedStartWhole</span><span class="sxs-lookup"><span data-stu-id="5c046-107">dispidApptProposedStartWhole</span></span>  <br/> |
|<span data-ttu-id="5c046-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5c046-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c046-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5c046-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5c046-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5c046-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c046-111">0x00008250</span><span class="sxs-lookup"><span data-stu-id="5c046-111">0x00008250</span></span>  <br/> |
|<span data-ttu-id="5c046-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5c046-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c046-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5c046-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5c046-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5c046-114">Area:</span></span>  <br/> |<span data-ttu-id="5c046-115">会議</span><span class="sxs-lookup"><span data-stu-id="5c046-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c046-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5c046-116">Remarks</span></span>

<span data-ttu-id="5c046-117">この値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c046-117">This value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c046-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5c046-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c046-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5c046-119">Protocol specifications</span></span>

<span data-ttu-id="5c046-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c046-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c046-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c046-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c046-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c046-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c046-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c046-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c046-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5c046-124">Header files</span></span>

<span data-ttu-id="5c046-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c046-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c046-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c046-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c046-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c046-127">See also</span></span>



[<span data-ttu-id="5c046-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c046-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c046-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c046-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c046-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c046-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c046-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c046-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

