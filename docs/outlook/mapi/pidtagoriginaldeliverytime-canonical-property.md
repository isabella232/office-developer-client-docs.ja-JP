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
ms.openlocfilehash: cd8c44923e64fcea4464f758389db05bb6b7e374
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803053"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="e57de-103">PidTagOriginalDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e57de-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="e57de-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e57de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e57de-105">元のメッセージの配信日時のスレッドでのコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e57de-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e57de-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e57de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e57de-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="e57de-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="e57de-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e57de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e57de-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="e57de-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="e57de-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e57de-110">Data type:</span></span>  <br/> |<span data-ttu-id="e57de-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e57de-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e57de-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e57de-112">Area:</span></span>  <br/> |<span data-ttu-id="e57de-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="e57de-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e57de-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e57de-114">Remarks</span></span>

<span data-ttu-id="e57de-115">このプロパティはそれ以降の返信または転送操作で元の**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) のプロパティからコピー、読み取りおよび nonread のレポートで使用されています。</span><span class="sxs-lookup"><span data-stu-id="e57de-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="e57de-116">配信レポートでは、代わりに**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e57de-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e57de-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e57de-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e57de-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e57de-118">Protocol specifications</span></span>

<span data-ttu-id="e57de-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e57de-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e57de-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e57de-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e57de-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e57de-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e57de-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e57de-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e57de-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e57de-123">Header files</span></span>

<span data-ttu-id="e57de-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e57de-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e57de-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e57de-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e57de-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e57de-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e57de-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e57de-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e57de-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e57de-128">See also</span></span>



[<span data-ttu-id="e57de-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e57de-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e57de-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e57de-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e57de-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e57de-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e57de-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e57de-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

