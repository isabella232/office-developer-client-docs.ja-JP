---
title: PidTagReceivedByEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab3ffed8dd5b8d73d8024d27790f18397d615c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567469"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="b69ff-103">PidTagReceivedByEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b69ff-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b69ff-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b69ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b69ff-105">実際にメッセージを受け取るユーザーはメッセージのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b69ff-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b69ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b69ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b69ff-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b69ff-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b69ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b69ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b69ff-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="b69ff-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="b69ff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b69ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="b69ff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b69ff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b69ff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b69ff-112">Area:</span></span>  <br/> |<span data-ttu-id="b69ff-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="b69ff-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b69ff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b69ff-114">Remarks</span></span>

<span data-ttu-id="b69ff-115">このプロパティは、メッセージを受信したメッセージのユーザーのアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b69ff-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="b69ff-116">受信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b69ff-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="b69ff-117">このプロパティは、X.400 配信エンベロープ メッセージごとの MH_T_ 属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b69ff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b69ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b69ff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b69ff-119">Protocol specifications</span></span>

<span data-ttu-id="b69ff-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b69ff-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b69ff-124">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-125">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b69ff-126">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムに変換します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="b69ff-128">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-129">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b69ff-130">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b69ff-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b69ff-131">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="b69ff-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b69ff-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b69ff-132">Header files</span></span>

<span data-ttu-id="b69ff-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b69ff-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b69ff-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b69ff-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="b69ff-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b69ff-135">Mapitags.h</span></span>
  
> <span data-ttu-id="b69ff-136">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b69ff-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b69ff-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="b69ff-137">See also</span></span>



[<span data-ttu-id="b69ff-138">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b69ff-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="b69ff-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b69ff-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b69ff-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b69ff-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b69ff-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b69ff-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b69ff-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b69ff-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

