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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359088"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="e85ee-103">PidTagSentRepresentingEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e85ee-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e85ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e85ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e85ee-105">送信者によって表されるメッセージング ユーザーのエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e85ee-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e85ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e85ee-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e85ee-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e85ee-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e85ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e85ee-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="e85ee-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="e85ee-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e85ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="e85ee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e85ee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e85ee-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e85ee-112">Area:</span></span>  <br/> |<span data-ttu-id="e85ee-113">Address</span><span class="sxs-lookup"><span data-stu-id="e85ee-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e85ee-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e85ee-114">Remarks</span></span>

<span data-ttu-id="e85ee-115">このプロパティは、送信者が表すメッセージング ユーザーのアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="e85ee-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="e85ee-116">クライアント アプリケーションが別のクライアントに代わってメッセージを送信する場合は、表される送信者のすべてのプロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85ee-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="e85ee-117">一般に、独自に送信するメッセージング ユーザーは、表される送信者プロパティを設定解除します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="e85ee-118">送信トランスポート プロバイダーは、送信側クライアントによって設定されている場合は、常にこのプロパティを変更しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85ee-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="e85ee-119">設定されていない場合、トランスポート プロバイダーは、メッセージの送信コピーで **PR_SENDER_ENTRYID** ([PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)に設定し、ローカル コピーで設定を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e85ee-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e85ee-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e85ee-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e85ee-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e85ee-121">Protocol specifications</span></span>

<span data-ttu-id="e85ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-123">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e85ee-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-125">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e85ee-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-127">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e85ee-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-129">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e85ee-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-131">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e85ee-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-133">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e85ee-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85ee-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85ee-135">ポスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e85ee-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e85ee-136">Header files</span></span>

<span data-ttu-id="e85ee-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e85ee-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e85ee-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e85ee-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="e85ee-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e85ee-139">Mapitags.h</span></span>
  
> <span data-ttu-id="e85ee-140">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e85ee-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e85ee-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="e85ee-141">See also</span></span>



[<span data-ttu-id="e85ee-142">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e85ee-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="e85ee-143">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e85ee-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e85ee-144">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e85ee-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e85ee-145">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e85ee-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e85ee-146">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e85ee-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

