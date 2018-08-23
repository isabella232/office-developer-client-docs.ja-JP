---
title: PidTagOriginallyIntendedRecipAddrtype 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipAddrtype
api_type:
- COM
ms.assetid: dcfb6bd5-bff5-4a50-aec7-4bdfdabf7631
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9bd7e95b00d27073536d130d443bd20970d48109
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574357"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a><span data-ttu-id="383fd-103">PidTagOriginallyIntendedRecipAddrtype 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="383fd-103">PidTagOriginallyIntendedRecipAddrtype Canonical Property</span></span>

  
  
<span data-ttu-id="383fd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="383fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="383fd-105">自動転送されたメッセージの最初の目的の受信者のアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="383fd-105">Contains the address type of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="383fd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="383fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="383fd-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="383fd-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="383fd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="383fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="383fd-109">0x007B</span><span class="sxs-lookup"><span data-stu-id="383fd-109">0x007B</span></span>  <br/> |
|<span data-ttu-id="383fd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="383fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="383fd-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="383fd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="383fd-112">領域:</span><span class="sxs-lookup"><span data-stu-id="383fd-112">Area:</span></span>  <br/> |<span data-ttu-id="383fd-113">Server</span><span class="sxs-lookup"><span data-stu-id="383fd-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="383fd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="383fd-114">Remarks</span></span>

<span data-ttu-id="383fd-115">これらのプロパティは、本来意図されているメッセージの受信者のアドレスのプロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="383fd-115">These properties are one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="383fd-116">メッセージを転送するには、自動でエージェントを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="383fd-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="383fd-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="383fd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="383fd-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="383fd-118">Header files</span></span>

<span data-ttu-id="383fd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="383fd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="383fd-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="383fd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="383fd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="383fd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="383fd-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="383fd-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="383fd-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="383fd-123">See also</span></span>



[<span data-ttu-id="383fd-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="383fd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="383fd-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="383fd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="383fd-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="383fd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="383fd-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="383fd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

