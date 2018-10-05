---
title: PidLidAppointmentSequenceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSequenceTime
api_type:
- COM
ms.assetid: 0170bb9b-f43b-4089-9144-b8652c38f43d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d5daa2672fb0b392c4f01492c4dcd36bdac3ba2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391361"
---
# <a name="pidlidappointmentsequencetime-canonical-property"></a><span data-ttu-id="4c18f-103">PidLidAppointmentSequenceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c18f-103">PidLidAppointmentSequenceTime Canonical Property</span></span>

  
  
<span data-ttu-id="4c18f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c18f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c18f-105">このプロパティが最後に修正された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c18f-105">Specifies the date and time at which this property was last modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c18f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4c18f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c18f-107">dispidApptSeqTime</span><span class="sxs-lookup"><span data-stu-id="4c18f-107">dispidApptSeqTime</span></span>  <br/> |
|<span data-ttu-id="4c18f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4c18f-108">Property set:</span></span>  <br/> |<span data-ttu-id="4c18f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4c18f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4c18f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4c18f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4c18f-111">0x00008202</span><span class="sxs-lookup"><span data-stu-id="4c18f-111">0x00008202</span></span>  <br/> |
|<span data-ttu-id="4c18f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4c18f-112">Data type:</span></span>  <br/> |<span data-ttu-id="4c18f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4c18f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4c18f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="4c18f-114">Area:</span></span>  <br/> |<span data-ttu-id="4c18f-115">会議</span><span class="sxs-lookup"><span data-stu-id="4c18f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c18f-116">備考</span><span class="sxs-lookup"><span data-stu-id="4c18f-116">Remarks</span></span>

<span data-ttu-id="4c18f-117">値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c18f-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c18f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4c18f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c18f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4c18f-119">Protocol specifications</span></span>

<span data-ttu-id="4c18f-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c18f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c18f-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c18f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c18f-122">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c18f-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c18f-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c18f-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c18f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4c18f-124">Header files</span></span>

<span data-ttu-id="4c18f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c18f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c18f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c18f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c18f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c18f-127">See also</span></span>



[<span data-ttu-id="4c18f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c18f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c18f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c18f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c18f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c18f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c18f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c18f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

