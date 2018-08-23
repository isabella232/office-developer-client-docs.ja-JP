---
title: PidTagReceivedRepresentingAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c57324972f02366822a64e9e6c642d0f22ce158b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563381"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a><span data-ttu-id="27df2-103">PidTagReceivedRepresentingAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27df2-103">PidTagReceivedRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="27df2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27df2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27df2-105">実際にメッセージを受信したユーザーはメッセージング ユーザーのアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27df2-105">Contains the address type for the messaging user who is represented by the user actually receiving the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27df2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="27df2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27df2-107">PR_RCVD_REPRESENTING_ADDRTYPE、PR_RCVD_REPRESENTING_ADDRTYPE_A、PR_RCVD_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="27df2-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="27df2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="27df2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27df2-109">0x0077</span><span class="sxs-lookup"><span data-stu-id="27df2-109">0x0077</span></span>  <br/> |
|<span data-ttu-id="27df2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="27df2-110">Data type:</span></span>  <br/> |<span data-ttu-id="27df2-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="27df2-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="27df2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="27df2-112">Area:</span></span>  <br/> |<span data-ttu-id="27df2-113">Address</span><span class="sxs-lookup"><span data-stu-id="27df2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27df2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="27df2-114">Remarks</span></span>

<span data-ttu-id="27df2-115">これらのプロパティでは、受信側のユーザーによって表現されているメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="27df2-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="27df2-116">承認または代理人の確認を担当するも、受信トランスポート プロバイダーによって設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="27df2-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="27df2-117">表されるは、メッセージング ユーザーがない場合、 **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) のプロパティに含まれているアドレスの種類にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27df2-117">If no messaging user is being represented, this property should be set to the address type contained in the **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="27df2-118">クライアント アプリケーションに返信する他のクライアントの代理として受信したメッセージ、受信したメッセージからの応答を**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) のプロパティにこのプロパティする必要がありますコピーします。</span><span class="sxs-lookup"><span data-stu-id="27df2-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27df2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="27df2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27df2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="27df2-120">Protocol specifications</span></span>

<span data-ttu-id="27df2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="27df2-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27df2-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="27df2-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="27df2-125">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="27df2-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="27df2-127">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="27df2-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="27df2-129">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-130">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="27df2-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="27df2-131">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27df2-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27df2-132">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="27df2-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27df2-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="27df2-133">Header files</span></span>

<span data-ttu-id="27df2-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27df2-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="27df2-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="27df2-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="27df2-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27df2-136">Mapitags.h</span></span>
  
> <span data-ttu-id="27df2-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27df2-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27df2-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="27df2-138">See also</span></span>



[<span data-ttu-id="27df2-139">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27df2-139">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="27df2-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="27df2-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27df2-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="27df2-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27df2-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27df2-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27df2-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="27df2-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

