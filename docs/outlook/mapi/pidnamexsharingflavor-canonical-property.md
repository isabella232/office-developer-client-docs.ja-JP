---
title: PidNameXSharingFlavor の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1f07a11c47c6785bc9a166f11bde8f2e5ef464a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802386"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="5cc86-103">PidNameXSharingFlavor の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5cc86-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="5cc86-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5cc86-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5cc86-105">**DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cc86-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="5cc86-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="5cc86-107">なし</span><span class="sxs-lookup"><span data-stu-id="5cc86-107">None</span></span>  <br/> |
|<span data-ttu-id="5cc86-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-108">Property set:</span></span>  <br/> |<span data-ttu-id="5cc86-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5cc86-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="5cc86-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="5cc86-110">Property name:</span></span>  <br/> |<span data-ttu-id="5cc86-111">X 共有フレーバー</span><span class="sxs-lookup"><span data-stu-id="5cc86-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="5cc86-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-112">Data type:</span></span>  <br/> |<span data-ttu-id="5cc86-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5cc86-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5cc86-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5cc86-114">Area:</span></span>  <br/> |<span data-ttu-id="5cc86-115">共有</span><span class="sxs-lookup"><span data-stu-id="5cc86-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cc86-116">備考</span><span class="sxs-lookup"><span data-stu-id="5cc86-116">Remarks</span></span>

<span data-ttu-id="5cc86-117">**DispidSharingFlavor**プロパティは、次の値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc86-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="5cc86-118">**値**</span><span class="sxs-lookup"><span data-stu-id="5cc86-118">**Value**</span></span>|<span data-ttu-id="5cc86-119">**共有メッセージの種類**</span><span class="sxs-lookup"><span data-stu-id="5cc86-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cc86-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="5cc86-120">0x00020310</span></span>  <br/> |<span data-ttu-id="5cc86-121">特殊フォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="5cc86-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="5cc86-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="5cc86-122">0x00000310</span></span>  <br/> |<span data-ttu-id="5cc86-123">特別なフォルダーではないフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="5cc86-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="5cc86-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="5cc86-124">0x00020500</span></span>  <br/> |<span data-ttu-id="5cc86-125">共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="5cc86-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="5cc86-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="5cc86-126">0x00020710</span></span>  <br/> |<span data-ttu-id="5cc86-127">両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="5cc86-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="5cc86-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="5cc86-128">0x00025100</span></span>  <br/> |<span data-ttu-id="5cc86-129">共有の応答、要求を拒否します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="5cc86-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="5cc86-130">0x00023310</span></span>  <br/> |<span data-ttu-id="5cc86-131">共有の応答 (も一種の共有への招待) の要求を受け入れる。</span><span class="sxs-lookup"><span data-stu-id="5cc86-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5cc86-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5cc86-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cc86-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5cc86-133">Protocol specifications</span></span>

<span data-ttu-id="5cc86-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cc86-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cc86-135">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5cc86-136">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cc86-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cc86-137">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cc86-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5cc86-138">Header files</span></span>

<span data-ttu-id="5cc86-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cc86-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cc86-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5cc86-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cc86-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="5cc86-141">See also</span></span>



[<span data-ttu-id="5cc86-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5cc86-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cc86-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5cc86-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cc86-144">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5cc86-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cc86-145">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5cc86-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

