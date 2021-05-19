---
title: PidTagSenderSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342631"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="9a850-103">PidTagSenderSmtpAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a850-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="9a850-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a850-105">送信メールボックス所有者の簡易メール トランスポート プロトコル (SMTP) 電子メール アドレスの形式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a850-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a850-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9a850-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a850-107">PR_SENDER_SMTP_ADDRESS、PR_SENDER_SMTP_ADDRESS_A、PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="9a850-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="9a850-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9a850-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a850-109">0x5D01</span><span class="sxs-lookup"><span data-stu-id="9a850-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="9a850-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9a850-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a850-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9a850-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9a850-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9a850-112">Area:</span></span>  <br/> |<span data-ttu-id="9a850-113">Address</span><span class="sxs-lookup"><span data-stu-id="9a850-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a850-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9a850-114">Remarks</span></span>

<span data-ttu-id="9a850-115">このプロパティは、メッセージ送信者のアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="9a850-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="9a850-116">これは、送信トランスポート プロバイダーによって設定する必要があります。これは、以前に既存の値を伝達する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a850-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="9a850-117">送信側アドレスプロパティを提供しているトランスポート プロバイダーがない場合、MAPI スプーラーは、エントリ識別子の [IMAPISession::QueryIdentity](imapisession-queryidentity.md) メソッドを呼び出して、それらを入力します。</span><span class="sxs-lookup"><span data-stu-id="9a850-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="9a850-118">エントリ識別子が指定されていない場合は、MAPI スプーラーは、種類が PT_UNICODE または PT_STRING8 のすべての送信者アドレス プロパティに "不明" を格納します。</span><span class="sxs-lookup"><span data-stu-id="9a850-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9a850-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9a850-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a850-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9a850-120">Protocol specifications</span></span>

<span data-ttu-id="9a850-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-122">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9a850-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9a850-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a850-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="9a850-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-126">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="9a850-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9a850-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-128">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="9a850-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9a850-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-130">ポスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a850-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="9a850-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-132">連絡先および個人用配布リスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a850-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="9a850-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a850-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a850-134">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="9a850-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a850-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9a850-135">Header files</span></span>

<span data-ttu-id="9a850-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a850-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a850-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a850-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a850-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9a850-138">Mapitags.h</span></span>
  
> <span data-ttu-id="9a850-139">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9a850-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a850-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a850-140">See also</span></span>



[<span data-ttu-id="9a850-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9a850-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a850-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a850-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a850-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9a850-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a850-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9a850-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

