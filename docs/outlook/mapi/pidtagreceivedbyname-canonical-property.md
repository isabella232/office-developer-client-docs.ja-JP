---
title: PidTagReceivedByName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 039a51c2bb4cf1fe2a83e2ba144a87462b5d6d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359214"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="d84b4-103">PidTagReceivedByName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84b4-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="d84b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d84b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d84b4-105">メッセージを受信するメッセージング ユーザーの表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d84b4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d84b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d84b4-107">PR_RECEIVED_BY_NAME、PR_RECEIVED_BY_NAME_A、PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d84b4-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d84b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d84b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d84b4-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="d84b4-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="d84b4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d84b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="d84b4-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d84b4-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d84b4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d84b4-112">Area:</span></span>  <br/> |<span data-ttu-id="d84b4-113">Address</span><span class="sxs-lookup"><span data-stu-id="d84b4-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d84b4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d84b4-114">Remarks</span></span>

<span data-ttu-id="d84b4-115">これらのプロパティは、メッセージを受信するメッセージング ユーザーのアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="d84b4-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="d84b4-116">これらは、受信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84b4-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d84b4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d84b4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d84b4-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d84b4-118">Protocol specifications</span></span>

<span data-ttu-id="d84b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d84b4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-122">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d84b4-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-124">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d84b4-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-126">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d84b4-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-128">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="d84b4-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d84b4-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d84b4-130">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="d84b4-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d84b4-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d84b4-131">Header files</span></span>

<span data-ttu-id="d84b4-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d84b4-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d84b4-133">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d84b4-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="d84b4-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d84b4-134">Mapitags.h</span></span>
  
> <span data-ttu-id="d84b4-135">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d84b4-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d84b4-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="d84b4-136">See also</span></span>



[<span data-ttu-id="d84b4-137">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84b4-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="d84b4-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d84b4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d84b4-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d84b4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d84b4-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d84b4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d84b4-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d84b4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

