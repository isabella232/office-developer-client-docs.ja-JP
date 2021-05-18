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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360887"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="49304-103">PidNameXSharingFlavor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49304-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="49304-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49304-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49304-105">**dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="49304-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49304-106">分名:</span><span class="sxs-lookup"><span data-stu-id="49304-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="49304-107">なし</span><span class="sxs-lookup"><span data-stu-id="49304-107">None</span></span>  <br/> |
|<span data-ttu-id="49304-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="49304-108">Property set:</span></span>  <br/> |<span data-ttu-id="49304-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="49304-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="49304-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="49304-110">Property name:</span></span>  <br/> |<span data-ttu-id="49304-111">X-Sharing-Flavor</span><span class="sxs-lookup"><span data-stu-id="49304-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="49304-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="49304-112">Data type:</span></span>  <br/> |<span data-ttu-id="49304-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49304-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49304-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="49304-114">Area:</span></span>  <br/> |<span data-ttu-id="49304-115">共有</span><span class="sxs-lookup"><span data-stu-id="49304-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49304-116">注釈</span><span class="sxs-lookup"><span data-stu-id="49304-116">Remarks</span></span>

<span data-ttu-id="49304-117">**dispidSharingFlavor** プロパティは、次のいずれかの値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="49304-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="49304-118">**値**</span><span class="sxs-lookup"><span data-stu-id="49304-118">**Value**</span></span>|<span data-ttu-id="49304-119">**共有メッセージの種類**</span><span class="sxs-lookup"><span data-stu-id="49304-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49304-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="49304-120">0x00020310</span></span>  <br/> |<span data-ttu-id="49304-121">特別なフォルダーの共有の招待。</span><span class="sxs-lookup"><span data-stu-id="49304-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="49304-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="49304-122">0x00000310</span></span>  <br/> |<span data-ttu-id="49304-123">特別なフォルダーではないフォルダーの共有の招待。</span><span class="sxs-lookup"><span data-stu-id="49304-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="49304-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="49304-124">0x00020500</span></span>  <br/> |<span data-ttu-id="49304-125">共有要求。</span><span class="sxs-lookup"><span data-stu-id="49304-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="49304-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="49304-126">0x00020710</span></span>  <br/> |<span data-ttu-id="49304-127">特別なフォルダーの共有の招待と、受信者と同等の特別なフォルダーの共有要求の両方。</span><span class="sxs-lookup"><span data-stu-id="49304-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="49304-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="49304-128">0x00025100</span></span>  <br/> |<span data-ttu-id="49304-129">要求を拒否する共有応答。</span><span class="sxs-lookup"><span data-stu-id="49304-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="49304-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="49304-130">0x00023310</span></span>  <br/> |<span data-ttu-id="49304-131">要求 (共有招待の種類) を受け入れる共有応答。</span><span class="sxs-lookup"><span data-stu-id="49304-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="49304-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="49304-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49304-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="49304-133">Protocol specifications</span></span>

<span data-ttu-id="49304-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49304-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49304-135">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="49304-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49304-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49304-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49304-137">クライアント間でメールボックス フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="49304-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49304-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="49304-138">Header files</span></span>

<span data-ttu-id="49304-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49304-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="49304-140">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="49304-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49304-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="49304-141">See also</span></span>



[<span data-ttu-id="49304-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="49304-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49304-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49304-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49304-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="49304-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49304-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="49304-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

