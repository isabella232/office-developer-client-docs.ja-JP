---
title: PidLidMeetingType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ebc7ed4563040e16c71e1df1094667f87a4c09b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572369"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="ae696-103">PidLidMeetingType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae696-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="ae696-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae696-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae696-105">会議出席依頼または会議の更新の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="ae696-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae696-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ae696-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae696-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="ae696-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="ae696-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae696-108">Property set:</span></span>  <br/> |<span data-ttu-id="ae696-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="ae696-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="ae696-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ae696-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ae696-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="ae696-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="ae696-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ae696-112">Data type:</span></span>  <br/> |<span data-ttu-id="ae696-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ae696-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ae696-114">領域:</span><span class="sxs-lookup"><span data-stu-id="ae696-114">Area:</span></span>  <br/> |<span data-ttu-id="ae696-115">会議</span><span class="sxs-lookup"><span data-stu-id="ae696-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae696-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ae696-116">Remarks</span></span>

<span data-ttu-id="ae696-117">このプロパティの値を次のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae696-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="ae696-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="ae696-118">**Property**</span></span>|<span data-ttu-id="ae696-119">**値**</span><span class="sxs-lookup"><span data-stu-id="ae696-119">**Value**</span></span>|<span data-ttu-id="ae696-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae696-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae696-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="ae696-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="ae696-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae696-122">0x00000000</span></span>  <br/> |<span data-ttu-id="ae696-123">指定されていません。</span><span class="sxs-lookup"><span data-stu-id="ae696-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="ae696-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="ae696-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="ae696-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae696-125">0x00000001</span></span>  <br/> |<span data-ttu-id="ae696-126">最初の会議出席依頼の場合。</span><span class="sxs-lookup"><span data-stu-id="ae696-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="ae696-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="ae696-127">mtgFull</span></span>  <br/> |<span data-ttu-id="ae696-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ae696-128">0x00010000</span></span>  <br/> |<span data-ttu-id="ae696-129">フル更新します。</span><span class="sxs-lookup"><span data-stu-id="ae696-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="ae696-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="ae696-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="ae696-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="ae696-131">0x00020000</span></span>  <br/> |<span data-ttu-id="ae696-132">情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="ae696-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="ae696-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="ae696-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="ae696-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="ae696-134">0x00080000</span></span>  <br/> |<span data-ttu-id="ae696-135">この後に新しい会議出席依頼または会議の更新を受信しました。</span><span class="sxs-lookup"><span data-stu-id="ae696-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="ae696-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="ae696-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="ae696-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="ae696-137">0x00100000</span></span>  <br/> |<span data-ttu-id="ae696-138">これは、委任者の場合、デリゲートのハンドルの会議に関連するオブジェクトに設定されています。</span><span class="sxs-lookup"><span data-stu-id="ae696-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ae696-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ae696-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae696-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ae696-140">Protocol specifications</span></span>

<span data-ttu-id="ae696-141">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae696-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae696-142">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae696-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae696-143">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae696-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae696-144">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae696-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae696-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ae696-145">Header files</span></span>

<span data-ttu-id="ae696-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae696-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae696-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae696-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae696-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae696-148">See also</span></span>



[<span data-ttu-id="ae696-149">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae696-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae696-150">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae696-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae696-151">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ae696-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae696-152">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ae696-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

