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
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801717"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="6ba04-103">PidLidAppointmentColor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ba04-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="6ba04-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ba04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ba04-105">予定表を表示するときに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ba04-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6ba04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ba04-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="6ba04-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="6ba04-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ba04-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6ba04-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6ba04-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6ba04-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ba04-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="6ba04-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="6ba04-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6ba04-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ba04-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6ba04-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6ba04-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6ba04-114">Area:</span></span>  <br/> |<span data-ttu-id="6ba04-115">予定表</span><span class="sxs-lookup"><span data-stu-id="6ba04-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ba04-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6ba04-116">Remarks</span></span>

<span data-ttu-id="6ba04-117">このプロパティは、予定表を表示するときに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="6ba04-118">クライアントまたはサーバーは、古いクライアントとの下位互換性のためには、この値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ba04-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="6ba04-119">カレンダーで指定した[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)として**のキーワード**([PidNameKeywords](pidnamekeywords-canonical-property.md)) プロパティの値に基づくことが代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ba04-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="6ba04-120">設定すると、値があります、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="6ba04-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="6ba04-121">**値**</span><span class="sxs-lookup"><span data-stu-id="6ba04-121">**Value**</span></span>|<span data-ttu-id="6ba04-122">**色**</span><span class="sxs-lookup"><span data-stu-id="6ba04-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ba04-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ba04-123">0x00000000</span></span>  <br/> |<span data-ttu-id="6ba04-124">なし</span><span class="sxs-lookup"><span data-stu-id="6ba04-124">None</span></span>  <br/> |
|<span data-ttu-id="6ba04-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ba04-125">0x00000001</span></span>  <br/> |<span data-ttu-id="6ba04-126">赤</span><span class="sxs-lookup"><span data-stu-id="6ba04-126">Red</span></span>  <br/> |
|<span data-ttu-id="6ba04-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6ba04-127">0x00000002</span></span>  <br/> |<span data-ttu-id="6ba04-128">青</span><span class="sxs-lookup"><span data-stu-id="6ba04-128">Blue</span></span>  <br/> |
|<span data-ttu-id="6ba04-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6ba04-129">0x00000003</span></span>  <br/> |<span data-ttu-id="6ba04-130">緑</span><span class="sxs-lookup"><span data-stu-id="6ba04-130">Green</span></span>  <br/> |
|<span data-ttu-id="6ba04-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6ba04-131">0x00000004</span></span>  <br/> |<span data-ttu-id="6ba04-132">灰色</span><span class="sxs-lookup"><span data-stu-id="6ba04-132">Grey</span></span>  <br/> |
|<span data-ttu-id="6ba04-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6ba04-133">0x00000005</span></span>  <br/> |<span data-ttu-id="6ba04-134">オレンジ</span><span class="sxs-lookup"><span data-stu-id="6ba04-134">Orange</span></span>  <br/> |
|<span data-ttu-id="6ba04-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="6ba04-135">0x00000006</span></span>  <br/> |<span data-ttu-id="6ba04-136">シアン</span><span class="sxs-lookup"><span data-stu-id="6ba04-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="6ba04-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="6ba04-137">0x00000007</span></span>  <br/> |<span data-ttu-id="6ba04-138">オリーブ</span><span class="sxs-lookup"><span data-stu-id="6ba04-138">Olive</span></span>  <br/> |
|<span data-ttu-id="6ba04-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6ba04-139">0x00000008</span></span>  <br/> |<span data-ttu-id="6ba04-140">紫</span><span class="sxs-lookup"><span data-stu-id="6ba04-140">Purple</span></span>  <br/> |
|<span data-ttu-id="6ba04-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6ba04-141">0x00000009</span></span>  <br/> |<span data-ttu-id="6ba04-142">青緑</span><span class="sxs-lookup"><span data-stu-id="6ba04-142">Teal</span></span>  <br/> |
|<span data-ttu-id="6ba04-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="6ba04-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="6ba04-144">黄</span><span class="sxs-lookup"><span data-stu-id="6ba04-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6ba04-145">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6ba04-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ba04-146">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6ba04-146">Protocol specifications</span></span>

<span data-ttu-id="6ba04-147">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba04-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba04-148">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ba04-149">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba04-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba04-150">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ba04-151">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6ba04-151">Header files</span></span>

<span data-ttu-id="6ba04-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ba04-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ba04-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ba04-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ba04-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ba04-154">See also</span></span>



[<span data-ttu-id="6ba04-155">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ba04-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ba04-156">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ba04-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ba04-157">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ba04-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ba04-158">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ba04-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

