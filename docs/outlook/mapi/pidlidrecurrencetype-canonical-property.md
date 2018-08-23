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
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802102"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="a4e28-103">PidLidRecurrenceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4e28-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="a4e28-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4e28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4e28-105">定期的な一連の定期的なアイテムの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4e28-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a4e28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4e28-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="a4e28-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="a4e28-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-108">Property set:</span></span>  <br/> |<span data-ttu-id="a4e28-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a4e28-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a4e28-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a4e28-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a4e28-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="a4e28-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="a4e28-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a4e28-112">Data type:</span></span>  <br/> |<span data-ttu-id="a4e28-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a4e28-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a4e28-114">領域:</span><span class="sxs-lookup"><span data-stu-id="a4e28-114">Area:</span></span>  <br/> |<span data-ttu-id="a4e28-115">予定表</span><span class="sxs-lookup"><span data-stu-id="a4e28-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4e28-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a4e28-116">Remarks</span></span>

<span data-ttu-id="a4e28-117">このプロパティは、次の値のいずれかを使用して定期的な一連の定期的なアイテムの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="a4e28-118">**Status**</span><span class="sxs-lookup"><span data-stu-id="a4e28-118">**Status**</span></span>|<span data-ttu-id="a4e28-119">**値**</span><span class="sxs-lookup"><span data-stu-id="a4e28-119">**Value**</span></span>|<span data-ttu-id="a4e28-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4e28-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4e28-121">rectypeNone</span><span class="sxs-lookup"><span data-stu-id="a4e28-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="a4e28-122">0</span><span class="sxs-lookup"><span data-stu-id="a4e28-122">0</span></span>  <br/> |<span data-ttu-id="a4e28-123">単一インスタンスの予定です。</span><span class="sxs-lookup"><span data-stu-id="a4e28-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="a4e28-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="a4e28-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="a4e28-125">1</span><span class="sxs-lookup"><span data-stu-id="a4e28-125">1</span></span>  <br/> |<span data-ttu-id="a4e28-126">毎日の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="a4e28-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="a4e28-127">rectypeWeekly</span><span class="sxs-lookup"><span data-stu-id="a4e28-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="a4e28-128">2</span><span class="sxs-lookup"><span data-stu-id="a4e28-128">2</span></span>  <br/> |<span data-ttu-id="a4e28-129">毎週定期的なパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="a4e28-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="a4e28-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="a4e28-131">3</span><span class="sxs-lookup"><span data-stu-id="a4e28-131">3</span></span>  <br/> |<span data-ttu-id="a4e28-132">毎月の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="a4e28-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="a4e28-133">rectypeYearly</span><span class="sxs-lookup"><span data-stu-id="a4e28-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="a4e28-134">4</span><span class="sxs-lookup"><span data-stu-id="a4e28-134">4</span></span>  <br/> |<span data-ttu-id="a4e28-135">年間の定期的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="a4e28-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a4e28-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a4e28-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a4e28-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a4e28-137">Protocol specifications</span></span>

<span data-ttu-id="a4e28-138">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4e28-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4e28-139">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a4e28-140">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a4e28-140">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a4e28-141">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a4e28-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a4e28-142">Header files</span></span>

<span data-ttu-id="a4e28-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4e28-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4e28-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a4e28-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4e28-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4e28-145">See also</span></span>



[<span data-ttu-id="a4e28-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4e28-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4e28-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a4e28-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4e28-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a4e28-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4e28-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a4e28-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

