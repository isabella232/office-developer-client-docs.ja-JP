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
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359088"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="c85f9-103">PidTagSentRepresentingEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85f9-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c85f9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c85f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c85f9-105">送信者によって表されるメッセージングユーザーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="c85f9-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c85f9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c85f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c85f9-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c85f9-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c85f9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c85f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c85f9-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="c85f9-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="c85f9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c85f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="c85f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c85f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c85f9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c85f9-112">Area:</span></span>  <br/> |<span data-ttu-id="c85f9-113">Address</span><span class="sxs-lookup"><span data-stu-id="c85f9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c85f9-114">解説</span><span class="sxs-lookup"><span data-stu-id="c85f9-114">Remarks</span></span>

<span data-ttu-id="c85f9-115">このプロパティは、送信者が表すメッセージングユーザーのアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="c85f9-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="c85f9-116">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、表示されているすべての sender プロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c85f9-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="c85f9-117">通常、メッセージングユーザーが自分の代わりに送信すると、表示される sender プロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="c85f9-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="c85f9-118">送信側クライアントによって設定されている場合、送信トランスポートプロバイダーは常にこのプロパティを変更しないでおく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c85f9-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="c85f9-119">設定されていない場合、トランスポートプロバイダーは、メッセージの送信コピーで**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) に設定し、ローカルコピー上の設定を解除したままにします。</span><span class="sxs-lookup"><span data-stu-id="c85f9-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c85f9-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c85f9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c85f9-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c85f9-121">Protocol specifications</span></span>

<span data-ttu-id="c85f9-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c85f9-124">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-125">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c85f9-126">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-127">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c85f9-128">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-129">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c85f9-130">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-131">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c85f9-132">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-133">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c85f9-134">[[OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85f9-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85f9-135">post オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c85f9-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c85f9-136">Header files</span></span>

<span data-ttu-id="c85f9-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c85f9-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c85f9-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c85f9-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="c85f9-139">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c85f9-139">Mapitags.h</span></span>
  
> <span data-ttu-id="c85f9-140">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c85f9-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c85f9-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="c85f9-141">See also</span></span>



[<span data-ttu-id="c85f9-142">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85f9-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="c85f9-143">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c85f9-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c85f9-144">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85f9-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c85f9-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c85f9-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c85f9-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c85f9-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

