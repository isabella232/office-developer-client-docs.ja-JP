---
title: PidLidSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327483"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="4f629-103">PidLidSharingFlavor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f629-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="4f629-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f629-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f629-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="4f629-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f629-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4f629-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f629-107">dispidsharingflavor</span><span class="sxs-lookup"><span data-stu-id="4f629-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="4f629-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="4f629-108">Property set:</span></span>  <br/> |<span data-ttu-id="4f629-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="4f629-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="4f629-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4f629-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4f629-111">0x00008a18</span><span class="sxs-lookup"><span data-stu-id="4f629-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="4f629-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4f629-112">Data type:</span></span>  <br/> |<span data-ttu-id="4f629-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f629-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f629-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="4f629-114">Area:</span></span>  <br/> |<span data-ttu-id="4f629-115">共有</span><span class="sxs-lookup"><span data-stu-id="4f629-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f629-116">解説</span><span class="sxs-lookup"><span data-stu-id="4f629-116">Remarks</span></span>

<span data-ttu-id="4f629-117">このプロパティの値は、次のいずれかであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="4f629-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="4f629-118">**値**</span><span class="sxs-lookup"><span data-stu-id="4f629-118">**Value**</span></span>|<span data-ttu-id="4f629-119">**共有メッセージオブジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="4f629-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f629-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="4f629-120">0x00020310</span></span>  <br/> |<span data-ttu-id="4f629-121">特別なフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="4f629-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="4f629-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="4f629-122">0x00000310</span></span>  <br/> |<span data-ttu-id="4f629-123">特別なフォルダーではないフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="4f629-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="4f629-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="4f629-124">0x00020500</span></span>  <br/> |<span data-ttu-id="4f629-125">共有の依頼。</span><span class="sxs-lookup"><span data-stu-id="4f629-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="4f629-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="4f629-126">0x00020710</span></span>  <br/> |<span data-ttu-id="4f629-127">特別なフォルダーの共有への招待と、受信者の同等の特殊フォルダーに対する共有要求の両方。</span><span class="sxs-lookup"><span data-stu-id="4f629-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="4f629-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="4f629-128">0x00025100</span></span>  <br/> |<span data-ttu-id="4f629-129">要求を拒否する共有応答。</span><span class="sxs-lookup"><span data-stu-id="4f629-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="4f629-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="4f629-130">0x00023310</span></span>  <br/> |<span data-ttu-id="4f629-131">要求 (共有への招待の種類も) を受け入れる共有の応答。</span><span class="sxs-lookup"><span data-stu-id="4f629-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4f629-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4f629-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f629-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4f629-133">Protocol specifications</span></span>

<span data-ttu-id="4f629-134">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f629-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f629-135">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f629-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f629-136">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f629-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f629-137">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="4f629-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f629-138">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4f629-138">Header files</span></span>

<span data-ttu-id="4f629-139">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f629-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f629-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f629-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f629-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f629-141">See also</span></span>



[<span data-ttu-id="4f629-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4f629-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f629-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f629-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f629-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f629-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f629-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f629-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

