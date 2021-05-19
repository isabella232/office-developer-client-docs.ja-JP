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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341952"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="75f1e-103">PidTagTnefCorrelationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75f1e-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="75f1e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75f1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75f1e-105">トランスポート ニュートラル カプセル化形式 (TNEF) 添付ファイルとメッセージを関連付ける値を格納します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75f1e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="75f1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75f1e-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="75f1e-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="75f1e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="75f1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75f1e-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="75f1e-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="75f1e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="75f1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="75f1e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75f1e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75f1e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="75f1e-112">Area:</span></span>  <br/> |<span data-ttu-id="75f1e-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="75f1e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75f1e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="75f1e-114">Remarks</span></span>

<span data-ttu-id="75f1e-115">TNEF 添付ファイルサブオブジェクトでこのプロパティを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="75f1e-116">このプロパティは、受信 TNEF ファイルが添付されているメッセージに属するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="75f1e-117">これは、主にトランスポート プロバイダーとゲートウェイによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="75f1e-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="75f1e-118">送信メッセージでは、トランスポート プロバイダーは、そのメッセージに固有のバイナリ値を計算するか、メッセージ識別子などの一意性要件を満たす既存の値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="75f1e-119">トランスポート プロバイダーは、この値をこのプロパティに格納し [、ITnef::AddProps](itnef-addprops.md) メソッドを呼び出してカプセル化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="75f1e-120">メッセージ ヘッダーなど、プロバイダーによって定義された場所にも同じ値をトランスポート エンベロープに格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="75f1e-121">受信メッセージでは、トランスポート プロバイダーは [ITnef::ExtractProps](itnef-extractprops.md) メソッドを呼び出して TNEF 添付ファイルをカプセル化し、このプロパティをトランスポート エンベロープに格納されている値と比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="75f1e-122">値が一致する場合は、TNEF を正常に処理する必要があります。つまり、TNEF 添付ファイルから抽出されたプロパティはすべて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="75f1e-123">値が一致しない場合は、TNEF 添付ファイルのすべてのプロパティを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="75f1e-124">このプロパティを設定しない場合、TNEF ファイルはこのメッセージに属すると見なされ、そこから抽出された他のプロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75f1e-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75f1e-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75f1e-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75f1e-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="75f1e-126">Protocol specifications</span></span>

<span data-ttu-id="75f1e-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75f1e-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75f1e-128">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75f1e-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75f1e-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75f1e-130">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="75f1e-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75f1e-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75f1e-132">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="75f1e-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75f1e-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75f1e-134">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="75f1e-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75f1e-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="75f1e-135">Header files</span></span>

<span data-ttu-id="75f1e-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75f1e-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="75f1e-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75f1e-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="75f1e-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75f1e-138">Mapitags.h</span></span>
  
> <span data-ttu-id="75f1e-139">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="75f1e-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75f1e-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="75f1e-140">See also</span></span>



[<span data-ttu-id="75f1e-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="75f1e-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75f1e-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75f1e-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75f1e-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75f1e-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75f1e-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="75f1e-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

