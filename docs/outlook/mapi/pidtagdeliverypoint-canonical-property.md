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
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360880"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="69389-103">PidTagDeliveryPoint 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69389-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="69389-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69389-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69389-105">機能エンティティの性質を指定します。これにより、メッセージが受信者に配信されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="69389-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69389-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="69389-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69389-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="69389-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="69389-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="69389-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69389-109">0x0c07</span><span class="sxs-lookup"><span data-stu-id="69389-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="69389-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="69389-110">Data type:</span></span>  <br/> |<span data-ttu-id="69389-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69389-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69389-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="69389-112">Area:</span></span>  <br/> |<span data-ttu-id="69389-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="69389-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69389-114">解説</span><span class="sxs-lookup"><span data-stu-id="69389-114">Remarks</span></span>

<span data-ttu-id="69389-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="69389-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="69389-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="69389-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="69389-117">配布リストに配信されます。この配信ポイントによって、メッセージが多数の受信者に配布される場合があります。</span><span class="sxs-lookup"><span data-stu-id="69389-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="69389-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="69389-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="69389-119">受信者に直接配信される代わりに、メッセージストアに配信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="69389-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="69389-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="69389-121">FAX システムなどの物理的な配信アクセス装置 (pdau) 以外のアクセスユニット (au) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="69389-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="69389-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="69389-123">ユーザーは、実際の郵便電話会社などの物理的な配信アクセス単位に配信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="69389-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="69389-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="69389-125">従来の郵便メールボックスのような、物理的な配信システムの場合に送信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="69389-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="69389-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="69389-127">社内メッセージングシステムのクライアントなど、プライベートユーザーエージェント (UA) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="69389-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="69389-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="69389-129">パブリックユーザーエージェントまたはパブリックサービスプロバイダに配信されます。</span><span class="sxs-lookup"><span data-stu-id="69389-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="69389-130">既定値は MAPI_MH_DP_PRIVATE_UA です。つまり、MAPI クライアントです。</span><span class="sxs-lookup"><span data-stu-id="69389-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69389-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69389-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="69389-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="69389-132">Header files</span></span>

<span data-ttu-id="69389-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69389-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="69389-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69389-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="69389-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="69389-135">Mapitags.h</span></span>
  
> <span data-ttu-id="69389-136">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="69389-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69389-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="69389-137">See also</span></span>



[<span data-ttu-id="69389-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="69389-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69389-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69389-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69389-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69389-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69389-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69389-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

