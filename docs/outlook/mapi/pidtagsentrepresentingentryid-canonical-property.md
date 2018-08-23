---
title: PidTagSentRepresentingEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1afb34dace1b28053b185bc25a495a19e48ec1c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577822"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="50b5d-103">PidTagSentRepresentingEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50b5d-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="50b5d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50b5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50b5d-105">送信者によって表されるメッセージのユーザーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50b5d-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50b5d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50b5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50b5d-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="50b5d-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="50b5d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="50b5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50b5d-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="50b5d-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="50b5d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50b5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="50b5d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="50b5d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="50b5d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="50b5d-112">Area:</span></span>  <br/> |<span data-ttu-id="50b5d-113">Address</span><span class="sxs-lookup"><span data-stu-id="50b5d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50b5d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="50b5d-114">Remarks</span></span>

<span data-ttu-id="50b5d-115">このプロパティは、メッセージに送信者によって表されるユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="50b5d-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="50b5d-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50b5d-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="50b5d-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="50b5d-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50b5d-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="50b5d-119">設定しない場合は、トランスポート プロバイダーは、必要があります**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) に、メッセージの送信のコピーに設定し、ローカル コピーに設定されていないままです。</span><span class="sxs-lookup"><span data-stu-id="50b5d-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50b5d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50b5d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50b5d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50b5d-121">Protocol specifications</span></span>

<span data-ttu-id="50b5d-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50b5d-124">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="50b5d-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-127">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="50b5d-128">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-129">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="50b5d-130">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-131">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="50b5d-132">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-132">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-133">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="50b5d-134">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b5d-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50b5d-135">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50b5d-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50b5d-136">Header files</span></span>

<span data-ttu-id="50b5d-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50b5d-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="50b5d-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50b5d-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="50b5d-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50b5d-139">Mapitags.h</span></span>
  
> <span data-ttu-id="50b5d-140">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50b5d-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50b5d-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="50b5d-141">See also</span></span>



[<span data-ttu-id="50b5d-142">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50b5d-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="50b5d-143">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50b5d-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50b5d-144">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50b5d-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50b5d-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50b5d-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50b5d-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50b5d-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

