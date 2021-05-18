---
title: PidTagReceivedRepresentingAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9592057757b7bad0c2400f8b1c720ef0146bb9a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359200"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a><span data-ttu-id="bbe22-103">PidTagReceivedRepresentingAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbe22-103">PidTagReceivedRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="bbe22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbe22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbe22-105">メッセージを実際に受信したユーザーによって表されるメッセージング ユーザーのアドレスの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-105">Contains the address type for the messaging user who is represented by the user actually receiving the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbe22-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bbe22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbe22-107">PR_RCVD_REPRESENTING_ADDRTYPE、PR_RCVD_REPRESENTING_ADDRTYPE_A、PR_RCVD_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="bbe22-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="bbe22-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bbe22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbe22-109">0x0077</span><span class="sxs-lookup"><span data-stu-id="bbe22-109">0x0077</span></span>  <br/> |
|<span data-ttu-id="bbe22-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bbe22-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbe22-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bbe22-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bbe22-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bbe22-112">Area:</span></span>  <br/> |<span data-ttu-id="bbe22-113">Address</span><span class="sxs-lookup"><span data-stu-id="bbe22-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbe22-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bbe22-114">Remarks</span></span>

<span data-ttu-id="bbe22-115">これらのプロパティは、受信ユーザーによって表されるメッセージング ユーザーのアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="bbe22-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="bbe22-116">これは、代理人の承認または検証を担当する受信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe22-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="bbe22-117">メッセージング ユーザーが表されていない場合、このプロパティは **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) プロパティに含まれるアドレスの種類に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe22-117">If no messaging user is being represented, this property should be set to the address type contained in the **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bbe22-118">別のクライアントに代わって受信したメッセージに返信するクライアント アプリケーションは、このプロパティを受信したメッセージから返信の **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType)](pidtagsentrepresentingaddresstype-canonical-property.md)プロパティにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe22-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbe22-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bbe22-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbe22-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bbe22-120">Protocol specifications</span></span>

<span data-ttu-id="bbe22-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbe22-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bbe22-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-126">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="bbe22-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-128">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="bbe22-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-130">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="bbe22-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbe22-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbe22-132">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="bbe22-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbe22-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bbe22-133">Header files</span></span>

<span data-ttu-id="bbe22-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbe22-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbe22-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbe22-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbe22-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbe22-136">Mapitags.h</span></span>
  
> <span data-ttu-id="bbe22-137">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bbe22-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbe22-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbe22-138">See also</span></span>



[<span data-ttu-id="bbe22-139">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbe22-139">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="bbe22-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bbe22-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbe22-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbe22-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbe22-142">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bbe22-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbe22-143">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bbe22-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

