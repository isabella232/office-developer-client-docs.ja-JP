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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386300"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="030ac-103">PidLidRecurrencePattern 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="030ac-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="030ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="030ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="030ac-105">カレンダー オブジェクトの定期的なパターンの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="030ac-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="030ac-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="030ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="030ac-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="030ac-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="030ac-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="030ac-108">Property set:</span></span>  <br/> |<span data-ttu-id="030ac-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="030ac-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="030ac-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="030ac-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="030ac-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="030ac-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="030ac-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="030ac-112">Data type:</span></span>  <br/> |<span data-ttu-id="030ac-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="030ac-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="030ac-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="030ac-114">Area:</span></span>  <br/> |<span data-ttu-id="030ac-115">予定表</span><span class="sxs-lookup"><span data-stu-id="030ac-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="030ac-116">備考</span><span class="sxs-lookup"><span data-stu-id="030ac-116">Remarks</span></span>

<span data-ttu-id="030ac-117">このプロパティが設定されている場合は、 **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) のプロパティで指定されている定期的なアイテムの説明を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="030ac-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="030ac-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="030ac-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="030ac-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="030ac-119">Protocol specifications</span></span>

<span data-ttu-id="030ac-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="030ac-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="030ac-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="030ac-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="030ac-122">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="030ac-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="030ac-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="030ac-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="030ac-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="030ac-124">Header files</span></span>

<span data-ttu-id="030ac-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="030ac-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="030ac-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="030ac-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="030ac-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="030ac-127">See also</span></span>



[<span data-ttu-id="030ac-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="030ac-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="030ac-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="030ac-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="030ac-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="030ac-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="030ac-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="030ac-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

