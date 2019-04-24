---
title: PidTagSentRepresentingSmtpAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341938"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="b94ed-103">PidTagSentRepresentingSmtpAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b94ed-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="b94ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b94ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b94ed-105">送信者によって表されるメッセージングユーザーの SMTP (Simple Mail Transport Protocol) 電子メールアドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b94ed-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b94ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b94ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b94ed-107">PR_SENT_REPRESENTING_SMTP_ADDRESS、PR_SENT_REPRESENTING_SMTP_ADDRESS_A、PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="b94ed-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="b94ed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b94ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b94ed-109">0x5d02</span><span class="sxs-lookup"><span data-stu-id="b94ed-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="b94ed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b94ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="b94ed-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b94ed-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b94ed-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b94ed-112">Area:</span></span>  <br/> |<span data-ttu-id="b94ed-113">Address</span><span class="sxs-lookup"><span data-stu-id="b94ed-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b94ed-114">解説</span><span class="sxs-lookup"><span data-stu-id="b94ed-114">Remarks</span></span>

<span data-ttu-id="b94ed-115">このプロパティは、送信者が表すメッセージングユーザーのアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="b94ed-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="b94ed-116">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、表示されているすべての sender プロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b94ed-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="b94ed-117">通常、メッセージングユーザーが自分の代わりに送信すると、表示される sender プロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="b94ed-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="b94ed-118">送信側クライアントによって設定されている場合、送信トランスポートプロバイダーは常にこのプロパティを変更しないでおく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b94ed-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="b94ed-119">このプロパティが設定されていない場合、トランスポートプロバイダーは、メッセージの送信コピーで**PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) プロパティに設定し、ローカルコピーで設定を解除したままにします。</span><span class="sxs-lookup"><span data-stu-id="b94ed-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b94ed-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b94ed-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b94ed-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b94ed-121">Protocol specifications</span></span>

<span data-ttu-id="b94ed-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b94ed-124">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-125">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b94ed-126">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-127">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b94ed-128">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-129">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b94ed-130">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-131">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b94ed-132">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-133">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="b94ed-134">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-135">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="b94ed-136">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b94ed-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b94ed-137">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="b94ed-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b94ed-138">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b94ed-138">Header files</span></span>

<span data-ttu-id="b94ed-139">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b94ed-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="b94ed-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b94ed-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="b94ed-141">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b94ed-141">Mapitags.h</span></span>
  
> <span data-ttu-id="b94ed-142">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b94ed-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b94ed-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="b94ed-143">See also</span></span>



[<span data-ttu-id="b94ed-144">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b94ed-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b94ed-145">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b94ed-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b94ed-146">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b94ed-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b94ed-147">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b94ed-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

