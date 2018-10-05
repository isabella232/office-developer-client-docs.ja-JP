---
title: PidLidAppointmentNotAllowPropose 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentNotAllowPropose
api_type:
- COM
ms.assetid: 8be9e2aa-2dc1-406d-8864-7f556de22809
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aa9aacd8a1d75ed4c14a980e162a68c47995a55c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385418"
---
# <a name="pidlidappointmentnotallowpropose-canonical-property"></a><span data-ttu-id="858ba-103">PidLidAppointmentNotAllowPropose 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="858ba-103">PidLidAppointmentNotAllowPropose Canonical Property</span></span>

  
  
<span data-ttu-id="858ba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="858ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="858ba-105">出席者が会議の新しい日時を提案するために使用できないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="858ba-105">Indicates whether attendees are not allowed to propose a new date/time for the meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="858ba-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="858ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="858ba-107">dispidApptNotAllowPropose</span><span class="sxs-lookup"><span data-stu-id="858ba-107">dispidApptNotAllowPropose</span></span>  <br/> |
|<span data-ttu-id="858ba-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="858ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="858ba-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="858ba-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="858ba-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="858ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="858ba-111">0x0000825A</span><span class="sxs-lookup"><span data-stu-id="858ba-111">0x0000825A</span></span>  <br/> |
|<span data-ttu-id="858ba-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="858ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="858ba-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="858ba-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="858ba-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="858ba-114">Area:</span></span>  <br/> |<span data-ttu-id="858ba-115">会議</span><span class="sxs-lookup"><span data-stu-id="858ba-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="858ba-116">備考</span><span class="sxs-lookup"><span data-stu-id="858ba-116">Remarks</span></span>

<span data-ttu-id="858ba-117">値 FALSE、またはこのプロパティがない場合は、出席者が新しい日時を提案するために許可されてことを示します。</span><span class="sxs-lookup"><span data-stu-id="858ba-117">A value of FALSE, or the absence of this property indicates that the attendees are allowed to propose a new date/time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="858ba-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="858ba-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="858ba-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="858ba-119">Protocol specifications</span></span>

<span data-ttu-id="858ba-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="858ba-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="858ba-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="858ba-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="858ba-122">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="858ba-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="858ba-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="858ba-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="858ba-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="858ba-124">Header files</span></span>

<span data-ttu-id="858ba-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="858ba-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="858ba-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="858ba-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="858ba-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="858ba-127">See also</span></span>



[<span data-ttu-id="858ba-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="858ba-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="858ba-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="858ba-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="858ba-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="858ba-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="858ba-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="858ba-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

