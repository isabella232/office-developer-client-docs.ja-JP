---
title: PidTagExpiryUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316409"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="adb91-103">PidTagExpiryUnits 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="adb91-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="adb91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adb91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adb91-105">プロパティ [(PidTagExpiryNumber)](pidtagexpirynumber-canonical-property.md)プロパティ **PR_EXPIRY_NUMBER** 乗算する時間の単位を示します。</span><span class="sxs-lookup"><span data-stu-id="adb91-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adb91-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="adb91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adb91-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="adb91-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="adb91-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="adb91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="adb91-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="adb91-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="adb91-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="adb91-110">Data type:</span></span>  <br/> |<span data-ttu-id="adb91-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="adb91-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="adb91-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="adb91-112">Area:</span></span>  <br/> |<span data-ttu-id="adb91-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="adb91-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adb91-114">注釈</span><span class="sxs-lookup"><span data-stu-id="adb91-114">Remarks</span></span>

<span data-ttu-id="adb91-115">このプロパティを設定する場合は、次のいずれかの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adb91-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adb91-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="adb91-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="adb91-117">説明 (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="adb91-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="adb91-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adb91-118">0x00000000</span></span>  <br/> |<span data-ttu-id="adb91-119">分 (60 秒など)</span><span class="sxs-lookup"><span data-stu-id="adb91-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="adb91-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="adb91-120">0x00000001</span></span>  <br/> |<span data-ttu-id="adb91-121">時間 (60x60 秒など)</span><span class="sxs-lookup"><span data-stu-id="adb91-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="adb91-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="adb91-122">0x00000002</span></span>  <br/> |<span data-ttu-id="adb91-123">Day (24x60x60 秒など)</span><span class="sxs-lookup"><span data-stu-id="adb91-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="adb91-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="adb91-124">0x00000003</span></span>  <br/> |<span data-ttu-id="adb91-125">週 (7x24x60x60 秒など)</span><span class="sxs-lookup"><span data-stu-id="adb91-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="adb91-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="adb91-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adb91-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="adb91-127">Protocol specifications</span></span>

<span data-ttu-id="adb91-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adb91-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adb91-129">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="adb91-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adb91-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="adb91-130">Header files</span></span>

<span data-ttu-id="adb91-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adb91-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="adb91-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="adb91-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="adb91-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="adb91-133">Mapitags.h</span></span>
  
> <span data-ttu-id="adb91-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="adb91-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adb91-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="adb91-135">See also</span></span>



[<span data-ttu-id="adb91-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="adb91-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adb91-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="adb91-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adb91-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="adb91-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adb91-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="adb91-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

