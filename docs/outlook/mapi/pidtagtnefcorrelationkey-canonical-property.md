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
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341952"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="1a6ee-103">PidTagTnefCorrelationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a6ee-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="1a6ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a6ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a6ee-105">トランスポートニュートラルカプセル化形式 (TNEF) 添付ファイルをメッセージに関連付ける値を格納します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a6ee-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1a6ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a6ee-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="1a6ee-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="1a6ee-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1a6ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a6ee-109">0x007f</span><span class="sxs-lookup"><span data-stu-id="1a6ee-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="1a6ee-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1a6ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a6ee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a6ee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a6ee-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1a6ee-112">Area:</span></span>  <br/> |<span data-ttu-id="1a6ee-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="1a6ee-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a6ee-114">解説</span><span class="sxs-lookup"><span data-stu-id="1a6ee-114">Remarks</span></span>

<span data-ttu-id="1a6ee-115">TNEF 添付サブオブジェクトは、このプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="1a6ee-116">このプロパティは、受信 TNEF ファイルが添付されるメッセージに属するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="1a6ee-117">これは主にトランスポートプロバイダーとゲートウェイによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="1a6ee-118">送信メッセージでは、トランスポートプロバイダーはそのメッセージに固有のバイナリ値を計算するか、またはメッセージ識別子などの一意性要件を満たす既存の値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="1a6ee-119">トランスポートプロバイダーは、この値をこのプロパティに格納し、 [ITnef:: addprops](itnef-addprops.md)メソッドを呼び出してカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="1a6ee-120">トランスポートエンベロープには、メッセージヘッダーなどのプロバイダーによって定義された場所に、同じ値も格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="1a6ee-121">受信メッセージでは、トランスポートプロバイダーは[ITnef:: ExtractProps](itnef-extractprops.md)メソッドを呼び出して TNEF 添付ファイルを decapsulate し、このプロパティをトランスポートエンベロープに格納されている値と比較します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="1a6ee-122">値が一致する場合、tnef は正常に処理される必要があります。つまり、tnef 添付から抽出されたすべてのプロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="1a6ee-123">値が一致しない場合は、TNEF 添付ファイルのすべてのプロパティを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="1a6ee-124">このプロパティが設定されていない場合、TNEF ファイルはこのメッセージに属するものと見なされる必要があり、それから抽出されたその他のプロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a6ee-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a6ee-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a6ee-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1a6ee-126">Protocol specifications</span></span>

<span data-ttu-id="1a6ee-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a6ee-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a6ee-128">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a6ee-129">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a6ee-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a6ee-130">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1a6ee-131">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a6ee-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a6ee-132">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="1a6ee-133">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a6ee-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a6ee-134">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a6ee-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1a6ee-135">Header files</span></span>

<span data-ttu-id="1a6ee-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a6ee-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a6ee-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a6ee-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1a6ee-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1a6ee-139">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a6ee-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a6ee-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a6ee-140">See also</span></span>



[<span data-ttu-id="1a6ee-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1a6ee-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a6ee-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a6ee-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a6ee-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a6ee-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a6ee-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a6ee-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

