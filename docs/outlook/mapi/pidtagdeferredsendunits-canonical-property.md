---
title: PidTagDeferredSendUnits の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 14b1b424bc55a3a8c898eaac386a5344c2e5cf99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802659"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="f849b-103">PidTagDeferredSendUnits の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f849b-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="f849b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f849b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f849b-105">**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) のプロパティ値の乗算する時間の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="f849b-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f849b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f849b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f849b-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="f849b-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="f849b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f849b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f849b-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="f849b-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="f849b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f849b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f849b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f849b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f849b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f849b-112">Area:</span></span>  <br/> |<span data-ttu-id="f849b-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="f849b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f849b-114">備考</span><span class="sxs-lookup"><span data-stu-id="f849b-114">Remarks</span></span>

<span data-ttu-id="f849b-115">かどうかこのオプションを設定すると、このプロパティには次の値のいずれか。</span><span class="sxs-lookup"><span data-stu-id="f849b-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f849b-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="f849b-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="f849b-117">説明</span><span class="sxs-lookup"><span data-stu-id="f849b-117">Description</span></span>  <br/> |
|<span data-ttu-id="f849b-118">0</span><span class="sxs-lookup"><span data-stu-id="f849b-118">0</span></span>  <br/> |<span data-ttu-id="f849b-119">分、たとえば 60 秒</span><span class="sxs-lookup"><span data-stu-id="f849b-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="f849b-120">1</span><span class="sxs-lookup"><span data-stu-id="f849b-120">1</span></span>  <br/> |<span data-ttu-id="f849b-121">時間、たとえば 60 × 60 秒</span><span class="sxs-lookup"><span data-stu-id="f849b-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f849b-122">2</span><span class="sxs-lookup"><span data-stu-id="f849b-122">2</span></span>  <br/> |<span data-ttu-id="f849b-123">日、たとえば 24 x 60 x 60 秒</span><span class="sxs-lookup"><span data-stu-id="f849b-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f849b-124">3</span><span class="sxs-lookup"><span data-stu-id="f849b-124">3</span></span>  <br/> |<span data-ttu-id="f849b-125">週、たとえば 7x24x60x60 秒</span><span class="sxs-lookup"><span data-stu-id="f849b-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f849b-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f849b-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f849b-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f849b-127">Protocol specifications</span></span>

<span data-ttu-id="f849b-128">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f849b-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f849b-129">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f849b-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f849b-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f849b-130">Header files</span></span>

<span data-ttu-id="f849b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f849b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f849b-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f849b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f849b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f849b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f849b-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f849b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f849b-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="f849b-135">See also</span></span>



[<span data-ttu-id="f849b-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f849b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f849b-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f849b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f849b-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f849b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f849b-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f849b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

