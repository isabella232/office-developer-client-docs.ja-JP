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
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342855"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="72f7b-103">PidTagSenderSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72f7b-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="72f7b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72f7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72f7b-105">メッセージ送信者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72f7b-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72f7b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="72f7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72f7b-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="72f7b-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="72f7b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="72f7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72f7b-109">0x0c1d</span><span class="sxs-lookup"><span data-stu-id="72f7b-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="72f7b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="72f7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="72f7b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="72f7b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="72f7b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="72f7b-112">Area:</span></span>  <br/> |<span data-ttu-id="72f7b-113">Address</span><span class="sxs-lookup"><span data-stu-id="72f7b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f7b-114">解説</span><span class="sxs-lookup"><span data-stu-id="72f7b-114">Remarks</span></span>

<span data-ttu-id="72f7b-115">このプロパティは、メッセージ送信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="72f7b-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="72f7b-116">送信トランスポートプロバイダーによって設定されている必要があります。これは、以前の既存の値を伝達しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72f7b-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="72f7b-117">トランスポートプロバイダーが送信者アドレスのプロパティを指定していない場合、MAPI スプーラーは、エントリ id に対して[imapisession:: queryidentity](imapisession-queryidentity.md)メソッドを呼び出して、これらのプロパティの読み込みを試みます。</span><span class="sxs-lookup"><span data-stu-id="72f7b-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="72f7b-118">エントリ識別子が指定されていない場合、MAPI スプーラーは、このプロパティに "Unknown" という文字列に対応するキーを格納します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72f7b-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="72f7b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72f7b-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="72f7b-120">Protocol specifications</span></span>

<span data-ttu-id="72f7b-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72f7b-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="72f7b-125">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-126">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="72f7b-127">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-128">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="72f7b-129">[[OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-130">post オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="72f7b-131">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-132">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="72f7b-133">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7b-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7b-134">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="72f7b-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72f7b-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="72f7b-135">Header files</span></span>

<span data-ttu-id="72f7b-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72f7b-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="72f7b-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="72f7b-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="72f7b-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="72f7b-138">Mapitags.h</span></span>
  
> <span data-ttu-id="72f7b-139">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72f7b-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72f7b-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="72f7b-140">See also</span></span>



[<span data-ttu-id="72f7b-141">PidTagSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72f7b-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="72f7b-142">PidTagSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72f7b-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="72f7b-143">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="72f7b-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72f7b-144">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72f7b-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72f7b-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="72f7b-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72f7b-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="72f7b-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

