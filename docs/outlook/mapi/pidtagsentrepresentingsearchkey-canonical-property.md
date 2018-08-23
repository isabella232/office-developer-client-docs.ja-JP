---
title: PidTagSentRepresentingSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d18a595a1019c3bd583ef0c38ee5cbe0d497bf93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803516"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="e66bc-103">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e66bc-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="e66bc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e66bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e66bc-105">メッセージに送信者によって表されるユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e66bc-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e66bc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e66bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e66bc-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e66bc-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="e66bc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e66bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e66bc-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="e66bc-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="e66bc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e66bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="e66bc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e66bc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e66bc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e66bc-112">Area:</span></span>  <br/> |<span data-ttu-id="e66bc-113">Address</span><span class="sxs-lookup"><span data-stu-id="e66bc-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e66bc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e66bc-114">Remarks</span></span>

<span data-ttu-id="e66bc-115">このプロパティは、送信者によって表現されているメッセージング ユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="e66bc-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="e66bc-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e66bc-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="e66bc-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="e66bc-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e66bc-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="e66bc-119">設定しない場合は、トランスポート プロバイダーは、必要があります**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) に、メッセージの送信のコピーに設定し、ローカル コピーに設定されていないままです。</span><span class="sxs-lookup"><span data-stu-id="e66bc-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e66bc-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e66bc-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e66bc-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e66bc-121">Protocol specifications</span></span>

<span data-ttu-id="e66bc-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e66bc-124">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e66bc-126">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-127">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e66bc-128">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-129">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e66bc-130">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-131">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e66bc-132">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-133">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="e66bc-134">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e66bc-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e66bc-135">プロパティは、連絡先と個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e66bc-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e66bc-136">Header files</span></span>

<span data-ttu-id="e66bc-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e66bc-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e66bc-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e66bc-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="e66bc-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e66bc-139">Mapitags.h</span></span>
  
> <span data-ttu-id="e66bc-140">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e66bc-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e66bc-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="e66bc-141">See also</span></span>



[<span data-ttu-id="e66bc-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e66bc-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e66bc-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e66bc-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e66bc-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e66bc-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e66bc-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e66bc-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

