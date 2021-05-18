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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315912"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="28ed8-103">PidLidRecurrenceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28ed8-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="28ed8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28ed8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28ed8-105">定期的な系列の定期的な種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="28ed8-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28ed8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="28ed8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28ed8-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="28ed8-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="28ed8-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="28ed8-108">Property set:</span></span>  <br/> |<span data-ttu-id="28ed8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="28ed8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="28ed8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="28ed8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28ed8-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="28ed8-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="28ed8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="28ed8-112">Data type:</span></span>  <br/> |<span data-ttu-id="28ed8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="28ed8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="28ed8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="28ed8-114">Area:</span></span>  <br/> |<span data-ttu-id="28ed8-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="28ed8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28ed8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="28ed8-116">Remarks</span></span>

<span data-ttu-id="28ed8-117">このプロパティは、次に示す値のいずれかを使用して、定期的な系列の定期的な種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="28ed8-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="28ed8-118">**状態**</span><span class="sxs-lookup"><span data-stu-id="28ed8-118">**Status**</span></span>|<span data-ttu-id="28ed8-119">**値**</span><span class="sxs-lookup"><span data-stu-id="28ed8-119">**Value**</span></span>|<span data-ttu-id="28ed8-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="28ed8-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="28ed8-121">rectypeNone</span><span class="sxs-lookup"><span data-stu-id="28ed8-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="28ed8-122">0</span><span class="sxs-lookup"><span data-stu-id="28ed8-122">0</span></span>  <br/> |<span data-ttu-id="28ed8-123">1 つのインスタンス予定。</span><span class="sxs-lookup"><span data-stu-id="28ed8-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="28ed8-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="28ed8-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="28ed8-125">1</span><span class="sxs-lookup"><span data-stu-id="28ed8-125">1</span></span>  <br/> |<span data-ttu-id="28ed8-126">毎日の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="28ed8-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="28ed8-127">rectypeWeekly</span><span class="sxs-lookup"><span data-stu-id="28ed8-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="28ed8-128">2</span><span class="sxs-lookup"><span data-stu-id="28ed8-128">2</span></span>  <br/> |<span data-ttu-id="28ed8-129">毎週の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="28ed8-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="28ed8-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="28ed8-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="28ed8-131">3</span><span class="sxs-lookup"><span data-stu-id="28ed8-131">3</span></span>  <br/> |<span data-ttu-id="28ed8-132">毎月の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="28ed8-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="28ed8-133">rectypeYearly</span><span class="sxs-lookup"><span data-stu-id="28ed8-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="28ed8-134">4</span><span class="sxs-lookup"><span data-stu-id="28ed8-134">4</span></span>  <br/> |<span data-ttu-id="28ed8-135">年次の定期的なパターン。</span><span class="sxs-lookup"><span data-stu-id="28ed8-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="28ed8-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="28ed8-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28ed8-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="28ed8-137">Protocol specifications</span></span>

<span data-ttu-id="28ed8-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28ed8-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28ed8-139">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="28ed8-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28ed8-140">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28ed8-140">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28ed8-141">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="28ed8-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28ed8-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="28ed8-142">Header files</span></span>

<span data-ttu-id="28ed8-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28ed8-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="28ed8-144">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="28ed8-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28ed8-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="28ed8-145">See also</span></span>



[<span data-ttu-id="28ed8-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="28ed8-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28ed8-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="28ed8-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28ed8-148">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28ed8-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28ed8-149">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="28ed8-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

