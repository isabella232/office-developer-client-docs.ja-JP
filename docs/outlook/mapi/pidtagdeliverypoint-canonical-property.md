---
title: PidTagDeliveryPoint の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802687"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="24d63-103">PidTagDeliveryPoint の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="24d63-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="24d63-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24d63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24d63-105">使用して、メッセージまたは受信者に配信されるように機能エンティティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="24d63-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24d63-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="24d63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24d63-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="24d63-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="24d63-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="24d63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24d63-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="24d63-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="24d63-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="24d63-110">Data type:</span></span>  <br/> |<span data-ttu-id="24d63-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24d63-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24d63-112">領域:</span><span class="sxs-lookup"><span data-stu-id="24d63-112">Area:</span></span>  <br/> |<span data-ttu-id="24d63-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="24d63-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24d63-114">備考</span><span class="sxs-lookup"><span data-stu-id="24d63-114">Remarks</span></span>

<span data-ttu-id="24d63-115">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="24d63-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="24d63-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="24d63-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="24d63-117">配布リストに配信、配信は、先に配布することが多くの受信者にメッセージをポイントします。</span><span class="sxs-lookup"><span data-stu-id="24d63-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="24d63-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="24d63-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="24d63-119">代わりに、受信者に直接のメッセージ ・ ストアに配信されます。</span><span class="sxs-lookup"><span data-stu-id="24d63-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="24d63-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="24d63-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="24d63-121">FAX システムなどの物理的な配信アクセス ユニット (PDAU)、以外のアクセス単位 (AU) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="24d63-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="24d63-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="24d63-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="24d63-123">人間の郵便キャリアなどの物理的な配信アクセス ユニットに配信されます。</span><span class="sxs-lookup"><span data-stu-id="24d63-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="24d63-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="24d63-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="24d63-125">従来の郵便番号のメールボックスなどの物理的な配信システムの patron に配信されます。</span><span class="sxs-lookup"><span data-stu-id="24d63-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="24d63-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="24d63-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="24d63-127">社内メッセージング システム内のクライアントなど、プライベートなユーザー エージェント (UA) に配信されます。</span><span class="sxs-lookup"><span data-stu-id="24d63-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="24d63-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="24d63-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="24d63-129">パブリックのユーザー エージェント、またはサービス プロバイダーに提供します。</span><span class="sxs-lookup"><span data-stu-id="24d63-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="24d63-130">既定値は、MAPI_MH_DP_PRIVATE_UA、つまり、MAPI クライアントです。</span><span class="sxs-lookup"><span data-stu-id="24d63-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24d63-131">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24d63-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="24d63-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24d63-132">Header files</span></span>

<span data-ttu-id="24d63-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24d63-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="24d63-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24d63-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="24d63-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24d63-135">Mapitags.h</span></span>
  
> <span data-ttu-id="24d63-136">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="24d63-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24d63-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="24d63-137">See also</span></span>



[<span data-ttu-id="24d63-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24d63-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24d63-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24d63-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24d63-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="24d63-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24d63-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="24d63-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

