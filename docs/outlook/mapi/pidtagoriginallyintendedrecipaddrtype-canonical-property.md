---
title: PidTagOriginallyIntendedRecipAddrtype の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ddb2a246ca77f751ddd428941cd16da6aa5e286b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803093"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a><span data-ttu-id="37dd3-103">PidTagOriginallyIntendedRecipAddrtype の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="37dd3-103">PidTagOriginallyIntendedRecipAddrtype Canonical Property</span></span>

  
  
<span data-ttu-id="37dd3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37dd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37dd3-105">自動転送されたメッセージの最初の目的の受信者のアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="37dd3-105">Contains the address type of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37dd3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="37dd3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37dd3-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="37dd3-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="37dd3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="37dd3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37dd3-109">0x007B</span><span class="sxs-lookup"><span data-stu-id="37dd3-109">0x007B</span></span>  <br/> |
|<span data-ttu-id="37dd3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="37dd3-110">Data type:</span></span>  <br/> |<span data-ttu-id="37dd3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37dd3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="37dd3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="37dd3-112">Area:</span></span>  <br/> |<span data-ttu-id="37dd3-113">Server</span><span class="sxs-lookup"><span data-stu-id="37dd3-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37dd3-114">備考</span><span class="sxs-lookup"><span data-stu-id="37dd3-114">Remarks</span></span>

<span data-ttu-id="37dd3-115">これらのプロパティは、本来意図されているメッセージの受信者のアドレスのプロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="37dd3-115">These properties are one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="37dd3-116">メッセージを転送するには、自動でエージェントを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="37dd3-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37dd3-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="37dd3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="37dd3-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="37dd3-118">Header files</span></span>

<span data-ttu-id="37dd3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37dd3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="37dd3-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="37dd3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="37dd3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="37dd3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="37dd3-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="37dd3-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37dd3-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="37dd3-123">See also</span></span>



[<span data-ttu-id="37dd3-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="37dd3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37dd3-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="37dd3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37dd3-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="37dd3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37dd3-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="37dd3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

