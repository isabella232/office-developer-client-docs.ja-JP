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
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359221"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="901f7-103">PidTagReceivedByEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901f7-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="901f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="901f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="901f7-105">実際にメッセージを受信するメッセージングユーザーのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="901f7-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="901f7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="901f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="901f7-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="901f7-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="901f7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="901f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="901f7-109">0x003f</span><span class="sxs-lookup"><span data-stu-id="901f7-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="901f7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="901f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="901f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="901f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="901f7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="901f7-112">Area:</span></span>  <br/> |<span data-ttu-id="901f7-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="901f7-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="901f7-114">解説</span><span class="sxs-lookup"><span data-stu-id="901f7-114">Remarks</span></span>

<span data-ttu-id="901f7-115">このプロパティは、メッセージを受信するメッセージングユーザーのアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="901f7-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="901f7-116">受信トランスポートプロバイダーによって設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="901f7-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="901f7-117">このプロパティは、メッセージごとの MH_T_ 属性の受信配信エンベロープに対応しています。</span><span class="sxs-lookup"><span data-stu-id="901f7-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="901f7-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="901f7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="901f7-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="901f7-119">Protocol specifications</span></span>

<span data-ttu-id="901f7-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="901f7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="901f7-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-123">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="901f7-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="901f7-124">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-125">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="901f7-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="901f7-126">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-127">IETF RFC2445、RFC2446、RFC2447、予定および会議のアイテムを変換します。</span><span class="sxs-lookup"><span data-stu-id="901f7-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="901f7-128">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-129">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="901f7-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="901f7-130">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="901f7-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="901f7-131">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="901f7-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="901f7-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="901f7-132">Header files</span></span>

<span data-ttu-id="901f7-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="901f7-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="901f7-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="901f7-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="901f7-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="901f7-135">Mapitags.h</span></span>
  
> <span data-ttu-id="901f7-136">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="901f7-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="901f7-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="901f7-137">See also</span></span>



[<span data-ttu-id="901f7-138">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901f7-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="901f7-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="901f7-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="901f7-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901f7-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="901f7-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="901f7-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="901f7-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="901f7-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

