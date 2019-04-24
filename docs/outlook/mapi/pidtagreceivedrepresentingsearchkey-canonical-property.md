---
title: PidTagReceivedRepresentingSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bcf310138e4b43b1cc36a177194f721c401caba6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356820"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="e20e3-103">PidTagReceivedRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e20e3-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="e20e3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e20e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e20e3-105">受信側ユーザーによって表されるメッセージングユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e20e3-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e20e3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e20e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e20e3-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e20e3-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="e20e3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e20e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e20e3-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="e20e3-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="e20e3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e20e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e20e3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e20e3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e20e3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e20e3-112">Area:</span></span>  <br/> |<span data-ttu-id="e20e3-113">Address</span><span class="sxs-lookup"><span data-stu-id="e20e3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e20e3-114">解説</span><span class="sxs-lookup"><span data-stu-id="e20e3-114">Remarks</span></span>

<span data-ttu-id="e20e3-115">このプロパティは、受信側ユーザーによって表されるメッセージングユーザーのアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="e20e3-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="e20e3-116">これは、受信トランスポートプロバイダーによって設定される必要があります。これは、代理人の承認または検証も行います。</span><span class="sxs-lookup"><span data-stu-id="e20e3-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="e20e3-117">メッセージングユーザーが表示されていない場合、このプロパティは**PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) プロパティに含まれる検索キーに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e20e3-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e20e3-118">他のクライアントに代わって受信したメッセージに応答するクライアントアプリケーションは、受信したメッセージから、返信の**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) プロパティにこのプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e20e3-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e20e3-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e20e3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e20e3-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e20e3-120">Protocol specifications</span></span>

<span data-ttu-id="e20e3-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e20e3-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e20e3-125">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-126">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e20e3-127">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-128">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e20e3-129">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-130">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e20e3-131">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e20e3-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e20e3-132">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="e20e3-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e20e3-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e20e3-133">Header files</span></span>

<span data-ttu-id="e20e3-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e20e3-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e20e3-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e20e3-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e20e3-136">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e20e3-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e20e3-137">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e20e3-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e20e3-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="e20e3-138">See also</span></span>



[<span data-ttu-id="e20e3-139">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e20e3-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="e20e3-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e20e3-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e20e3-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e20e3-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e20e3-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e20e3-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e20e3-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e20e3-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

