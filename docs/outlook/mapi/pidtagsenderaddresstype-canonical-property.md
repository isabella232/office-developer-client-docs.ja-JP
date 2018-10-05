---
title: PidTagSenderAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1389c1189293955145f14e65f4c0f3e58bec909f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388666"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a><span data-ttu-id="7618c-103">PidTagSenderAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7618c-103">PidTagSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="7618c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7618c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7618c-105">メッセージ送信者の電子メール アドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7618c-105">Contains the message sender's email address type.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7618c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7618c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7618c-107">PR_SENDER_ADDRTYPE、PR_SENDER_ADDRTYPE_A、PR_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="7618c-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="7618c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7618c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7618c-109">0x0C1E</span><span class="sxs-lookup"><span data-stu-id="7618c-109">0x0C1E</span></span>  <br/> |
|<span data-ttu-id="7618c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7618c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7618c-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7618c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7618c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7618c-112">Area:</span></span>  <br/> |<span data-ttu-id="7618c-113">Address</span><span class="sxs-lookup"><span data-stu-id="7618c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7618c-114">備考</span><span class="sxs-lookup"><span data-stu-id="7618c-114">Remarks</span></span>

<span data-ttu-id="7618c-115">これらのプロパティでは、メッセージの送信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="7618c-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="7618c-116">以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7618c-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="7618c-117">トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="7618c-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="7618c-118">エントリ id が指定されていません、MAPI スプーラーは PT_TSTRING の種類のすべての送信者アドレスのプロパティで「不明」を格納します。</span><span class="sxs-lookup"><span data-stu-id="7618c-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7618c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7618c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7618c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7618c-120">Protocol specifications</span></span>

<span data-ttu-id="7618c-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7618c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7618c-123">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7618c-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7618c-125">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="7618c-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7618c-127">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="7618c-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7618c-129">[[MS OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-130">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7618c-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="7618c-131">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-132">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7618c-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="7618c-133">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7618c-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7618c-134">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="7618c-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7618c-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7618c-135">Header files</span></span>

<span data-ttu-id="7618c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7618c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7618c-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7618c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7618c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7618c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7618c-139">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7618c-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7618c-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="7618c-140">See also</span></span>



[<span data-ttu-id="7618c-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7618c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7618c-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7618c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7618c-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7618c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7618c-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7618c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

