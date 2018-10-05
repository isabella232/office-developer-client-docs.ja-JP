---
title: PidLidAppointmentDuration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395407"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="864a5-103">PidLidAppointmentDuration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="864a5-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="864a5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="864a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="864a5-105">分単位で予定をスケジュールするときの時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="864a5-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="864a5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="864a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="864a5-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="864a5-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="864a5-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="864a5-108">Property set:</span></span>  <br/> |<span data-ttu-id="864a5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="864a5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="864a5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="864a5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="864a5-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="864a5-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="864a5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="864a5-112">Data type:</span></span>  <br/> |<span data-ttu-id="864a5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="864a5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="864a5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="864a5-114">Area:</span></span>  <br/> |<span data-ttu-id="864a5-115">予定表</span><span class="sxs-lookup"><span data-stu-id="864a5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="864a5-116">備考</span><span class="sxs-lookup"><span data-stu-id="864a5-116">Remarks</span></span>

<span data-ttu-id="864a5-117">値は**dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) の値と**dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) のプロパティとの間の時間を分単位である必要があります。</span><span class="sxs-lookup"><span data-stu-id="864a5-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="864a5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="864a5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="864a5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="864a5-119">Protocol specifications</span></span>

<span data-ttu-id="864a5-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="864a5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="864a5-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="864a5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="864a5-122">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="864a5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="864a5-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="864a5-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="864a5-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="864a5-124">Header files</span></span>

<span data-ttu-id="864a5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="864a5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="864a5-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="864a5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="864a5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="864a5-127">See also</span></span>



[<span data-ttu-id="864a5-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="864a5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="864a5-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="864a5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="864a5-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="864a5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="864a5-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="864a5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

