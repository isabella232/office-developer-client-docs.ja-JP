---
title: PidTagDeferredDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b33d3d26c9369bd0a0e18cdf9e4b8ca850666657
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584871"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="c54f5-103">PidTagDeferredDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c54f5-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c54f5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c54f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c54f5-105">日付と時刻のメッセージの送信者がメッセージの配信を希望する場合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c54f5-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c54f5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c54f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c54f5-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="c54f5-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="c54f5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c54f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c54f5-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="c54f5-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="c54f5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c54f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c54f5-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c54f5-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c54f5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c54f5-112">Area:</span></span>  <br/> |<span data-ttu-id="c54f5-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="c54f5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c54f5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c54f5-114">Remarks</span></span>

<span data-ttu-id="c54f5-115">MAPI は、遅延配信を行いません。遅延配信を処理するには、基になるメッセージング システムのオプションです。</span><span class="sxs-lookup"><span data-stu-id="c54f5-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c54f5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c54f5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c54f5-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c54f5-117">Protocol specifications</span></span>

<span data-ttu-id="c54f5-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c54f5-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c54f5-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c54f5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c54f5-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c54f5-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c54f5-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c54f5-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c54f5-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c54f5-122">Header files</span></span>

<span data-ttu-id="c54f5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c54f5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c54f5-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c54f5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c54f5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c54f5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c54f5-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c54f5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c54f5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c54f5-127">See also</span></span>



[<span data-ttu-id="c54f5-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c54f5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c54f5-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c54f5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c54f5-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c54f5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c54f5-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c54f5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

