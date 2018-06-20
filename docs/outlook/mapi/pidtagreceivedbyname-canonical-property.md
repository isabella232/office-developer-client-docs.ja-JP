---
title: PidTagReceivedByName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7b564b1dda1d72a28e16fad40f0ef90451aaaf0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803254"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="8d472-103">PidTagReceivedByName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d472-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="8d472-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d472-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d472-105">メッセージを受信したメッセージのユーザーの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d472-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d472-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8d472-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d472-107">PR_RECEIVED_BY_NAME、PR_RECEIVED_BY_NAME_A、PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8d472-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8d472-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d472-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d472-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="8d472-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="8d472-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8d472-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d472-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8d472-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8d472-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8d472-112">Area:</span></span>  <br/> |<span data-ttu-id="8d472-113">Address</span><span class="sxs-lookup"><span data-stu-id="8d472-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d472-114">備考</span><span class="sxs-lookup"><span data-stu-id="8d472-114">Remarks</span></span>

<span data-ttu-id="8d472-115">これらのプロパティは、メッセージを受信したメッセージのユーザーのアドレスのプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="8d472-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="8d472-116">着信トランスポート プロバイダーが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8d472-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d472-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d472-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d472-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d472-118">Protocol specifications</span></span>

<span data-ttu-id="8d472-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d472-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d472-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d472-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d472-123">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-124">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="8d472-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d472-125">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-126">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="8d472-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8d472-127">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-128">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="8d472-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8d472-129">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d472-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d472-130">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="8d472-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d472-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d472-131">Header files</span></span>

<span data-ttu-id="8d472-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d472-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d472-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d472-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d472-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d472-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8d472-135">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d472-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d472-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d472-136">See also</span></span>



[<span data-ttu-id="8d472-137">PidTagDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d472-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="8d472-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d472-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d472-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d472-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d472-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8d472-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d472-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8d472-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

