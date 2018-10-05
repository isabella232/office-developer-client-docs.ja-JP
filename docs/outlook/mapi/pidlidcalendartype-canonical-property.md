---
title: PidLidCalendarType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396520"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="43c54-103">PidLidCalendarType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43c54-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="43c54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43c54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43c54-105">**DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) のプロパティから [カレンダーの種類] フィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="43c54-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43c54-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="43c54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43c54-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="43c54-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="43c54-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="43c54-108">Property set:</span></span>  <br/> |<span data-ttu-id="43c54-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="43c54-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="43c54-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="43c54-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="43c54-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="43c54-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="43c54-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="43c54-112">Data type:</span></span>  <br/> |<span data-ttu-id="43c54-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43c54-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43c54-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="43c54-114">Area:</span></span>  <br/> |<span data-ttu-id="43c54-115">会議</span><span class="sxs-lookup"><span data-stu-id="43c54-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43c54-116">備考</span><span class="sxs-lookup"><span data-stu-id="43c54-116">Remarks</span></span>

<span data-ttu-id="43c54-117">会議出席依頼は、一連の定期的なまたは例外を表している場合は、 **dispidApptRecur**プロパティから [カレンダーの種類] フィールドの値になります。</span><span class="sxs-lookup"><span data-stu-id="43c54-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="43c54-118">それ以外の場合、このプロパティは設定されず、0 と見なされます。</span><span class="sxs-lookup"><span data-stu-id="43c54-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43c54-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43c54-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43c54-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="43c54-120">Protocol specifications</span></span>

<span data-ttu-id="43c54-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43c54-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43c54-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="43c54-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43c54-123">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43c54-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43c54-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="43c54-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43c54-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43c54-125">Header files</span></span>

<span data-ttu-id="43c54-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43c54-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="43c54-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43c54-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43c54-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="43c54-128">See also</span></span>



[<span data-ttu-id="43c54-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43c54-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43c54-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43c54-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43c54-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="43c54-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43c54-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="43c54-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

