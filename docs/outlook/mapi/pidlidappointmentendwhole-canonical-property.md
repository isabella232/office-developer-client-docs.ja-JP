---
title: PidLidAppointmentEndWhole 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358899"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="a5fa0-103">PidLidAppointmentEndWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5fa0-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="a5fa0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5fa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5fa0-105">予定が終了する日時を表します。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5fa0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a5fa0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5fa0-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="a5fa0-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="a5fa0-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a5fa0-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5fa0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a5fa0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a5fa0-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a5fa0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5fa0-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="a5fa0-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="a5fa0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a5fa0-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5fa0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a5fa0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a5fa0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a5fa0-114">Area:</span></span>  <br/> |<span data-ttu-id="a5fa0-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="a5fa0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5fa0-116">解説</span><span class="sxs-lookup"><span data-stu-id="a5fa0-116">Remarks</span></span>

<span data-ttu-id="a5fa0-117">このプロパティは、Microsoft Office Outlook オブジェクトモデルの予定の**dispidApptEndWhole**プロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="a5fa0-118">これにより、イベントの終了日時が指定されます。協定世界時 (UTC) で、 **dispidapptstartwhole** ([](pidlidappointmentstartwhole-canonical-property.md)) プロパティの値より大きい必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="a5fa0-119">定期的なアイテムの場合、 **dispidApptEndWhole**プロパティは、定期的なパターンに従って最初のインスタンスの終了日時です。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a5fa0-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a5fa0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5fa0-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a5fa0-121">Protocol specifications</span></span>

<span data-ttu-id="a5fa0-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5fa0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5fa0-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5fa0-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5fa0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5fa0-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5fa0-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a5fa0-126">Header files</span></span>

<span data-ttu-id="a5fa0-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5fa0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5fa0-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5fa0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5fa0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5fa0-129">See also</span></span>



[<span data-ttu-id="a5fa0-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a5fa0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5fa0-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5fa0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5fa0-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5fa0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5fa0-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5fa0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

