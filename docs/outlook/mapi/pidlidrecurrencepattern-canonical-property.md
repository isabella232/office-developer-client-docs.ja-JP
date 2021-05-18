---
title: PidLidRecurrencePattern 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315933"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="94754-103">PidLidRecurrencePattern 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94754-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="94754-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94754-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94754-105">予定表オブジェクトの定期的なパターンの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="94754-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94754-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94754-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94754-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="94754-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="94754-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="94754-108">Property set:</span></span>  <br/> |<span data-ttu-id="94754-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="94754-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="94754-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="94754-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="94754-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="94754-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="94754-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94754-112">Data type:</span></span>  <br/> |<span data-ttu-id="94754-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94754-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="94754-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="94754-114">Area:</span></span>  <br/> |<span data-ttu-id="94754-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="94754-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94754-116">注釈</span><span class="sxs-lookup"><span data-stu-id="94754-116">Remarks</span></span>

<span data-ttu-id="94754-117">このプロパティを設定する場合は **、dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティで指定された繰り返しの説明に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94754-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94754-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94754-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94754-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94754-119">Protocol specifications</span></span>

<span data-ttu-id="94754-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94754-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94754-121">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="94754-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94754-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94754-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94754-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94754-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94754-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94754-124">Header files</span></span>

<span data-ttu-id="94754-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94754-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="94754-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94754-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94754-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="94754-127">See also</span></span>



[<span data-ttu-id="94754-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="94754-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94754-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94754-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94754-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94754-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94754-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94754-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

