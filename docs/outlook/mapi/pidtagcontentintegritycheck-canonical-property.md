---
title: PidTagContentIntegrityCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585810"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="65e9c-103">PidTagContentIntegrityCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="65e9c-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="65e9c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65e9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65e9c-105">漏えいから不正な受信者にメッセージの内容を保護するためにメッセージの送信者を許可する ASN.1 のコンテンツの整合性チェック値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="65e9c-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65e9c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="65e9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65e9c-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="65e9c-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="65e9c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="65e9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65e9c-109">場合は 0x0c00。</span><span class="sxs-lookup"><span data-stu-id="65e9c-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="65e9c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="65e9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="65e9c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="65e9c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="65e9c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="65e9c-112">Area:</span></span>  <br/> |<span data-ttu-id="65e9c-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="65e9c-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65e9c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="65e9c-114">Remarks</span></span>

<span data-ttu-id="65e9c-115">このプロパティは、メッセージのコンテンツの否認を提供します。</span><span class="sxs-lookup"><span data-stu-id="65e9c-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="65e9c-116">**PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) と協力して、メッセージの内容がそのまま目的地に到着することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="65e9c-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65e9c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="65e9c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="65e9c-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="65e9c-118">Header files</span></span>

<span data-ttu-id="65e9c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65e9c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="65e9c-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="65e9c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="65e9c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65e9c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="65e9c-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="65e9c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65e9c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="65e9c-123">See also</span></span>



[<span data-ttu-id="65e9c-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="65e9c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65e9c-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="65e9c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65e9c-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="65e9c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65e9c-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="65e9c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

