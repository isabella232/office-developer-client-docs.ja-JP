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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389611"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="91d29-103">PidLidAppointmentEndWhole 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d29-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="91d29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91d29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91d29-105">予定の終了日時を表します。</span><span class="sxs-lookup"><span data-stu-id="91d29-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91d29-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91d29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91d29-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="91d29-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="91d29-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="91d29-108">Property set:</span></span>  <br/> |<span data-ttu-id="91d29-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="91d29-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="91d29-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="91d29-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91d29-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="91d29-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="91d29-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91d29-112">Data type:</span></span>  <br/> |<span data-ttu-id="91d29-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="91d29-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="91d29-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="91d29-114">Area:</span></span>  <br/> |<span data-ttu-id="91d29-115">予定表</span><span class="sxs-lookup"><span data-stu-id="91d29-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91d29-116">備考</span><span class="sxs-lookup"><span data-stu-id="91d29-116">Remarks</span></span>

<span data-ttu-id="91d29-117">このプロパティは、Microsoft Office Outlook オブジェクト モデルでは、予定の**dispidApptEndWhole**プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="91d29-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="91d29-118">イベントの終了日時を指定します。世界協定時刻 (UTC) である必要があり、 **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) プロパティの値より大きくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="91d29-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="91d29-119">一連の定期的な**dispidApptEndWhole**プロパティは、最後の日付と時刻に従って、定期的なパターンの最初のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="91d29-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="91d29-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91d29-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91d29-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91d29-121">Protocol specifications</span></span>

<span data-ttu-id="91d29-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d29-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d29-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="91d29-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91d29-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d29-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d29-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="91d29-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91d29-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="91d29-126">Header files</span></span>

<span data-ttu-id="91d29-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91d29-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="91d29-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91d29-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91d29-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="91d29-129">See also</span></span>



[<span data-ttu-id="91d29-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d29-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91d29-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="91d29-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91d29-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91d29-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91d29-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91d29-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

