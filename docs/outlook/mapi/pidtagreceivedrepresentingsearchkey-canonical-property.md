---
title: PidTagReceivedRepresentingSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 834e97d8bd7bf31a1241fcf0454594b015902673
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803270"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="80a18-103">PidTagReceivedRepresentingSearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="80a18-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="80a18-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80a18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80a18-105">受信側のユーザーによって表されるメッセージのユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="80a18-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80a18-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="80a18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80a18-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="80a18-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="80a18-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="80a18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80a18-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="80a18-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="80a18-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="80a18-110">Data type:</span></span>  <br/> |<span data-ttu-id="80a18-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="80a18-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="80a18-112">領域:</span><span class="sxs-lookup"><span data-stu-id="80a18-112">Area:</span></span>  <br/> |<span data-ttu-id="80a18-113">Address</span><span class="sxs-lookup"><span data-stu-id="80a18-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80a18-114">備考</span><span class="sxs-lookup"><span data-stu-id="80a18-114">Remarks</span></span>

<span data-ttu-id="80a18-115">このプロパティは、受信側のユーザーによって表されるメッセージング ユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="80a18-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="80a18-116">承認または代理人の確認を担当するも、受信トランスポート プロバイダーによって設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="80a18-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="80a18-117">表されるは、メッセージング ユーザーがない場合、このプロパティは**PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) のプロパティに含まれている検索キーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80a18-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="80a18-118">クライアント アプリケーションに返信する他のクライアントの代理として受信したメッセージ、受信したメッセージからの応答を**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) のプロパティにこのプロパティする必要がありますコピーします。</span><span class="sxs-lookup"><span data-stu-id="80a18-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80a18-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="80a18-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80a18-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="80a18-120">Protocol specifications</span></span>

<span data-ttu-id="80a18-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="80a18-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80a18-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="80a18-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="80a18-125">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="80a18-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="80a18-127">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="80a18-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="80a18-129">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-130">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="80a18-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="80a18-131">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80a18-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80a18-132">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="80a18-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80a18-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="80a18-133">Header files</span></span>

<span data-ttu-id="80a18-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80a18-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="80a18-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="80a18-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="80a18-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80a18-136">Mapitags.h</span></span>
  
> <span data-ttu-id="80a18-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="80a18-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80a18-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="80a18-138">See also</span></span>



[<span data-ttu-id="80a18-139">PidTagSearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="80a18-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="80a18-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="80a18-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80a18-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="80a18-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80a18-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="80a18-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80a18-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="80a18-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

