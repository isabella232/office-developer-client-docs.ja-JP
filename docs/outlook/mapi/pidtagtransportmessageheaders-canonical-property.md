---
title: PidTagTransportMessageHeaders 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 16c3684176de765a10b5bac620ea65a824cfe83a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588763"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="e0dca-103">PidTagTransportMessageHeaders 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dca-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="e0dca-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0dca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0dca-105">トランスポートに固有のメッセージのエンベロープ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0dca-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0dca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e0dca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0dca-107">PR_TRANSPORT_MESSAGE_HEADERS、PR_TRANSPORT_MESSAGE_HEADERS_A、PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="e0dca-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="e0dca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e0dca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0dca-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="e0dca-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="e0dca-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e0dca-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0dca-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0dca-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e0dca-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e0dca-112">Area:</span></span>  <br/> |<span data-ttu-id="e0dca-113">メール</span><span class="sxs-lookup"><span data-stu-id="e0dca-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0dca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e0dca-114">Remarks</span></span>

<span data-ttu-id="e0dca-115">トランスポート プロバイダーは、受信メッセージのメッセージのヘッダー情報を生成できます。</span><span class="sxs-lookup"><span data-stu-id="e0dca-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="e0dca-116">これらのプロパティは、トランスポート メッセージのヘッダー情報を破棄するか、メッセージのテキストに付加することに代わりを提供しています。</span><span class="sxs-lookup"><span data-stu-id="e0dca-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="e0dca-117">クライアントは、情報を表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0dca-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0dca-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e0dca-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0dca-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e0dca-119">Protocol specifications</span></span>

<span data-ttu-id="e0dca-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dca-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0dca-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0dca-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dca-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dca-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0dca-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="e0dca-124">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dca-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dca-125">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="e0dca-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0dca-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e0dca-126">Header files</span></span>

<span data-ttu-id="e0dca-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0dca-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0dca-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0dca-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0dca-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0dca-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e0dca-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0dca-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0dca-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0dca-131">See also</span></span>



[<span data-ttu-id="e0dca-132">PidTagBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dca-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="e0dca-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dca-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0dca-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dca-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0dca-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e0dca-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0dca-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e0dca-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

