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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327483"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="2554e-103">PidLidSharingFlavor 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2554e-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="2554e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2554e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2554e-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="2554e-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2554e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2554e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2554e-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="2554e-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="2554e-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="2554e-108">Property set:</span></span>  <br/> |<span data-ttu-id="2554e-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="2554e-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="2554e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2554e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2554e-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="2554e-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="2554e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2554e-112">Data type:</span></span>  <br/> |<span data-ttu-id="2554e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2554e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2554e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="2554e-114">Area:</span></span>  <br/> |<span data-ttu-id="2554e-115">共有</span><span class="sxs-lookup"><span data-stu-id="2554e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2554e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2554e-116">Remarks</span></span>

<span data-ttu-id="2554e-117">このプロパティの値は、次のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2554e-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="2554e-118">**値**</span><span class="sxs-lookup"><span data-stu-id="2554e-118">**Value**</span></span>|<span data-ttu-id="2554e-119">**共有メッセージ オブジェクトの種類**</span><span class="sxs-lookup"><span data-stu-id="2554e-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2554e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="2554e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="2554e-121">特別なフォルダーの共有の招待。</span><span class="sxs-lookup"><span data-stu-id="2554e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="2554e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="2554e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="2554e-123">特別なフォルダーではないフォルダーの共有の招待。</span><span class="sxs-lookup"><span data-stu-id="2554e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="2554e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="2554e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="2554e-125">共有要求。</span><span class="sxs-lookup"><span data-stu-id="2554e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="2554e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="2554e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="2554e-127">特別なフォルダーの共有の招待と、受信者と同等の特別なフォルダーの共有要求の両方。</span><span class="sxs-lookup"><span data-stu-id="2554e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="2554e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="2554e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="2554e-129">要求を拒否する共有応答。</span><span class="sxs-lookup"><span data-stu-id="2554e-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="2554e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="2554e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="2554e-131">要求を受け入れる共有応答 (共有招待の種類も含む)。</span><span class="sxs-lookup"><span data-stu-id="2554e-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2554e-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2554e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2554e-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2554e-133">Protocol specifications</span></span>

<span data-ttu-id="2554e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2554e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2554e-135">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="2554e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2554e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2554e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2554e-137">クライアント間でメールボックス フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="2554e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2554e-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2554e-138">Header files</span></span>

<span data-ttu-id="2554e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2554e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="2554e-140">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2554e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2554e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="2554e-141">See also</span></span>



[<span data-ttu-id="2554e-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2554e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2554e-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2554e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2554e-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2554e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2554e-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2554e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

