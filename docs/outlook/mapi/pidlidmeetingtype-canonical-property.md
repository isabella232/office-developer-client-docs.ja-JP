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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331578"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="5f38a-103">PidLidMeetingType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f38a-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="5f38a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f38a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f38a-105">会議出席依頼または会議の更新の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="5f38a-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f38a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f38a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f38a-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="5f38a-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="5f38a-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="5f38a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f38a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="5f38a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="5f38a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5f38a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f38a-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="5f38a-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="5f38a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f38a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f38a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f38a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f38a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5f38a-114">Area:</span></span>  <br/> |<span data-ttu-id="5f38a-115">会議</span><span class="sxs-lookup"><span data-stu-id="5f38a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f38a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5f38a-116">Remarks</span></span>

<span data-ttu-id="5f38a-117">このプロパティの値は、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f38a-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="5f38a-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5f38a-118">**Property**</span></span>|<span data-ttu-id="5f38a-119">**値**</span><span class="sxs-lookup"><span data-stu-id="5f38a-119">**Value**</span></span>|<span data-ttu-id="5f38a-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f38a-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f38a-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="5f38a-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="5f38a-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f38a-122">0x00000000</span></span>  <br/> |<span data-ttu-id="5f38a-123">未指定。</span><span class="sxs-lookup"><span data-stu-id="5f38a-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="5f38a-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="5f38a-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="5f38a-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f38a-125">0x00000001</span></span>  <br/> |<span data-ttu-id="5f38a-126">最初の会議出席依頼。</span><span class="sxs-lookup"><span data-stu-id="5f38a-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="5f38a-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="5f38a-127">mtgFull</span></span>  <br/> |<span data-ttu-id="5f38a-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5f38a-128">0x00010000</span></span>  <br/> |<span data-ttu-id="5f38a-129">完全な更新。</span><span class="sxs-lookup"><span data-stu-id="5f38a-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="5f38a-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="5f38a-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="5f38a-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5f38a-131">0x00020000</span></span>  <br/> |<span data-ttu-id="5f38a-132">情報更新。</span><span class="sxs-lookup"><span data-stu-id="5f38a-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="5f38a-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="5f38a-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="5f38a-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="5f38a-134">0x00080000</span></span>  <br/> |<span data-ttu-id="5f38a-135">この後、新しい会議出席依頼または会議の更新プログラムが受信された。</span><span class="sxs-lookup"><span data-stu-id="5f38a-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="5f38a-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="5f38a-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="5f38a-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="5f38a-137">0x00100000</span></span>  <br/> |<span data-ttu-id="5f38a-138">これは、代理人が会議関連のオブジェクトを処理する場合に、委任者のコピーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="5f38a-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5f38a-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f38a-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f38a-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5f38a-140">Protocol specifications</span></span>

<span data-ttu-id="5f38a-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f38a-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f38a-142">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="5f38a-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f38a-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f38a-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f38a-144">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f38a-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f38a-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5f38a-145">Header files</span></span>

<span data-ttu-id="5f38a-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f38a-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f38a-147">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f38a-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f38a-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f38a-148">See also</span></span>



[<span data-ttu-id="5f38a-149">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5f38a-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f38a-150">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f38a-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f38a-151">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5f38a-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f38a-152">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5f38a-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

