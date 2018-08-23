---
title: PidTagSenderSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea0e2b753212acc48c56240b3a72b7f22954802a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803506"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="46f35-103">PidTagSenderSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="46f35-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="46f35-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46f35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46f35-105">メッセージ送信者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="46f35-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46f35-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="46f35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46f35-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="46f35-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="46f35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="46f35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46f35-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="46f35-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="46f35-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="46f35-110">Data type:</span></span>  <br/> |<span data-ttu-id="46f35-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="46f35-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="46f35-112">領域:</span><span class="sxs-lookup"><span data-stu-id="46f35-112">Area:</span></span>  <br/> |<span data-ttu-id="46f35-113">Address</span><span class="sxs-lookup"><span data-stu-id="46f35-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46f35-114">注釈</span><span class="sxs-lookup"><span data-stu-id="46f35-114">Remarks</span></span>

<span data-ttu-id="46f35-115">このプロパティは、メッセージの送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="46f35-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="46f35-116">以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46f35-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="46f35-117">トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="46f35-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="46f35-118">エントリ id が指定されていません、MAPI スプーラーは、このプロパティに文字列「不明」に対応するキーを格納します。</span><span class="sxs-lookup"><span data-stu-id="46f35-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46f35-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="46f35-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46f35-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="46f35-120">Protocol specifications</span></span>

<span data-ttu-id="46f35-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="46f35-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46f35-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="46f35-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="46f35-125">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="46f35-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="46f35-127">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="46f35-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="46f35-129">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-130">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="46f35-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="46f35-131">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-132">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="46f35-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="46f35-133">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f35-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f35-134">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="46f35-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46f35-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="46f35-135">Header files</span></span>

<span data-ttu-id="46f35-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46f35-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="46f35-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="46f35-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="46f35-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46f35-138">Mapitags.h</span></span>
  
> <span data-ttu-id="46f35-139">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="46f35-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46f35-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="46f35-140">See also</span></span>



[<span data-ttu-id="46f35-141">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="46f35-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="46f35-142">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="46f35-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="46f35-143">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="46f35-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46f35-144">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="46f35-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46f35-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="46f35-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46f35-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="46f35-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

