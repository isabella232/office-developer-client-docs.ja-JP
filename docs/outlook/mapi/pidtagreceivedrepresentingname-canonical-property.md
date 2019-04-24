---
title: PidTagReceivedRepresentingName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356736"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="f1fd4-103">PidTagReceivedRepresentingName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1fd4-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="f1fd4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1fd4-105">受信側ユーザーが表すメッセージングユーザーの表示名を含みます。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1fd4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f1fd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1fd4-107">PR_RCVD_REPRESENTING_NAME、PR_RCVD_REPRESENTING_NAME_A、PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f1fd4-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f1fd4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f1fd4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1fd4-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="f1fd4-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="f1fd4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f1fd4-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1fd4-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f1fd4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f1fd4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f1fd4-112">Area:</span></span>  <br/> |<span data-ttu-id="f1fd4-113">Address</span><span class="sxs-lookup"><span data-stu-id="f1fd4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1fd4-114">解説</span><span class="sxs-lookup"><span data-stu-id="f1fd4-114">Remarks</span></span>

<span data-ttu-id="f1fd4-115">これらのプロパティは、受信側ユーザーによって表されるメッセージングユーザーのアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="f1fd4-116">これらは、受信トランスポートプロバイダーによって設定される必要があります。これは、代理人の承認または検証も担当します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="f1fd4-117">メッセージングユーザーが表示されていない場合は、これらのプロパティを**PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) プロパティに含まれる表示名に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f1fd4-118">他のクライアントに代わって受信したメッセージに応答するクライアントアプリケーションは、受信したメッセージから返信の**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) プロパティにこれらのプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1fd4-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f1fd4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1fd4-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f1fd4-120">Protocol specifications</span></span>

<span data-ttu-id="f1fd4-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1fd4-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f1fd4-125">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-126">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f1fd4-127">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-128">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f1fd4-129">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-130">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f1fd4-131">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fd4-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fd4-132">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1fd4-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f1fd4-133">Header files</span></span>

<span data-ttu-id="f1fd4-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1fd4-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1fd4-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1fd4-136">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f1fd4-136">Mapitags.h</span></span>
  
> <span data-ttu-id="f1fd4-137">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f1fd4-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1fd4-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1fd4-138">See also</span></span>



[<span data-ttu-id="f1fd4-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f1fd4-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1fd4-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1fd4-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1fd4-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f1fd4-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1fd4-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f1fd4-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

