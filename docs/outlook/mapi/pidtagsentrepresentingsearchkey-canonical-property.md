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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356687"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="2a7cd-103">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a7cd-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2a7cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a7cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a7cd-105">送信者によって表されるメッセージングユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a7cd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2a7cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a7cd-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2a7cd-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2a7cd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2a7cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a7cd-109">0x003b</span><span class="sxs-lookup"><span data-stu-id="2a7cd-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="2a7cd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2a7cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a7cd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a7cd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a7cd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2a7cd-112">Area:</span></span>  <br/> |<span data-ttu-id="2a7cd-113">Address</span><span class="sxs-lookup"><span data-stu-id="2a7cd-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a7cd-114">解説</span><span class="sxs-lookup"><span data-stu-id="2a7cd-114">Remarks</span></span>

<span data-ttu-id="2a7cd-115">このプロパティは、送信者が表すメッセージングユーザーのアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="2a7cd-116">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、表示されているすべての sender プロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="2a7cd-117">通常、メッセージングユーザーが自分の代わりに送信すると、表示される sender プロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="2a7cd-118">送信側クライアントによって設定されている場合、送信トランスポートプロバイダーは常にこのプロパティを変更しないでおく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="2a7cd-119">設定されていない場合、トランスポートプロバイダーは、メッセージの送信コピーで**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) に設定し、ローカルコピー上の設定を解除したままにします。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a7cd-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2a7cd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a7cd-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2a7cd-121">Protocol specifications</span></span>

<span data-ttu-id="2a7cd-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a7cd-124">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-125">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="2a7cd-126">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-127">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="2a7cd-128">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-129">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2a7cd-130">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-131">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="2a7cd-132">[[OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-133">post オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="2a7cd-134">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a7cd-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a7cd-135">連絡先と個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a7cd-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2a7cd-136">Header files</span></span>

<span data-ttu-id="2a7cd-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a7cd-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a7cd-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a7cd-139">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2a7cd-139">Mapitags.h</span></span>
  
> <span data-ttu-id="2a7cd-140">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a7cd-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a7cd-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a7cd-141">See also</span></span>



[<span data-ttu-id="2a7cd-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2a7cd-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a7cd-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a7cd-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a7cd-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a7cd-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a7cd-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a7cd-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

