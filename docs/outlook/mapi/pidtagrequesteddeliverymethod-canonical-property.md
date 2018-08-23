---
title: PidTagRequestedDeliveryMethod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571368"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="d7f11-103">PidTagRequestedDeliveryMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7f11-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="d7f11-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7f11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7f11-105">このプロパティには、メッセージの送信元の優先順位に従って指定の配送方法 (サービス プロバイダー) のバイナリの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7f11-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7f11-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d7f11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7f11-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="d7f11-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="d7f11-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d7f11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7f11-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="d7f11-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="d7f11-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d7f11-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7f11-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7f11-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7f11-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d7f11-112">Area:</span></span>  <br/> |<span data-ttu-id="d7f11-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="d7f11-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7f11-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d7f11-114">Remarks</span></span>

<span data-ttu-id="d7f11-115">このに含まれている配列の各サービス プロバイダーの ASN.1 識別子のプロパティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d7f11-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7f11-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d7f11-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d7f11-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d7f11-117">Header files</span></span>

<span data-ttu-id="d7f11-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7f11-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7f11-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7f11-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7f11-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7f11-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d7f11-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7f11-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7f11-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7f11-122">See also</span></span>



[<span data-ttu-id="d7f11-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7f11-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7f11-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7f11-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7f11-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7f11-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7f11-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7f11-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

