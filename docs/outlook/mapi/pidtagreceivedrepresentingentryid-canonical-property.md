---
title: PidTagReceivedRepresentingEntryId 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359095"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="7e6a0-103">PidTagReceivedRepresentingEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e6a0-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7e6a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e6a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e6a0-105">受信側ユーザーが表すメッセージングユーザーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e6a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7e6a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e6a0-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7e6a0-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7e6a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7e6a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e6a0-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="7e6a0-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="7e6a0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7e6a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e6a0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7e6a0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7e6a0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7e6a0-112">Area:</span></span>  <br/> |<span data-ttu-id="7e6a0-113">Address</span><span class="sxs-lookup"><span data-stu-id="7e6a0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e6a0-114">解説</span><span class="sxs-lookup"><span data-stu-id="7e6a0-114">Remarks</span></span>

<span data-ttu-id="7e6a0-115">このプロパティは、受信側ユーザーが表すメッセージングユーザーのアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="7e6a0-116">これは、受信トランスポートプロバイダーによって設定される必要があります。これは、代理人の承認または検証も行います。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="7e6a0-117">メッセージングユーザーが表示されていない場合、このプロパティは**PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) プロパティに含まれるエントリ識別子に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7e6a0-118">他のクライアントに代わって受信したメッセージに応答するクライアントアプリケーションは、受信したメッセージから、返信の**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) プロパティにこのプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e6a0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7e6a0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e6a0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7e6a0-120">Protocol specifications</span></span>

<span data-ttu-id="7e6a0-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e6a0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e6a0-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e6a0-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e6a0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e6a0-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7e6a0-125">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e6a0-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e6a0-126">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7e6a0-127">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e6a0-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e6a0-128">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e6a0-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7e6a0-129">Header files</span></span>

<span data-ttu-id="7e6a0-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e6a0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e6a0-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e6a0-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7e6a0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="7e6a0-133">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7e6a0-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e6a0-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e6a0-134">See also</span></span>



[<span data-ttu-id="7e6a0-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7e6a0-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e6a0-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e6a0-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e6a0-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7e6a0-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e6a0-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7e6a0-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

