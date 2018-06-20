---
title: PidLidAppointmentSubType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb9f4e0f58ea27d36ba911ed60527a2e53f23727
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801804"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="39b0c-103">PidLidAppointmentSubType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="39b0c-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="39b0c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39b0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39b0c-105">イベントが 1 日であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39b0c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="39b0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39b0c-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="39b0c-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="39b0c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-108">Property set:</span></span>  <br/> |<span data-ttu-id="39b0c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="39b0c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="39b0c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="39b0c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="39b0c-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="39b0c-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="39b0c-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-112">Data type:</span></span>  <br/> |<span data-ttu-id="39b0c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="39b0c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="39b0c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="39b0c-114">Area:</span></span>  <br/> |<span data-ttu-id="39b0c-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="39b0c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39b0c-116">備考</span><span class="sxs-lookup"><span data-stu-id="39b0c-116">Remarks</span></span>

<span data-ttu-id="39b0c-117">このプロパティは、イベントは、終日イベントでは、ユーザーが指定されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="39b0c-118">TRUE の値は、イベントが終日イベントでは、場合に、開始時刻と終了時刻する必要があることで、午前 0 時 24 時間の倍数の期間とは、少なくとも 24 時間を示します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="39b0c-119">値が FALSE の場合、またはこのプロパティがない場合は、イベントが終日イベントではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="39b0c-120">クライアントまたはサーバーではイベントが開始され、午前 0 時に終了した場合でも、ユーザーが 24 時間であるイベントを作成する場合、値は TRUE としてを推測こと必要がありますいません。</span><span class="sxs-lookup"><span data-stu-id="39b0c-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="39b0c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="39b0c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39b0c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="39b0c-122">Protocol specifications</span></span>

<span data-ttu-id="39b0c-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39b0c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39b0c-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39b0c-125">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39b0c-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39b0c-126">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39b0c-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="39b0c-127">Header files</span></span>

<span data-ttu-id="39b0c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39b0c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="39b0c-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="39b0c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39b0c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="39b0c-130">See also</span></span>



[<span data-ttu-id="39b0c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="39b0c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39b0c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="39b0c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39b0c-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="39b0c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39b0c-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="39b0c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

