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
ms.openlocfilehash: 8f3c385c29589638bc314cc15635a12bb157d949
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568743"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="24804-103">PidLidRecurrenceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24804-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="24804-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24804-105">定期的な一連の定期的なアイテムの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="24804-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24804-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="24804-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24804-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="24804-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="24804-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="24804-108">Property set:</span></span>  <br/> |<span data-ttu-id="24804-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="24804-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="24804-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="24804-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="24804-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="24804-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="24804-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="24804-112">Data type:</span></span>  <br/> |<span data-ttu-id="24804-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24804-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24804-114">領域:</span><span class="sxs-lookup"><span data-stu-id="24804-114">Area:</span></span>  <br/> |<span data-ttu-id="24804-115">予定表</span><span class="sxs-lookup"><span data-stu-id="24804-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24804-116">注釈</span><span class="sxs-lookup"><span data-stu-id="24804-116">Remarks</span></span>

<span data-ttu-id="24804-117">このプロパティは、次の値のいずれかを使用して定期的な一連の定期的なアイテムの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="24804-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="24804-118">**Status**</span><span class="sxs-lookup"><span data-stu-id="24804-118">**Status**</span></span>|<span data-ttu-id="24804-119">**値**</span><span class="sxs-lookup"><span data-stu-id="24804-119">**Value**</span></span>|<span data-ttu-id="24804-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="24804-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24804-121">rectypeNone</span><span class="sxs-lookup"><span data-stu-id="24804-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="24804-122">0</span><span class="sxs-lookup"><span data-stu-id="24804-122">0</span></span>  <br/> |<span data-ttu-id="24804-123">単一インスタンスの予定です。</span><span class="sxs-lookup"><span data-stu-id="24804-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="24804-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="24804-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="24804-125">1</span><span class="sxs-lookup"><span data-stu-id="24804-125">1</span></span>  <br/> |<span data-ttu-id="24804-126">毎日の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="24804-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="24804-127">rectypeWeekly</span><span class="sxs-lookup"><span data-stu-id="24804-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="24804-128">2</span><span class="sxs-lookup"><span data-stu-id="24804-128">2</span></span>  <br/> |<span data-ttu-id="24804-129">毎週定期的なパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="24804-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="24804-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="24804-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="24804-131">3</span><span class="sxs-lookup"><span data-stu-id="24804-131">3</span></span>  <br/> |<span data-ttu-id="24804-132">毎月の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="24804-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="24804-133">rectypeYearly</span><span class="sxs-lookup"><span data-stu-id="24804-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="24804-134">4</span><span class="sxs-lookup"><span data-stu-id="24804-134">4</span></span>  <br/> |<span data-ttu-id="24804-135">年間の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="24804-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="24804-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24804-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24804-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="24804-137">Protocol specifications</span></span>

<span data-ttu-id="24804-138">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24804-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24804-139">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="24804-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24804-140">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24804-140">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24804-141">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="24804-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24804-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24804-142">Header files</span></span>

<span data-ttu-id="24804-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24804-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="24804-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24804-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24804-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="24804-145">See also</span></span>



[<span data-ttu-id="24804-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24804-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24804-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24804-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24804-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="24804-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24804-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="24804-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

