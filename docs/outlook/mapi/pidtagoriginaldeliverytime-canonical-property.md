---
title: PidTagOriginalDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391375"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="b95a0-103">PidTagOriginalDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b95a0-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="b95a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b95a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b95a0-105">元のメッセージの配信日時のスレッドでのコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b95a0-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b95a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b95a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b95a0-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="b95a0-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="b95a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b95a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b95a0-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="b95a0-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="b95a0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b95a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b95a0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b95a0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b95a0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b95a0-112">Area:</span></span>  <br/> |<span data-ttu-id="b95a0-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="b95a0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b95a0-114">備考</span><span class="sxs-lookup"><span data-stu-id="b95a0-114">Remarks</span></span>

<span data-ttu-id="b95a0-115">このプロパティはそれ以降の返信または転送操作で元の**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) のプロパティからコピー、読み取りおよび nonread のレポートで使用されています。</span><span class="sxs-lookup"><span data-stu-id="b95a0-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="b95a0-116">配信レポートでは、代わりに**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b95a0-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b95a0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b95a0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b95a0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b95a0-118">Protocol specifications</span></span>

<span data-ttu-id="b95a0-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b95a0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b95a0-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b95a0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b95a0-121">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b95a0-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b95a0-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b95a0-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b95a0-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b95a0-123">Header files</span></span>

<span data-ttu-id="b95a0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b95a0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b95a0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b95a0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b95a0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b95a0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b95a0-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b95a0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b95a0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b95a0-128">See also</span></span>



[<span data-ttu-id="b95a0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b95a0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b95a0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b95a0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b95a0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b95a0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b95a0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b95a0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

