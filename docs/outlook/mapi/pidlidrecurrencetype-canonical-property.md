---
title: PidLidRecurrenceType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315912"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="1306d-103">PidLidRecurrenceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1306d-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="1306d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1306d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1306d-105">定期的なアイテムの定期的なパターンの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="1306d-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1306d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1306d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1306d-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="1306d-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="1306d-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1306d-108">Property set:</span></span>  <br/> |<span data-ttu-id="1306d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1306d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1306d-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1306d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1306d-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="1306d-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="1306d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1306d-112">Data type:</span></span>  <br/> |<span data-ttu-id="1306d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1306d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1306d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1306d-114">Area:</span></span>  <br/> |<span data-ttu-id="1306d-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="1306d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1306d-116">解説</span><span class="sxs-lookup"><span data-stu-id="1306d-116">Remarks</span></span>

<span data-ttu-id="1306d-117">このプロパティは、次に示す値のいずれかを使用して定期的なアイテムの定期的な種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="1306d-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="1306d-118">**状態**</span><span class="sxs-lookup"><span data-stu-id="1306d-118">**Status**</span></span>|<span data-ttu-id="1306d-119">**値**</span><span class="sxs-lookup"><span data-stu-id="1306d-119">**Value**</span></span>|<span data-ttu-id="1306d-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="1306d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1306d-121">rectypenone</span><span class="sxs-lookup"><span data-stu-id="1306d-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="1306d-122">.0</span><span class="sxs-lookup"><span data-stu-id="1306d-122">0</span></span>  <br/> |<span data-ttu-id="1306d-123">1つのインスタンスの予定。</span><span class="sxs-lookup"><span data-stu-id="1306d-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="1306d-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="1306d-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="1306d-125">1-d</span><span class="sxs-lookup"><span data-stu-id="1306d-125">1</span></span>  <br/> |<span data-ttu-id="1306d-126">日単位の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="1306d-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="1306d-127">rectypeweekly</span><span class="sxs-lookup"><span data-stu-id="1306d-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="1306d-128">pbm-2</span><span class="sxs-lookup"><span data-stu-id="1306d-128">2</span></span>  <br/> |<span data-ttu-id="1306d-129">週単位の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="1306d-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="1306d-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="1306d-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="1306d-131">1/3</span><span class="sxs-lookup"><span data-stu-id="1306d-131">3</span></span>  <br/> |<span data-ttu-id="1306d-132">月単位の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="1306d-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="1306d-133">rectypeyearly</span><span class="sxs-lookup"><span data-stu-id="1306d-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="1306d-134">2/4</span><span class="sxs-lookup"><span data-stu-id="1306d-134">4</span></span>  <br/> |<span data-ttu-id="1306d-135">年単位の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="1306d-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1306d-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1306d-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1306d-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1306d-137">Protocol specifications</span></span>

<span data-ttu-id="1306d-138">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1306d-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1306d-139">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1306d-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1306d-140">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1306d-140">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1306d-141">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1306d-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1306d-142">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1306d-142">Header files</span></span>

<span data-ttu-id="1306d-143">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1306d-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="1306d-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1306d-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1306d-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="1306d-145">See also</span></span>



[<span data-ttu-id="1306d-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1306d-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1306d-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1306d-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1306d-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1306d-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1306d-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1306d-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

