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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341994"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="3d3d7-103">PidLidCalendarType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d3d7-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="3d3d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d3d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d3d7-105">**dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティの CalendarType フィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d3d7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3d3d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d3d7-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3d3d7-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="3d3d7-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="3d3d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="3d3d7-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="3d3d7-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="3d3d7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3d3d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3d3d7-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="3d3d7-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="3d3d7-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3d3d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="3d3d7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d3d7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d3d7-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="3d3d7-114">Area:</span></span>  <br/> |<span data-ttu-id="3d3d7-115">会議</span><span class="sxs-lookup"><span data-stu-id="3d3d7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d3d7-116">注釈</span><span class="sxs-lookup"><span data-stu-id="3d3d7-116">Remarks</span></span>

<span data-ttu-id="3d3d7-117">会議出席依頼が定期的な系列または例外を表す場合、 **これは dispidApptRecur** プロパティの CalendarType フィールドの値です。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="3d3d7-118">それ以外の場合、このプロパティは設定され、0 と見なされます。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d3d7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3d3d7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d3d7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3d3d7-120">Protocol specifications</span></span>

<span data-ttu-id="3d3d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d3d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d3d7-122">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d3d7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d3d7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d3d7-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d3d7-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d3d7-125">Header files</span></span>

<span data-ttu-id="3d3d7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d3d7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d3d7-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d3d7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d3d7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d3d7-128">See also</span></span>



[<span data-ttu-id="3d3d7-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3d3d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d3d7-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d3d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d3d7-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3d3d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d3d7-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3d3d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

