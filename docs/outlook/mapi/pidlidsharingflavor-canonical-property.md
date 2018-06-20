---
title: PidLidSharingFlavor の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802154"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="1441e-103">PidLidSharingFlavor の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1441e-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="1441e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1441e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1441e-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="1441e-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1441e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1441e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1441e-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="1441e-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="1441e-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1441e-108">Property set:</span></span>  <br/> |<span data-ttu-id="1441e-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="1441e-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="1441e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1441e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1441e-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="1441e-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="1441e-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1441e-112">Data type:</span></span>  <br/> |<span data-ttu-id="1441e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1441e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1441e-114">領域:</span><span class="sxs-lookup"><span data-stu-id="1441e-114">Area:</span></span>  <br/> |<span data-ttu-id="1441e-115">共有</span><span class="sxs-lookup"><span data-stu-id="1441e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1441e-116">備考</span><span class="sxs-lookup"><span data-stu-id="1441e-116">Remarks</span></span>

<span data-ttu-id="1441e-117">このプロパティの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1441e-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="1441e-118">**値**</span><span class="sxs-lookup"><span data-stu-id="1441e-118">**Value**</span></span>|<span data-ttu-id="1441e-119">**メッセージの共有オブジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="1441e-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1441e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="1441e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="1441e-121">特殊フォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="1441e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="1441e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="1441e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="1441e-123">特別なフォルダーではないフォルダーの共有への招待。</span><span class="sxs-lookup"><span data-stu-id="1441e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="1441e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="1441e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="1441e-125">共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="1441e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="1441e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="1441e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="1441e-127">両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。</span><span class="sxs-lookup"><span data-stu-id="1441e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="1441e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="1441e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="1441e-129">共有の応答で要求を拒否します。</span><span class="sxs-lookup"><span data-stu-id="1441e-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="1441e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="1441e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="1441e-131">共有の応答で (も一種の共有への招待) の要求を承諾します。</span><span class="sxs-lookup"><span data-stu-id="1441e-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1441e-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1441e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1441e-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1441e-133">Protocol specifications</span></span>

<span data-ttu-id="1441e-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1441e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1441e-135">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1441e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1441e-136">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1441e-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1441e-137">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="1441e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1441e-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1441e-138">Header files</span></span>

<span data-ttu-id="1441e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1441e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="1441e-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1441e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1441e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="1441e-141">See also</span></span>



[<span data-ttu-id="1441e-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1441e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1441e-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1441e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1441e-144">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1441e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1441e-145">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1441e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

