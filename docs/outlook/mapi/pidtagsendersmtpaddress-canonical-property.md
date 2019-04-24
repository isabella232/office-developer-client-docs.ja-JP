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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342631"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a><span data-ttu-id="c0e0d-103">PidTagSenderSmtpAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0e0d-103">PidTagSenderSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="c0e0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e0d-105">送信メールボックス所有者の簡易メールトランスポートプロトコル (SMTP) 電子メールアドレスの形式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-105">Contains the format of the Simple Mail Transport Protocol (SMTP) email address of the sending mailbox owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0e0d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c0e0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0e0d-107">PR_SENDER_SMTP_ADDRESS、PR_SENDER_SMTP_ADDRESS_A、PR_SENDER_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="c0e0d-107">PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="c0e0d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c0e0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0e0d-109">0x5d01</span><span class="sxs-lookup"><span data-stu-id="c0e0d-109">0x5D01</span></span>  <br/> |
|<span data-ttu-id="c0e0d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c0e0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0e0d-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c0e0d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c0e0d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c0e0d-112">Area:</span></span>  <br/> |<span data-ttu-id="c0e0d-113">Address</span><span class="sxs-lookup"><span data-stu-id="c0e0d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0e0d-114">解説</span><span class="sxs-lookup"><span data-stu-id="c0e0d-114">Remarks</span></span>

<span data-ttu-id="c0e0d-115">このプロパティは、メッセージ送信者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-115">This property is an example of the address properties for the message sender.</span></span> <span data-ttu-id="c0e0d-116">送信トランスポートプロバイダーによって設定されている必要があります。これは、以前の既存の値を伝達しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="c0e0d-117">トランスポートプロバイダーが送信者アドレスのプロパティを指定していない場合、MAPI スプーラーは、エントリ id に対して[imapisession:: queryidentity](imapisession-queryidentity.md)メソッドを呼び出して、これらのプロパティの読み込みを試みます。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="c0e0d-118">エントリ識別子が指定されていない場合、MAPI スプーラーは、PT_UNICODE または PT_STRING8 型のすべての送信者アドレスプロパティに "Unknown" を格納します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_UNICODE or PT_STRING8.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0e0d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c0e0d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0e0d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c0e0d-120">Protocol specifications</span></span>

<span data-ttu-id="c0e0d-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-122">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-122">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0e0d-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c0e0d-125">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-126">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c0e0d-127">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-128">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c0e0d-129">[[OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-130">post オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="c0e0d-131">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-132">連絡先および個人用配布リストオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="c0e0d-133">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0e0d-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0e0d-134">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0e0d-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c0e0d-135">Header files</span></span>

<span data-ttu-id="c0e0d-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0e0d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0e0d-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0e0d-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c0e0d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c0e0d-139">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c0e0d-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0e0d-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0e0d-140">See also</span></span>



[<span data-ttu-id="c0e0d-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c0e0d-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0e0d-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0e0d-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0e0d-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c0e0d-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0e0d-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c0e0d-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

