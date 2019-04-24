---
title: PidTagSentRepresentingName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314932"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="4ede1-103">PidTagSentRepresentingName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ede1-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="4ede1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ede1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ede1-105">送信者が表すメッセージユーザーの表示名を含みます。</span><span class="sxs-lookup"><span data-stu-id="4ede1-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ede1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4ede1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ede1-107">PR_SENT_REPRESENTING_NAME、PR_SENT_REPRESENTING_NAME_A、PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4ede1-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4ede1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4ede1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ede1-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="4ede1-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="4ede1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4ede1-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ede1-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4ede1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4ede1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4ede1-112">Area:</span></span>  <br/> |<span data-ttu-id="4ede1-113">Address</span><span class="sxs-lookup"><span data-stu-id="4ede1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ede1-114">解説</span><span class="sxs-lookup"><span data-stu-id="4ede1-114">Remarks</span></span>

<span data-ttu-id="4ede1-115">これらのプロパティは、送信者が表すメッセージングユーザーのアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="4ede1-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="4ede1-116">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、表示されているすべての sender プロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ede1-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="4ede1-117">通常、メッセージングユーザーが自分の代わりに送信すると、表示される sender プロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="4ede1-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="4ede1-118">送信側クライアントによって設定されている場合、送信トランスポートプロバイダーは常にこのプロパティを変更しないでおく必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ede1-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="4ede1-119">設定されていない場合、トランスポートプロバイダーは、メッセージの送信コピーで**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) に設定し、ローカルコピー上の設定を解除したままにします。</span><span class="sxs-lookup"><span data-stu-id="4ede1-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ede1-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4ede1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ede1-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4ede1-121">Protocol specifications</span></span>

<span data-ttu-id="4ede1-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ede1-124">[[OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-125">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4ede1-126">[[OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-127">RSS アイテムを表すプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="4ede1-128">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-129">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="4ede1-130">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-131">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4ede1-132">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-133">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="4ede1-134">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-135">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="4ede1-136">[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-137">カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="4ede1-138">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-139">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="4ede1-140">[[OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-141">post オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="4ede1-142">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-143">連絡先および個人用配布リストオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="4ede1-144">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ede1-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ede1-145">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="4ede1-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ede1-146">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4ede1-146">Header files</span></span>

<span data-ttu-id="4ede1-147">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ede1-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ede1-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ede1-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ede1-149">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4ede1-149">Mapitags.h</span></span>
  
> <span data-ttu-id="4ede1-150">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ede1-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ede1-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ede1-151">See also</span></span>



[<span data-ttu-id="4ede1-152">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ede1-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="4ede1-153">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4ede1-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ede1-154">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ede1-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ede1-155">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4ede1-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ede1-156">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4ede1-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

