---
title: PidTagSentRepresentingEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341091"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="8d7e0-103">PidTagSentRepresentingEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d7e0-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8d7e0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d7e0-105">送信者によって表されるメッセージングユーザーの電子メールアドレスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d7e0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d7e0-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS、PR_SENT_REPRESENTING_EMAIL_ADDRESS_A、PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8d7e0-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8d7e0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d7e0-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="8d7e0-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="8d7e0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8d7e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d7e0-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8d7e0-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8d7e0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-112">Area:</span></span>  <br/> |<span data-ttu-id="8d7e0-113">Address</span><span class="sxs-lookup"><span data-stu-id="8d7e0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d7e0-114">解説</span><span class="sxs-lookup"><span data-stu-id="8d7e0-114">Remarks</span></span>

<span data-ttu-id="8d7e0-115">これらのプロパティは、送信者が表すメッセージングユーザーのアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="8d7e0-116">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、表示されているすべての sender プロパティをそのクライアントの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8d7e0-117">通常、メッセージングユーザーが自分の代わりに送信すると、表示される sender プロパティは未設定のままになります。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8d7e0-118">送信側クライアントによって設定されている場合、送信トランスポートプロバイダーは常にこれらのプロパティを変更しないでおく必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8d7e0-119">このプロパティが設定されていない場合、トランスポートプロバイダーは、メッセージの送信コピーで**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) プロパティに設定し、ローカルコピーで設定を解除したままにします。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d7e0-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d7e0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d7e0-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d7e0-121">Protocol specifications</span></span>

<span data-ttu-id="8d7e0-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d7e0-124">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-125">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d7e0-126">[[OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-127">RSS アイテムを表すプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8d7e0-128">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-129">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d7e0-130">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-131">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8d7e0-132">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-133">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8d7e0-134">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-135">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="8d7e0-136">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e0-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e0-137">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d7e0-138">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8d7e0-138">Header files</span></span>

<span data-ttu-id="8d7e0-139">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d7e0-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d7e0-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d7e0-141">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8d7e0-141">Mapitags.h</span></span>
  
> <span data-ttu-id="8d7e0-142">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d7e0-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d7e0-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d7e0-143">See also</span></span>



[<span data-ttu-id="8d7e0-144">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d7e0-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d7e0-145">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d7e0-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d7e0-146">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d7e0-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d7e0-147">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d7e0-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

