---
title: PidTagSentRepresentingSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: afb50c2aaffd507cb269b80f1fb59f548685f2cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564921"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="c187e-103">PidTagSentRepresentingSmtpAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c187e-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="c187e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c187e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c187e-105">送信者はメッセージのユーザーの簡易メール転送プロトコル (SMTP) 電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c187e-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c187e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c187e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c187e-107">PR_SENT_REPRESENTING_SMTP_ADDRESS、PR_SENT_REPRESENTING_SMTP_ADDRESS_A、PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="c187e-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="c187e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c187e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c187e-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="c187e-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="c187e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c187e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c187e-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c187e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c187e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c187e-112">Area:</span></span>  <br/> |<span data-ttu-id="c187e-113">Address</span><span class="sxs-lookup"><span data-stu-id="c187e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c187e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c187e-114">Remarks</span></span>

<span data-ttu-id="c187e-115">このプロパティは、メッセージに送信者によって表されるユーザーのアドレスのプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="c187e-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="c187e-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c187e-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="c187e-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="c187e-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="c187e-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c187e-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="c187e-119">設定しない場合は、トランスポート プロバイダーは、必要がありますプロパティを設定する**PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md))、メッセージの送信のコピーとローカル コピーに設定されていないまま。</span><span class="sxs-lookup"><span data-stu-id="c187e-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c187e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c187e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c187e-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c187e-121">Protocol specifications</span></span>

<span data-ttu-id="c187e-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c187e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c187e-124">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c187e-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c187e-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-127">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="c187e-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c187e-128">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-129">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="c187e-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c187e-130">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-131">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="c187e-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c187e-132">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-133">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="c187e-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="c187e-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-135">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c187e-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="c187e-136">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c187e-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c187e-137">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="c187e-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c187e-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c187e-138">Header files</span></span>

<span data-ttu-id="c187e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c187e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="c187e-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c187e-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="c187e-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c187e-141">Mapitags.h</span></span>
  
> <span data-ttu-id="c187e-142">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c187e-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c187e-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="c187e-143">See also</span></span>



[<span data-ttu-id="c187e-144">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c187e-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c187e-145">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c187e-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c187e-146">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c187e-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c187e-147">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c187e-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

