---
title: PidTagSentRepresentingAddressType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a58ae878ba13415823e61db3b1717e3cf07f29c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803518"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="f1952-103">PidTagSentRepresentingAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f1952-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="f1952-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1952-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1952-105">送信者によって表される、メッセージング ユーザーのアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1952-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1952-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f1952-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1952-107">PR_SENT_REPRESENTING_ADDRTYPE、PR_SENT_REPRESENTING_ADDRTYPE_A、PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="f1952-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="f1952-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f1952-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1952-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="f1952-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="f1952-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f1952-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1952-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f1952-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f1952-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f1952-112">Area:</span></span>  <br/> |<span data-ttu-id="f1952-113">Address</span><span class="sxs-lookup"><span data-stu-id="f1952-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1952-114">備考</span><span class="sxs-lookup"><span data-stu-id="f1952-114">Remarks</span></span>

<span data-ttu-id="f1952-115">これらのプロパティでは、送信者によって表されるメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="f1952-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="f1952-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1952-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="f1952-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="f1952-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="f1952-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1952-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="f1952-119">設定しない場合は、トランスポート プロバイダーは、必要がありますプロパティを設定する**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))、メッセージの送信のコピーとローカル コピーに設定されていないまま。</span><span class="sxs-lookup"><span data-stu-id="f1952-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1952-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f1952-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1952-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f1952-121">Protocol specifications</span></span>

<span data-ttu-id="f1952-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1952-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1952-124">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-125">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="f1952-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f1952-126">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="f1952-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f1952-128">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="f1952-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f1952-130">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-131">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="f1952-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f1952-132">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-133">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1952-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f1952-134">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-135">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1952-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="f1952-136">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-137">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1952-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="f1952-138">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1952-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1952-139">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="f1952-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1952-140">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f1952-140">Header files</span></span>

<span data-ttu-id="f1952-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1952-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1952-142">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1952-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1952-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1952-143">Mapitags.h</span></span>
  
> <span data-ttu-id="f1952-144">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1952-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1952-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1952-145">See also</span></span>



[<span data-ttu-id="f1952-146">PidTagAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f1952-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="f1952-147">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1952-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1952-148">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1952-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1952-149">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f1952-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1952-150">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f1952-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

