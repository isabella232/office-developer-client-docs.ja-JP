---
title: PidTagReceivedRepresentingEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEmailAddress
api_type:
- COM
ms.assetid: f85ce31c-f621-47ed-badf-4f59a45ec0a1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 47c2fdf3a48a7c672e7bf1b69d8315675a537e42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803267"
---
# <a name="pidtagreceivedrepresentingemailaddress-canonical-property"></a><span data-ttu-id="3d0e9-103">PidTagReceivedRepresentingEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d0e9-103">PidTagReceivedRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="3d0e9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d0e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d0e9-105">受信側ユーザーはメッセージングのユーザーの電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-105">Contains the email address for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d0e9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3d0e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d0e9-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS、PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A、PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="3d0e9-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="3d0e9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3d0e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d0e9-109">0x0078</span><span class="sxs-lookup"><span data-stu-id="3d0e9-109">0x0078</span></span>  <br/> |
|<span data-ttu-id="3d0e9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3d0e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d0e9-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3d0e9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3d0e9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3d0e9-112">Area:</span></span>  <br/> |<span data-ttu-id="3d0e9-113">Address</span><span class="sxs-lookup"><span data-stu-id="3d0e9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d0e9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3d0e9-114">Remarks</span></span>

<span data-ttu-id="3d0e9-115">これらのプロパティでは、受信側のユーザーによって表現されているメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="3d0e9-116">承認または代理人の確認を担当するも、受信トランスポート プロバイダーによって設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="3d0e9-117">表されるは、メッセージング ユーザーがない場合、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) のプロパティに含まれている電子メール アドレスをこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-117">If no messaging user is being represented, these properties should be set to the email address contained in the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3d0e9-118">別のクライアントの代理として受信したメッセージに返信しようクライアント アプリケーションする必要がありますコピーこれらのプロパティ受信したメッセージからの**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) のプロパティに、返信します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d0e9-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3d0e9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d0e9-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3d0e9-120">Protocol specifications</span></span>

<span data-ttu-id="3d0e9-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d0e9-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="3d0e9-125">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3d0e9-127">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3d0e9-129">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-130">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="3d0e9-131">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0e9-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0e9-132">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d0e9-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d0e9-133">Header files</span></span>

<span data-ttu-id="3d0e9-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d0e9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d0e9-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d0e9-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d0e9-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3d0e9-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d0e9-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d0e9-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d0e9-138">See also</span></span>



[<span data-ttu-id="3d0e9-139">PidTagEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d0e9-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="3d0e9-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d0e9-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d0e9-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d0e9-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d0e9-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3d0e9-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d0e9-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3d0e9-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

