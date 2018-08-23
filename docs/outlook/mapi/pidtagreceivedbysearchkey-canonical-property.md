---
title: PidTagReceivedBySearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 94d33910650de4f0d625d7a819c66ad8c599a47e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581455"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="535d5-103">PidTagReceivedBySearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="535d5-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="535d5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="535d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="535d5-105">メッセージを受信したメッセージのユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="535d5-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="535d5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="535d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="535d5-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="535d5-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="535d5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="535d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="535d5-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="535d5-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="535d5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="535d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="535d5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="535d5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="535d5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="535d5-112">Area:</span></span>  <br/> |<span data-ttu-id="535d5-113">Address</span><span class="sxs-lookup"><span data-stu-id="535d5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="535d5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="535d5-114">Remarks</span></span>

<span data-ttu-id="535d5-115">このプロパティは、メッセージを受信したメッセージのユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="535d5-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="535d5-116">受信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="535d5-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="535d5-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="535d5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="535d5-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="535d5-118">Protocol specifications</span></span>

<span data-ttu-id="535d5-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="535d5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="535d5-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="535d5-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="535d5-123">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-124">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="535d5-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="535d5-125">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-126">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="535d5-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="535d5-127">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-128">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="535d5-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="535d5-129">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="535d5-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="535d5-130">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="535d5-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="535d5-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="535d5-131">Header files</span></span>

<span data-ttu-id="535d5-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="535d5-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="535d5-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="535d5-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="535d5-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="535d5-134">Mapitags.h</span></span>
  
> <span data-ttu-id="535d5-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="535d5-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="535d5-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="535d5-136">See also</span></span>



[<span data-ttu-id="535d5-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="535d5-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="535d5-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="535d5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="535d5-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="535d5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="535d5-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="535d5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

