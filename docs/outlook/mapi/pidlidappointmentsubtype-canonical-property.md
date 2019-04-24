---
title: PidLidAppointmentSubType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345417"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="5b2bc-103">PidLidAppointmentSubType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b2bc-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="5b2bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b2bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b2bc-105">イベントが終日であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b2bc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5b2bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b2bc-107">dispidapptsubtype</span><span class="sxs-lookup"><span data-stu-id="5b2bc-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="5b2bc-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="5b2bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b2bc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5b2bc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5b2bc-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5b2bc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b2bc-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="5b2bc-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="5b2bc-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5b2bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b2bc-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5b2bc-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5b2bc-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5b2bc-114">Area:</span></span>  <br/> |<span data-ttu-id="5b2bc-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="5b2bc-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b2bc-116">解説</span><span class="sxs-lookup"><span data-stu-id="5b2bc-116">Remarks</span></span>

<span data-ttu-id="5b2bc-117">このプロパティは、イベントがユーザーによって指定された終日イベントであるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="5b2bc-118">値が TRUE の場合は、イベントが終日イベントであることを示します。この場合、期間は24時間の倍数で、24時間以上になるように開始時刻と終了時刻が午前0時になる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="5b2bc-119">値が FALSE の場合、またはこのプロパティが存在しない場合は、イベントが終日イベントではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="5b2bc-120">イベントが開始されて午前0時に終了した場合でも、ユーザーが24時間のイベントを作成した場合、クライアントまたはサーバーは値を TRUE として推論してはなりません。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b2bc-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5b2bc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b2bc-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5b2bc-122">Protocol specifications</span></span>

<span data-ttu-id="5b2bc-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b2bc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b2bc-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b2bc-125">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b2bc-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b2bc-126">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b2bc-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5b2bc-127">Header files</span></span>

<span data-ttu-id="5b2bc-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b2bc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b2bc-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b2bc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b2bc-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b2bc-130">See also</span></span>



[<span data-ttu-id="5b2bc-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5b2bc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b2bc-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b2bc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b2bc-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b2bc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b2bc-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b2bc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

