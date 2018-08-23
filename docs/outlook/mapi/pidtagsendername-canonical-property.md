---
title: PidTagSenderName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6dd3f07ae4c854d3ee87206adf4a3090fe050971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803508"
---
# <a name="pidtagsendername-canonical-property"></a><span data-ttu-id="03ae6-103">PidTagSenderName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ae6-103">PidTagSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="03ae6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03ae6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03ae6-105">メッセージの送信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03ae6-105">Contains the message sender's display name.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03ae6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="03ae6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03ae6-107">PR_SENDER_NAME、PR_SENDER_NAME_A、PR_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="03ae6-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="03ae6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="03ae6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03ae6-109">0x0C1A</span><span class="sxs-lookup"><span data-stu-id="03ae6-109">0x0C1A</span></span>  <br/> |
|<span data-ttu-id="03ae6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="03ae6-110">Data type:</span></span>  <br/> |<span data-ttu-id="03ae6-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="03ae6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="03ae6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="03ae6-112">Area:</span></span>  <br/> |<span data-ttu-id="03ae6-113">Address</span><span class="sxs-lookup"><span data-stu-id="03ae6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03ae6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="03ae6-114">Remarks</span></span>

<span data-ttu-id="03ae6-115">これらのプロパティでは、メッセージの送信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="03ae6-116">以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03ae6-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="03ae6-117">トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="03ae6-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="03ae6-118">エントリ id が指定されていません、MAPI スプーラーは PT_TSTRING の種類のすべての送信者アドレスのプロパティで「不明」を格納します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03ae6-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="03ae6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03ae6-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="03ae6-120">Protocol specifications</span></span>

<span data-ttu-id="03ae6-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03ae6-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-124">クライアント上のフォルダーを共有に関連する情報の送信に使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-124">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
<span data-ttu-id="03ae6-125">[[MS OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-126">RSS 項目を表すための操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="03ae6-127">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-128">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="03ae6-129">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-130">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="03ae6-131">[[MS OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-131">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-132">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-132">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="03ae6-133">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-133">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-134">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-134">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="03ae6-135">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ae6-135">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ae6-136">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="03ae6-136">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03ae6-137">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="03ae6-137">Header files</span></span>

<span data-ttu-id="03ae6-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03ae6-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="03ae6-139">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="03ae6-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="03ae6-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03ae6-140">Mapitags.h</span></span>
  
> <span data-ttu-id="03ae6-141">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03ae6-141">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03ae6-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="03ae6-142">See also</span></span>



[<span data-ttu-id="03ae6-143">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ae6-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03ae6-144">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03ae6-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03ae6-145">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03ae6-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03ae6-146">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="03ae6-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

