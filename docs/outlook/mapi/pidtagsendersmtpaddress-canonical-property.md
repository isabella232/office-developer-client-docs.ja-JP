---
title: PidTagSenderSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387028"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="10900-103">PidTagSenderSmtpAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10900-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="10900-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10900-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10900-105">送信元のメールボックスの所有者の簡易メール転送プロトコル (SMTP) 電子メール アドレスの形式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10900-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10900-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="10900-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10900-107">PR_SENDER_SMTP_ADDRESS、PR_SENDER_SMTP_ADDRESS_A、PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="10900-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="10900-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="10900-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10900-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="10900-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="10900-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="10900-110">Data type:</span></span>  <br/> |<span data-ttu-id="10900-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="10900-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="10900-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="10900-112">Area:</span></span>  <br/> |<span data-ttu-id="10900-113">Address</span><span class="sxs-lookup"><span data-stu-id="10900-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10900-114">備考</span><span class="sxs-lookup"><span data-stu-id="10900-114">Remarks</span></span>

<span data-ttu-id="10900-115">このプロパティは、メッセージの送信者のアドレスのプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="10900-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="10900-116">以前の既存の値を反映する必要があることはありませんが、送信トランスポート プロバイダーによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10900-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="10900-117">トランスポート プロバイダーは、任意の送信者アドレスのプロパティを指定しない場合、MAPI スプーラーはメソッドを呼び出して、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)のエントリ id を入力しようとします。</span><span class="sxs-lookup"><span data-stu-id="10900-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="10900-118">エントリ id が指定されていません、MAPI スプーラーは PT_UNICODE または PT_STRING8 型のすべての送信者アドレスのプロパティに「不明」を格納します。</span><span class="sxs-lookup"><span data-stu-id="10900-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="10900-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="10900-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10900-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="10900-120">Protocol specifications</span></span>

<span data-ttu-id="10900-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-122">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="10900-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10900-123">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="10900-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="10900-125">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-126">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="10900-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="10900-127">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="10900-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="10900-129">[[MS OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-130">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="10900-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="10900-131">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-132">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="10900-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="10900-133">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10900-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10900-134">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="10900-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10900-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="10900-135">Header files</span></span>

<span data-ttu-id="10900-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10900-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="10900-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="10900-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="10900-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10900-138">Mapitags.h</span></span>
  
> <span data-ttu-id="10900-139">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10900-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10900-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="10900-140">See also</span></span>



[<span data-ttu-id="10900-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="10900-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10900-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="10900-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10900-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10900-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10900-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="10900-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

