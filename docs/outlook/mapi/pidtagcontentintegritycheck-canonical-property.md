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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331893"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="d60ec-103">PidTagContentIntegrityCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d60ec-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="d60ec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d60ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d60ec-105">メッセージの送信者がメッセージの内容を漏洩から権限のない受信者に保護できるようにする、ASN. 1 コンテンツの整合性チェック値を格納します。</span><span class="sxs-lookup"><span data-stu-id="d60ec-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d60ec-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d60ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d60ec-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="d60ec-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="d60ec-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d60ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d60ec-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="d60ec-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="d60ec-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d60ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="d60ec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d60ec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d60ec-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d60ec-112">Area:</span></span>  <br/> |<span data-ttu-id="d60ec-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="d60ec-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d60ec-114">解説</span><span class="sxs-lookup"><span data-stu-id="d60ec-114">Remarks</span></span>

<span data-ttu-id="d60ec-115">このプロパティは、メッセージコンテンツの否認不可を提供します。</span><span class="sxs-lookup"><span data-stu-id="d60ec-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="d60ec-116">**PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) と組み合わせて使用することにより、メッセージの内容がその宛先に変更されないようにします。</span><span class="sxs-lookup"><span data-stu-id="d60ec-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d60ec-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d60ec-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d60ec-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d60ec-118">Header files</span></span>

<span data-ttu-id="d60ec-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d60ec-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d60ec-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d60ec-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d60ec-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d60ec-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d60ec-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d60ec-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d60ec-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d60ec-123">See also</span></span>



[<span data-ttu-id="d60ec-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d60ec-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d60ec-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d60ec-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d60ec-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d60ec-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d60ec-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d60ec-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

