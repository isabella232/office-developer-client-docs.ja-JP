---
title: PidLidAppointmentStartWhole 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389135"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="769c3-103">PidLidAppointmentStartWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="769c3-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="769c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="769c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="769c3-105">予定を開始する時刻と日付を表します。</span><span class="sxs-lookup"><span data-stu-id="769c3-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="769c3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="769c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="769c3-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="769c3-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="769c3-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="769c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="769c3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="769c3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="769c3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="769c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="769c3-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="769c3-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="769c3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="769c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="769c3-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="769c3-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="769c3-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="769c3-114">Area:</span></span>  <br/> |<span data-ttu-id="769c3-115">予定表</span><span class="sxs-lookup"><span data-stu-id="769c3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="769c3-116">備考</span><span class="sxs-lookup"><span data-stu-id="769c3-116">Remarks</span></span>

<span data-ttu-id="769c3-117">このプロパティは、イベントの開始日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="769c3-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="769c3-118">このプロパティは、世界協定時刻 (UTC) である必要があります、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティの値より小さくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="769c3-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="769c3-119">定期的な一連のこのプロパティは、定期的なアイテムのパターンに従って、最初のインスタンスの開始日時です。</span><span class="sxs-lookup"><span data-stu-id="769c3-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="769c3-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="769c3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="769c3-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="769c3-121">Protocol specifications</span></span>

<span data-ttu-id="769c3-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="769c3-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="769c3-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="769c3-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="769c3-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="769c3-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="769c3-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="769c3-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="769c3-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="769c3-126">Header files</span></span>

<span data-ttu-id="769c3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="769c3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="769c3-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="769c3-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="769c3-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="769c3-129">See also</span></span>



[<span data-ttu-id="769c3-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="769c3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="769c3-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="769c3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="769c3-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="769c3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="769c3-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="769c3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

