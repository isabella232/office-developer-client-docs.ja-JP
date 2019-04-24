---
title: PidNameXSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360887"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="9b68b-103">PidNameXSharingFlavor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b68b-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="9b68b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b68b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b68b-105">**dispidsharingflavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="9b68b-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b68b-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="9b68b-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9b68b-107">なし</span><span class="sxs-lookup"><span data-stu-id="9b68b-107">None</span></span>  <br/> |
|<span data-ttu-id="9b68b-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="9b68b-108">Property set:</span></span>  <br/> |<span data-ttu-id="9b68b-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="9b68b-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="9b68b-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="9b68b-110">Property name:</span></span>  <br/> |<span data-ttu-id="9b68b-111">X 共有-フレーバー</span><span class="sxs-lookup"><span data-stu-id="9b68b-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="9b68b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9b68b-112">Data type:</span></span>  <br/> |<span data-ttu-id="9b68b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b68b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b68b-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9b68b-114">Area:</span></span>  <br/> |<span data-ttu-id="9b68b-115">共有</span><span class="sxs-lookup"><span data-stu-id="9b68b-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b68b-116">解説</span><span class="sxs-lookup"><span data-stu-id="9b68b-116">Remarks</span></span>

<span data-ttu-id="9b68b-117">**dispidsharingflavor**プロパティには、次のいずれかの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b68b-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="9b68b-118">**値**</span><span class="sxs-lookup"><span data-stu-id="9b68b-118">**Value**</span></span>|<span data-ttu-id="9b68b-119">**共有メッセージの種類**</span><span class="sxs-lookup"><span data-stu-id="9b68b-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b68b-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="9b68b-120">0x00020310</span></span>  <br/> |<span data-ttu-id="9b68b-121">特別なフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="9b68b-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="9b68b-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="9b68b-122">0x00000310</span></span>  <br/> |<span data-ttu-id="9b68b-123">特別なフォルダーではないフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="9b68b-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="9b68b-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="9b68b-124">0x00020500</span></span>  <br/> |<span data-ttu-id="9b68b-125">共有の依頼。</span><span class="sxs-lookup"><span data-stu-id="9b68b-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="9b68b-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="9b68b-126">0x00020710</span></span>  <br/> |<span data-ttu-id="9b68b-127">特別なフォルダーの共有への招待と、受信者の同等の特殊フォルダーに対する共有要求の両方。</span><span class="sxs-lookup"><span data-stu-id="9b68b-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="9b68b-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="9b68b-128">0x00025100</span></span>  <br/> |<span data-ttu-id="9b68b-129">要求を拒否する共有応答。</span><span class="sxs-lookup"><span data-stu-id="9b68b-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="9b68b-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="9b68b-130">0x00023310</span></span>  <br/> |<span data-ttu-id="9b68b-131">要求 (共有への招待の種類も) を受け入れる共有応答。</span><span class="sxs-lookup"><span data-stu-id="9b68b-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9b68b-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9b68b-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b68b-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9b68b-133">Protocol specifications</span></span>

<span data-ttu-id="9b68b-134">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b68b-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b68b-135">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b68b-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b68b-136">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b68b-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b68b-137">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="9b68b-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b68b-138">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9b68b-138">Header files</span></span>

<span data-ttu-id="9b68b-139">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b68b-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b68b-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b68b-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b68b-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b68b-141">See also</span></span>



[<span data-ttu-id="9b68b-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9b68b-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b68b-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b68b-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b68b-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9b68b-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b68b-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9b68b-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

