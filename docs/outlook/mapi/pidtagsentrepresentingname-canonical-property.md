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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383073"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="86540-103">PidTagSentRepresentingName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86540-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="86540-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86540-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86540-105">送信者によって表されるメッセージング ユーザーの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86540-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86540-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="86540-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86540-107">PR_SENT_REPRESENTING_NAME、PR_SENT_REPRESENTING_NAME_A、PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="86540-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="86540-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="86540-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86540-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="86540-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="86540-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="86540-110">Data type:</span></span>  <br/> |<span data-ttu-id="86540-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="86540-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="86540-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="86540-112">Area:</span></span>  <br/> |<span data-ttu-id="86540-113">Address</span><span class="sxs-lookup"><span data-stu-id="86540-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86540-114">備考</span><span class="sxs-lookup"><span data-stu-id="86540-114">Remarks</span></span>

<span data-ttu-id="86540-115">これらのプロパティでは、送信者によって表されるメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="86540-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="86540-116">クライアント アプリケーションは、別のクライアントの代わりにメッセージを送信するときは、そのクライアントの値に表される送信者のすべてのプロパティを設定にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86540-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="86540-117">通常それ自体の代わりに送信するメッセージのユーザーのまま表される送信者のプロパティ設定を解除します。</span><span class="sxs-lookup"><span data-stu-id="86540-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="86540-118">トランスポート プロバイダーは、送信は、送信元のクライアントで設定されている場合、このプロパティを常に確保する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86540-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="86540-119">設定しない場合は、トランスポート プロバイダーは、必要があります**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) に、メッセージの送信のコピーに設定し、ローカル コピーに設定されていないままです。</span><span class="sxs-lookup"><span data-stu-id="86540-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86540-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="86540-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86540-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="86540-121">Protocol specifications</span></span>

<span data-ttu-id="86540-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="86540-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86540-124">[[MS OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="86540-125">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="86540-126">[[MS OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="86540-127">RSS 項目を表すための操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="86540-128">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-129">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="86540-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="86540-130">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-131">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="86540-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="86540-132">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-133">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="86540-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="86540-134">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-135">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="86540-136">[[MS OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-137">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="86540-138">[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-139">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="86540-140">[[MS OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-141">投稿オブジェクトのプロパティとは、許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="86540-142">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-143">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86540-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="86540-144">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86540-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86540-145">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="86540-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86540-146">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="86540-146">Header files</span></span>

<span data-ttu-id="86540-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86540-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="86540-148">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="86540-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="86540-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86540-149">Mapitags.h</span></span>
  
> <span data-ttu-id="86540-150">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86540-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86540-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="86540-151">See also</span></span>



[<span data-ttu-id="86540-152">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86540-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="86540-153">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86540-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86540-154">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86540-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86540-155">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86540-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86540-156">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86540-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

