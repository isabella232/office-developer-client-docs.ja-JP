---
title: PidTagReceivedByEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEmailAddress
api_type:
- COM
ms.assetid: 5f9ebe20-b037-422b-9991-69f85122a706
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 442a5a69138fdd229289b4201224a4f151c8ccc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581903"
---
# <a name="pidtagreceivedbyemailaddress-canonical-property"></a><span data-ttu-id="ca001-103">PidTagReceivedByEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca001-103">PidTagReceivedByEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="ca001-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca001-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca001-105">メッセージを受信したメッセージのユーザーの電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca001-105">Contains the email address for the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca001-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ca001-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca001-107">PR_RECEIVED_BY_EMAIL_ADDRESS、PR_RECEIVED_BY_EMAIL_ADDRESS_A、PR_RECEIVED_BY_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="ca001-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="ca001-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ca001-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca001-109">0x0076</span><span class="sxs-lookup"><span data-stu-id="ca001-109">0x0076</span></span>  <br/> |
|<span data-ttu-id="ca001-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ca001-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca001-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ca001-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ca001-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ca001-112">Area:</span></span>  <br/> |<span data-ttu-id="ca001-113">Address</span><span class="sxs-lookup"><span data-stu-id="ca001-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca001-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ca001-114">Remarks</span></span>

<span data-ttu-id="ca001-115">これらのプロパティでは、メッセージを受信したメッセージのユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="ca001-115">These properties are examples of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="ca001-116">着信トランスポート プロバイダーが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ca001-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca001-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ca001-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca001-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ca001-118">Protocol specifications</span></span>

<span data-ttu-id="ca001-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca001-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca001-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca001-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ca001-123">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-124">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="ca001-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ca001-125">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-126">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="ca001-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ca001-127">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-128">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="ca001-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="ca001-129">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-130">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca001-130">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ca001-131">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca001-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca001-132">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="ca001-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca001-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ca001-133">Header files</span></span>

<span data-ttu-id="ca001-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca001-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca001-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca001-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca001-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca001-136">Mapitags.h</span></span>
  
> <span data-ttu-id="ca001-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca001-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca001-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca001-138">See also</span></span>



[<span data-ttu-id="ca001-139">PidTagEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca001-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="ca001-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca001-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca001-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca001-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca001-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca001-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca001-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca001-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

