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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c6aab4228af0f584d96a2a8cc02c5f36e05a01e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569604"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="f2b75-103">PidTagExpiryUnits 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b75-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="f2b75-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2b75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2b75-105">**PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) のプロパティを乗算すると時間の単位について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2b75-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b75-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2b75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2b75-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="f2b75-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="f2b75-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2b75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2b75-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="f2b75-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="f2b75-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2b75-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2b75-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f2b75-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f2b75-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f2b75-112">Area:</span></span>  <br/> |<span data-ttu-id="f2b75-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="f2b75-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2b75-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f2b75-114">Remarks</span></span>

<span data-ttu-id="f2b75-115">このプロパティでは場合は、次の値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2b75-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b75-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="f2b75-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="f2b75-117">説明 (水曜)</span><span class="sxs-lookup"><span data-stu-id="f2b75-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="f2b75-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2b75-118">0x00000000</span></span>  <br/> |<span data-ttu-id="f2b75-119">分、たとえば 60 秒</span><span class="sxs-lookup"><span data-stu-id="f2b75-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="f2b75-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f2b75-120">0x00000001</span></span>  <br/> |<span data-ttu-id="f2b75-121">時間、たとえば 60 × 60 秒</span><span class="sxs-lookup"><span data-stu-id="f2b75-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f2b75-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f2b75-122">0x00000002</span></span>  <br/> |<span data-ttu-id="f2b75-123">日、たとえば 24 x 60 x 60 秒</span><span class="sxs-lookup"><span data-stu-id="f2b75-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f2b75-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="f2b75-124">0x00000003</span></span>  <br/> |<span data-ttu-id="f2b75-125">週、たとえば 7x24x60x60 秒</span><span class="sxs-lookup"><span data-stu-id="f2b75-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f2b75-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2b75-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2b75-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f2b75-127">Protocol specifications</span></span>

<span data-ttu-id="f2b75-128">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2b75-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2b75-129">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2b75-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2b75-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f2b75-130">Header files</span></span>

<span data-ttu-id="f2b75-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2b75-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2b75-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2b75-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2b75-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2b75-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f2b75-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f2b75-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2b75-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2b75-135">See also</span></span>



[<span data-ttu-id="f2b75-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b75-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2b75-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2b75-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2b75-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2b75-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2b75-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2b75-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

