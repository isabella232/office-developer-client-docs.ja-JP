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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360761"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="94758-103">PidTagTransportMessageHeaders 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94758-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="94758-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94758-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94758-105">トランスポート固有のメッセージ エンベロープ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94758-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94758-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94758-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94758-107">PR_TRANSPORT_MESSAGE_HEADERS、PR_TRANSPORT_MESSAGE_HEADERS_A、PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="94758-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="94758-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="94758-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94758-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="94758-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="94758-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94758-110">Data type:</span></span>  <br/> |<span data-ttu-id="94758-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94758-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="94758-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="94758-112">Area:</span></span>  <br/> |<span data-ttu-id="94758-113">メール</span><span class="sxs-lookup"><span data-stu-id="94758-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94758-114">注釈</span><span class="sxs-lookup"><span data-stu-id="94758-114">Remarks</span></span>

<span data-ttu-id="94758-115">トランスポート プロバイダーは、受信メッセージのメッセージ ヘッダー情報を生成できます。</span><span class="sxs-lookup"><span data-stu-id="94758-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="94758-116">これらのプロパティは、トランスポート メッセージ ヘッダー情報を破棄するか、メッセージ テキストに事前に保留する代わりに使用できます。</span><span class="sxs-lookup"><span data-stu-id="94758-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="94758-117">クライアントは、情報を表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="94758-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94758-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94758-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94758-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94758-119">Protocol specifications</span></span>

<span data-ttu-id="94758-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94758-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94758-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="94758-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94758-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94758-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94758-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94758-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="94758-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94758-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94758-125">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="94758-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94758-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94758-126">Header files</span></span>

<span data-ttu-id="94758-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94758-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="94758-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94758-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="94758-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94758-129">Mapitags.h</span></span>
  
> <span data-ttu-id="94758-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="94758-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94758-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="94758-131">See also</span></span>



[<span data-ttu-id="94758-132">PidTagBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94758-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="94758-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="94758-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94758-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94758-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94758-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94758-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94758-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="94758-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

