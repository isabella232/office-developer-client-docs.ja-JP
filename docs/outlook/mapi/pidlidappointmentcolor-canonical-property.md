---
title: PidLidAppointmentColor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345438"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="1ce69-103">PidLidAppointmentColor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ce69-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="1ce69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ce69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ce69-105">予定表を表示するときに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ce69-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ce69-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1ce69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ce69-107">dispidapptcolor</span><span class="sxs-lookup"><span data-stu-id="1ce69-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="1ce69-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1ce69-108">Property set:</span></span>  <br/> |<span data-ttu-id="1ce69-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1ce69-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1ce69-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1ce69-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1ce69-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="1ce69-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="1ce69-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1ce69-112">Data type:</span></span>  <br/> |<span data-ttu-id="1ce69-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1ce69-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1ce69-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1ce69-114">Area:</span></span>  <br/> |<span data-ttu-id="1ce69-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="1ce69-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ce69-116">解説</span><span class="sxs-lookup"><span data-stu-id="1ce69-116">Remarks</span></span>

<span data-ttu-id="1ce69-117">このプロパティは、予定表を表示するときに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ce69-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="1ce69-118">クライアントまたはサーバーは、以前のクライアントとの下位互換性のためにこの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ce69-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="1ce69-119">代わりに、 [[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で指定した**Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) プロパティの値に基づいて予定表が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="1ce69-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="1ce69-120">設定する場合、値は次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ce69-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="1ce69-121">**値**</span><span class="sxs-lookup"><span data-stu-id="1ce69-121">**Value**</span></span>|<span data-ttu-id="1ce69-122">**色**</span><span class="sxs-lookup"><span data-stu-id="1ce69-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ce69-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ce69-123">0x00000000</span></span>  <br/> |<span data-ttu-id="1ce69-124">なし</span><span class="sxs-lookup"><span data-stu-id="1ce69-124">None</span></span>  <br/> |
|<span data-ttu-id="1ce69-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1ce69-125">0x00000001</span></span>  <br/> |<span data-ttu-id="1ce69-126">赤</span><span class="sxs-lookup"><span data-stu-id="1ce69-126">Red</span></span>  <br/> |
|<span data-ttu-id="1ce69-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1ce69-127">0x00000002</span></span>  <br/> |<span data-ttu-id="1ce69-128">青</span><span class="sxs-lookup"><span data-stu-id="1ce69-128">Blue</span></span>  <br/> |
|<span data-ttu-id="1ce69-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1ce69-129">0x00000003</span></span>  <br/> |<span data-ttu-id="1ce69-130">緑</span><span class="sxs-lookup"><span data-stu-id="1ce69-130">Green</span></span>  <br/> |
|<span data-ttu-id="1ce69-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1ce69-131">0x00000004</span></span>  <br/> |<span data-ttu-id="1ce69-132">灰色</span><span class="sxs-lookup"><span data-stu-id="1ce69-132">Grey</span></span>  <br/> |
|<span data-ttu-id="1ce69-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1ce69-133">0x00000005</span></span>  <br/> |<span data-ttu-id="1ce69-134">Orange</span><span class="sxs-lookup"><span data-stu-id="1ce69-134">Orange</span></span>  <br/> |
|<span data-ttu-id="1ce69-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="1ce69-135">0x00000006</span></span>  <br/> |<span data-ttu-id="1ce69-136">シアン</span><span class="sxs-lookup"><span data-stu-id="1ce69-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="1ce69-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="1ce69-137">0x00000007</span></span>  <br/> |<span data-ttu-id="1ce69-138">オリーブ</span><span class="sxs-lookup"><span data-stu-id="1ce69-138">Olive</span></span>  <br/> |
|<span data-ttu-id="1ce69-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1ce69-139">0x00000008</span></span>  <br/> |<span data-ttu-id="1ce69-140">紫</span><span class="sxs-lookup"><span data-stu-id="1ce69-140">Purple</span></span>  <br/> |
|<span data-ttu-id="1ce69-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1ce69-141">0x00000009</span></span>  <br/> |<span data-ttu-id="1ce69-142">Teal</span><span class="sxs-lookup"><span data-stu-id="1ce69-142">Teal</span></span>  <br/> |
|<span data-ttu-id="1ce69-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="1ce69-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="1ce69-144">黄</span><span class="sxs-lookup"><span data-stu-id="1ce69-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1ce69-145">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1ce69-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ce69-146">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1ce69-146">Protocol specifications</span></span>

<span data-ttu-id="1ce69-147">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ce69-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ce69-148">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ce69-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ce69-149">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ce69-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ce69-150">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ce69-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ce69-151">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1ce69-151">Header files</span></span>

<span data-ttu-id="1ce69-152">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ce69-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ce69-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ce69-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ce69-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ce69-154">See also</span></span>



[<span data-ttu-id="1ce69-155">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1ce69-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ce69-156">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ce69-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ce69-157">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1ce69-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ce69-158">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1ce69-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

