---
title: PidTagDisplayCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360810"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="1d8a2-103">PidTagDisplayCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8a2-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="1d8a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d8a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d8a2-105">任意のカーボンコピー (CC) メッセージ受信者の表示名の ASCII リストをセミコロン (;) で区切って格納します。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d8a2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1d8a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d8a2-107">PR_DISPLAY_CC、PR_DISPLAY_CC_A、PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="1d8a2-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="1d8a2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1d8a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d8a2-109">0x0e03</span><span class="sxs-lookup"><span data-stu-id="1d8a2-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="1d8a2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1d8a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d8a2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d8a2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1d8a2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1d8a2-112">Area:</span></span>  <br/> |<span data-ttu-id="1d8a2-113">メッセージ</span><span class="sxs-lookup"><span data-stu-id="1d8a2-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d8a2-114">解説</span><span class="sxs-lookup"><span data-stu-id="1d8a2-114">Remarks</span></span>

<span data-ttu-id="1d8a2-115">メッセージストアは、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを使用して、これらのプロパティをメッセージオブジェクトで計算します。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="1d8a2-116">また、メッセージストアは、メッセージの最後に保存された状態を常に反映するようにこれらのプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="1d8a2-117">値は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)のすべての呼び出し時に同期されます。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="1d8a2-118">メッセージにカーボンコピー受信者が存在しない場合、メッセージストアは、戻り値が S_OK で、これらのプロパティに空の文字列がある[imapiprop:: GetProps](imapiprop-getprops.md)呼び出しに応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="1d8a2-119">ローカライズが必要になる可能性があるため、MAPI では、すべての受信者名について次のガイドラインが提供されています。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="1d8a2-120">すべての名前をローカライズできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="1d8a2-121">セミコロンは、 **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC**、 **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の各プロパティで名前を区切るために使用される文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="1d8a2-122">MAPI では、受信者名の中にセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="1d8a2-123">クライアントは、ユーザーインターフェイスにプロパティ情報が表示されるようにするために、このプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="1d8a2-124">メッセージを転送する場合、クライアントはカーボンコピーの受信者の行の区切り文字を変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="1d8a2-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1d8a2-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d8a2-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1d8a2-126">Protocol specifications</span></span>

<span data-ttu-id="1d8a2-127">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d8a2-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d8a2-128">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d8a2-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1d8a2-129">Header files</span></span>

<span data-ttu-id="1d8a2-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d8a2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d8a2-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d8a2-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1d8a2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="1d8a2-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d8a2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d8a2-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d8a2-134">See also</span></span>



[<span data-ttu-id="1d8a2-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8a2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d8a2-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d8a2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d8a2-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d8a2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d8a2-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d8a2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

