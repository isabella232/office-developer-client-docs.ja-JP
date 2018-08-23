---
title: PidTagTnefCorrelationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803633"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="19361-103">PidTagTnefCorrelationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="19361-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="19361-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19361-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19361-105">メッセージ トランスポート ニュートラル カプセル化形式 (TNEF) の添付ファイルを対応する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="19361-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19361-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="19361-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19361-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="19361-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="19361-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="19361-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19361-109">0x007f まで</span><span class="sxs-lookup"><span data-stu-id="19361-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="19361-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="19361-110">Data type:</span></span>  <br/> |<span data-ttu-id="19361-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="19361-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="19361-112">領域:</span><span class="sxs-lookup"><span data-stu-id="19361-112">Area:</span></span>  <br/> |<span data-ttu-id="19361-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="19361-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19361-114">注釈</span><span class="sxs-lookup"><span data-stu-id="19361-114">Remarks</span></span>

<span data-ttu-id="19361-115">TNEF の添付ファイルのサブ オブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="19361-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="19361-116">このプロパティは、接続しているメッセージを受信の TNEF ファイルが属しているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="19361-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="19361-117">トランスポート プロバイダーおよびゲートウェイによって主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="19361-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="19361-118">送信メッセージでは、トランスポート プロバイダーは、そのメッセージに一意のバイナリ値を計算またはメッセージ id など、一意性の必要条件を満たす既存の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="19361-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="19361-119">トランスポート プロバイダーは、このプロパティにこの値を格納し、それをカプセル化する[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="19361-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="19361-120">同じ値は、メッセージ ヘッダーなど、プロバイダーによって定義された場所にトランスポート エンベロープにも保存されます。</span><span class="sxs-lookup"><span data-stu-id="19361-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="19361-121">受信メッセージでは、トランスポート プロバイダーは、必要があります TNEF 添付ファイルをカプセル化解除する[ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出すし、トランスポート エンベロープに格納されている値にこのプロパティを比較します。</span><span class="sxs-lookup"><span data-stu-id="19361-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="19361-122">値が一致した場合は、TNEF を正常に処理する必要がありますは、TNEF 添付ファイルから抽出されたすべてのプロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19361-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="19361-123">値が一致しない場合は、TNEF の添付ファイルからのすべてのプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="19361-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="19361-124">このプロパティが設定されていない場合に属しているこのメッセージの TNEF ファイルを考慮する必要があり、そこから抽出された他のプロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19361-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19361-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="19361-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19361-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="19361-126">Protocol specifications</span></span>

<span data-ttu-id="19361-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19361-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19361-128">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="19361-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19361-129">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19361-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19361-130">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="19361-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="19361-131">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19361-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19361-132">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="19361-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="19361-133">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19361-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19361-134">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="19361-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19361-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="19361-135">Header files</span></span>

<span data-ttu-id="19361-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19361-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="19361-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="19361-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="19361-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19361-138">Mapitags.h</span></span>
  
> <span data-ttu-id="19361-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="19361-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19361-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="19361-140">See also</span></span>



[<span data-ttu-id="19361-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="19361-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19361-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="19361-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19361-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="19361-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19361-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="19361-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

