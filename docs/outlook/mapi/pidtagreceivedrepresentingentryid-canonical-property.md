---
title: PidTagReceivedRepresentingEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803260"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="0e56a-103">PidTagReceivedRepresentingEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0e56a-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0e56a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e56a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e56a-105">受信側ユーザーはメッセージング ユーザーのエントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0e56a-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e56a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0e56a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e56a-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0e56a-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0e56a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0e56a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e56a-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="0e56a-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="0e56a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e56a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0e56a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0e56a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0e56a-112">Area:</span></span>  <br/> |<span data-ttu-id="0e56a-113">Address</span><span class="sxs-lookup"><span data-stu-id="0e56a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e56a-114">備考</span><span class="sxs-lookup"><span data-stu-id="0e56a-114">Remarks</span></span>

<span data-ttu-id="0e56a-115">このプロパティは、受信側のユーザーによって表現されているメッセージング ユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0e56a-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="0e56a-116">承認または代理人の確認を担当するも、受信トランスポート プロバイダーによって設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0e56a-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="0e56a-117">表されるは、メッセージング ユーザーがない場合、このプロパティは**PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) のプロパティに含まれているエントリの識別子を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e56a-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0e56a-118">クライアント アプリケーションに返信する他のクライアントの代理として受信したメッセージ、受信したメッセージからの応答を**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) のプロパティにこのプロパティする必要がありますコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e56a-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e56a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0e56a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e56a-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0e56a-120">Protocol specifications</span></span>

<span data-ttu-id="0e56a-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e56a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e56a-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e56a-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e56a-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e56a-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0e56a-125">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e56a-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e56a-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0e56a-127">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e56a-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e56a-128">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e56a-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0e56a-129">Header files</span></span>

<span data-ttu-id="0e56a-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e56a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e56a-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e56a-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e56a-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e56a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0e56a-133">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0e56a-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e56a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e56a-134">See also</span></span>



[<span data-ttu-id="0e56a-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e56a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e56a-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e56a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e56a-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="0e56a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e56a-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="0e56a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

