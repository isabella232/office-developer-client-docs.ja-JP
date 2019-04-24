---
title: PidTagDisplayTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360789"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="25d4c-103">PidTagDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25d4c-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="25d4c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25d4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25d4c-105">セミコロン (;) で区切られた、プライマリ (宛先) メッセージ受信者の表示名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="25d4c-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25d4c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="25d4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25d4c-107">PR_DISPLAY_TO、PR_DISPLAY_TO_A、PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="25d4c-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="25d4c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="25d4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25d4c-109">0x0e04</span><span class="sxs-lookup"><span data-stu-id="25d4c-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="25d4c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="25d4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="25d4c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25d4c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25d4c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="25d4c-112">Area:</span></span>  <br/> |<span data-ttu-id="25d4c-113">メッセージ</span><span class="sxs-lookup"><span data-stu-id="25d4c-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25d4c-114">解説</span><span class="sxs-lookup"><span data-stu-id="25d4c-114">Remarks</span></span>

<span data-ttu-id="25d4c-115">メッセージストアは、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを使用して、これらのプロパティをメッセージオブジェクトで計算します。</span><span class="sxs-lookup"><span data-stu-id="25d4c-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="25d4c-116">また、メッセージストアは、メッセージの最後に保存された状態を常に反映するようにこれらのプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="25d4c-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="25d4c-117">値は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すたびに同期されます。</span><span class="sxs-lookup"><span data-stu-id="25d4c-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="25d4c-118">メッセージにプライマリ受信者が含まれていない場合、メッセージストアは、戻り値が S_OK で、 **PR_DISPLAY_TO**の空の文字列である[imapiprop:: GetProps](imapiprop-getprops.md)呼び出しに応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d4c-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="25d4c-119">ローカライズが必要になる可能性があるため、MAPI では、すべての受信者名について次のガイドラインが提供されています。</span><span class="sxs-lookup"><span data-stu-id="25d4c-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="25d4c-120">すべての名前をローカライズできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d4c-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="25d4c-121">セミコロンは、 **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、 **PR_DISPLAY_TO**の各プロパティで名前を区切るために使用される文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d4c-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="25d4c-122">MAPI では、受信者名の中にセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="25d4c-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="25d4c-123">クライアントは、ユーザーインターフェイスに情報が表示されるようにするために、 **PR_DISPLAY_TO**および関連するプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d4c-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="25d4c-124">メッセージを転送する場合、クライアントは、プライマリ受信者行の区切り文字を変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="25d4c-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="25d4c-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="25d4c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25d4c-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="25d4c-126">Protocol specifications</span></span>

<span data-ttu-id="25d4c-127">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25d4c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25d4c-128">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="25d4c-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25d4c-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="25d4c-129">Header files</span></span>

<span data-ttu-id="25d4c-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25d4c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="25d4c-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="25d4c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="25d4c-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="25d4c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="25d4c-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="25d4c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25d4c-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="25d4c-134">See also</span></span>



[<span data-ttu-id="25d4c-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="25d4c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25d4c-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25d4c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25d4c-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="25d4c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25d4c-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="25d4c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

