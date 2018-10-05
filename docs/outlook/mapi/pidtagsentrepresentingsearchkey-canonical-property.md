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
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399544"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="03469-103">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="03469-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="03469-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03469-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03469-105">メッセージに送信者によって表されるユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03469-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03469-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="03469-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03469-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="03469-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="03469-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="03469-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03469-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="03469-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="03469-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="03469-110">Data type:</span></span>  <br/> |<span data-ttu-id="03469-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03469-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03469-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="03469-112">Area:</span></span>  <br/> |<span data-ttu-id="03469-113">Address</span><span class="sxs-lookup"><span data-stu-id="03469-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03469-114">備考</span><span class="sxs-lookup"><span data-stu-id="03469-114">Remarks</span></span>

<span data-ttu-id="03469-115">このプロパティは、送信者によって表現されているメッセージング ユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="03469-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="03469-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03469-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="03469-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="03469-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="03469-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03469-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="03469-119">設定しない場合は、トランスポート プロバイダーは、必要があります**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) に、メッセージの送信のコピーに設定し、ローカル コピーに設定されていないままです。</span><span class="sxs-lookup"><span data-stu-id="03469-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03469-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="03469-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03469-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="03469-121">Protocol specifications</span></span>

<span data-ttu-id="03469-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="03469-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03469-124">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03469-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="03469-126">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-127">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="03469-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="03469-128">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-129">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="03469-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="03469-130">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-131">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03469-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="03469-132">[[MS OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-133">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03469-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="03469-134">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03469-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03469-135">プロパティは、連絡先と個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03469-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03469-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="03469-136">Header files</span></span>

<span data-ttu-id="03469-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03469-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="03469-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="03469-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="03469-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03469-139">Mapitags.h</span></span>
  
> <span data-ttu-id="03469-140">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03469-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03469-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="03469-141">See also</span></span>



[<span data-ttu-id="03469-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03469-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03469-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03469-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03469-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03469-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03469-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03469-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

