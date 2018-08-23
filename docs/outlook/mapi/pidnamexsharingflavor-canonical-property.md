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
ms.openlocfilehash: 1f07a11c47c6785bc9a166f11bde8f2e5ef464a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802386"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="3303e-103">PidNameXSharingFlavor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3303e-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="3303e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3303e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3303e-105">**DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="3303e-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3303e-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="3303e-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3303e-107">なし</span><span class="sxs-lookup"><span data-stu-id="3303e-107">None</span></span>  <br/> |
|<span data-ttu-id="3303e-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3303e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3303e-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3303e-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="3303e-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="3303e-110">Property name:</span></span>  <br/> |<span data-ttu-id="3303e-111">X 共有フレーバー</span><span class="sxs-lookup"><span data-stu-id="3303e-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="3303e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3303e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3303e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3303e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3303e-114">領域:</span><span class="sxs-lookup"><span data-stu-id="3303e-114">Area:</span></span>  <br/> |<span data-ttu-id="3303e-115">共有</span><span class="sxs-lookup"><span data-stu-id="3303e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3303e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="3303e-116">Remarks</span></span>

<span data-ttu-id="3303e-117">**DispidSharingFlavor**プロパティは、次の値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3303e-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="3303e-118">**値**</span><span class="sxs-lookup"><span data-stu-id="3303e-118">**Value**</span></span>|<span data-ttu-id="3303e-119">**共有メッセージの種類**</span><span class="sxs-lookup"><span data-stu-id="3303e-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3303e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="3303e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="3303e-121">特殊フォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="3303e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="3303e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="3303e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="3303e-123">特別なフォルダーではないフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="3303e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="3303e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="3303e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="3303e-125">共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="3303e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="3303e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="3303e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="3303e-127">両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="3303e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="3303e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="3303e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="3303e-129">共有の応答、要求を拒否します。</span><span class="sxs-lookup"><span data-stu-id="3303e-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="3303e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="3303e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="3303e-131">共有の応答 (も一種の共有への招待) の要求を受け入れる。</span><span class="sxs-lookup"><span data-stu-id="3303e-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3303e-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3303e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3303e-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3303e-133">Protocol specifications</span></span>

<span data-ttu-id="3303e-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3303e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3303e-135">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3303e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3303e-136">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3303e-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3303e-137">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="3303e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3303e-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3303e-138">Header files</span></span>

<span data-ttu-id="3303e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3303e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="3303e-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3303e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3303e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="3303e-141">See also</span></span>



[<span data-ttu-id="3303e-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3303e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3303e-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3303e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3303e-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3303e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3303e-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3303e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

