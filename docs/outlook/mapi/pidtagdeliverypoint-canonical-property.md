---
title: PidTagDeliveryPoint 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d8157c761cd21d5c8fcdf04948646d8102e774a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580139"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="062a4-103">PidTagDeliveryPoint 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="062a4-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="062a4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="062a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="062a4-105">使用して、メッセージまたは受信者に配信されるように機能エンティティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="062a4-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="062a4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="062a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="062a4-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="062a4-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="062a4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="062a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="062a4-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="062a4-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="062a4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="062a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="062a4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="062a4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="062a4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="062a4-112">Area:</span></span>  <br/> |<span data-ttu-id="062a4-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="062a4-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="062a4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="062a4-114">Remarks</span></span>

<span data-ttu-id="062a4-115">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="062a4-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="062a4-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="062a4-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="062a4-117">配布リストに配信、配信は、先に配布することが多くの受信者にメッセージをポイントします。</span><span class="sxs-lookup"><span data-stu-id="062a4-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="062a4-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="062a4-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="062a4-119">代わりに、受信者に直接のメッセージ ・ ストアに配信されます。</span><span class="sxs-lookup"><span data-stu-id="062a4-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="062a4-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="062a4-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="062a4-121">FAX システムなどの物理的な配信アクセス ユニット (PDAU)、以外のアクセス単位 (AU) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="062a4-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="062a4-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="062a4-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="062a4-123">人間の郵便キャリアなどの物理的な配信アクセス ユニットに配信されます。</span><span class="sxs-lookup"><span data-stu-id="062a4-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="062a4-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="062a4-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="062a4-125">従来の郵便番号のメールボックスなどの物理的な配信システムの patron に配信されます。</span><span class="sxs-lookup"><span data-stu-id="062a4-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="062a4-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="062a4-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="062a4-127">社内メッセージング システム内のクライアントなど、プライベートなユーザー エージェント (UA) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="062a4-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="062a4-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="062a4-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="062a4-129">パブリックのユーザー エージェント、またはサービス プロバイダーに提供します。</span><span class="sxs-lookup"><span data-stu-id="062a4-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="062a4-130">既定値は、MAPI_MH_DP_PRIVATE_UA、つまり、MAPI クライアントです。</span><span class="sxs-lookup"><span data-stu-id="062a4-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="062a4-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="062a4-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="062a4-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="062a4-132">Header files</span></span>

<span data-ttu-id="062a4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="062a4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="062a4-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="062a4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="062a4-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="062a4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="062a4-136">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="062a4-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="062a4-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="062a4-137">See also</span></span>



[<span data-ttu-id="062a4-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="062a4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="062a4-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="062a4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="062a4-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="062a4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="062a4-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="062a4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

