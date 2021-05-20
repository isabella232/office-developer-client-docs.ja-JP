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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439423"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="8ca22-103">PidTagDeliveryPoint 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8ca22-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="8ca22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca22-105">メッセージが受信者に配信された、または配信された可能性のある機能エンティティの性質を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ca22-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ca22-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8ca22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ca22-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="8ca22-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="8ca22-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8ca22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ca22-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="8ca22-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="8ca22-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8ca22-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ca22-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8ca22-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8ca22-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8ca22-112">Area:</span></span>  <br/> |<span data-ttu-id="8ca22-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="8ca22-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ca22-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8ca22-114">Remarks</span></span>

<span data-ttu-id="8ca22-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="8ca22-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="8ca22-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="8ca22-117">配布リストに配信され、配信ポイントがメッセージを多くの受信者に配布する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8ca22-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="8ca22-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="8ca22-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="8ca22-119">受信者に直接配信されるのではなく、メッセージ ストアに配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="8ca22-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="8ca22-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="8ca22-121">FAX システムなどの物理配信アクセス ユニット (PDAU) 以外のアクセス ユニット (AU) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="8ca22-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="8ca22-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="8ca22-123">人間の郵便運送業者などの物理的な配信アクセス ユニットに配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="8ca22-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="8ca22-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="8ca22-125">従来の郵便メールボックスなどの物理的な配信システムのパトロンに配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="8ca22-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="8ca22-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="8ca22-127">プライベート ユーザー エージェント (UA) (インハウス メッセージング システムのクライアントなど) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="8ca22-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="8ca22-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="8ca22-129">パブリック ユーザー エージェントまたはパブリック サービス プロバイダーに配信されます。</span><span class="sxs-lookup"><span data-stu-id="8ca22-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="8ca22-130">既定値は、mapi MAPI_MH_DP_PRIVATE_UA MAPI クライアントの値です。</span><span class="sxs-lookup"><span data-stu-id="8ca22-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ca22-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8ca22-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ca22-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8ca22-132">Header files</span></span>

<span data-ttu-id="8ca22-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ca22-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ca22-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8ca22-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ca22-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ca22-135">Mapitags.h</span></span>
  
> <span data-ttu-id="8ca22-136">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8ca22-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ca22-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ca22-137">See also</span></span>



[<span data-ttu-id="8ca22-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8ca22-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ca22-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8ca22-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ca22-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8ca22-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ca22-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8ca22-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

