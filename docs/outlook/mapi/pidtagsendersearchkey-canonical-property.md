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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342855"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="5e491-103">PidTagSenderSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e491-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5e491-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e491-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e491-105">メッセージ送信者の検索キーが含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e491-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e491-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5e491-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e491-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5e491-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5e491-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5e491-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e491-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="5e491-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="5e491-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5e491-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e491-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e491-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e491-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5e491-112">Area:</span></span>  <br/> |<span data-ttu-id="5e491-113">Address</span><span class="sxs-lookup"><span data-stu-id="5e491-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e491-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5e491-114">Remarks</span></span>

<span data-ttu-id="5e491-115">このプロパティは、メッセージ送信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="5e491-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="5e491-116">これは、送信トランスポート プロバイダーによって設定する必要があります。これは、以前に既存の値を伝達する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e491-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="5e491-117">送信側アドレスプロパティを提供しているトランスポート プロバイダーがない場合、MAPI スプーラーは、エントリ識別子の [IMAPISession::QueryIdentity](imapisession-queryidentity.md) メソッドを呼び出して、それらを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e491-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="5e491-118">エントリ識別子が指定されていない場合、MAPI スプーラーは、このプロパティの文字列 "Unknown" に対応するキーを格納します。</span><span class="sxs-lookup"><span data-stu-id="5e491-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e491-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5e491-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e491-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5e491-120">Protocol specifications</span></span>

<span data-ttu-id="5e491-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5e491-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e491-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e491-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5e491-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-126">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="5e491-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5e491-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-128">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="5e491-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5e491-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-130">ポスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e491-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="5e491-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-132">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e491-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="5e491-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e491-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e491-134">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="5e491-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e491-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5e491-135">Header files</span></span>

<span data-ttu-id="5e491-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e491-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e491-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e491-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e491-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e491-138">Mapitags.h</span></span>
  
> <span data-ttu-id="5e491-139">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e491-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e491-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e491-140">See also</span></span>



[<span data-ttu-id="5e491-141">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e491-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="5e491-142">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e491-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="5e491-143">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5e491-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e491-144">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e491-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e491-145">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e491-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e491-146">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e491-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

