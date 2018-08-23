---
title: PidTagDisplayBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cd37d72d6a214f91e371b7126c90e3fda25cde2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578900"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="b1c24-103">PidTagDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1c24-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="b1c24-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1c24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1c24-105">ASCII のリスト セミコロン (;)、ブラインド カーボン コピー (BCC) メッセージの受信者の表示名にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1c24-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1c24-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1c24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1c24-107">PR_DISPLAY_BCC、PR_DISPLAY_BCC_A、PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="b1c24-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="b1c24-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b1c24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1c24-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="b1c24-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="b1c24-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1c24-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1c24-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1c24-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b1c24-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b1c24-112">Area:</span></span>  <br/> |<span data-ttu-id="b1c24-113">Message</span><span class="sxs-lookup"><span data-stu-id="b1c24-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1c24-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b1c24-114">Remarks</span></span>

<span data-ttu-id="b1c24-115">メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="b1c24-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="b1c24-116">メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="b1c24-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="b1c24-117">値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しごとの時間に同期されます。</span><span class="sxs-lookup"><span data-stu-id="b1c24-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="b1c24-118">ブラインド カーボン コピー受信者、メッセージがない場合は、S_OK と空の文字列の戻り値を持つ[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出す**PR_DISPLAY_BCC**のメッセージ ・ ストアの応答です。</span><span class="sxs-lookup"><span data-stu-id="b1c24-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="b1c24-119">ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="b1c24-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="b1c24-120">すべての名前をローカライズすることがあります。</span><span class="sxs-lookup"><span data-stu-id="b1c24-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="b1c24-121">**PR_DISPLAY_BCC**、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、およびプロパティの**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の名を区切るために使用される文字にセミコロンがあります。</span><span class="sxs-lookup"><span data-stu-id="b1c24-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="b1c24-122">MAPI 受信者の名前にセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b1c24-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="b1c24-123">クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前にこのプロパティのローカライズされた区切り記号で発生した各セミコロンを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1c24-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="b1c24-124">メッセージを転送するには、クライアントでは、ブラインド カーボン コピー受信者行の区切り文字に変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b1c24-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="b1c24-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1c24-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1c24-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1c24-126">Protocol specifications</span></span>

<span data-ttu-id="b1c24-127">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1c24-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1c24-128">クライアント上のフォルダーを共有に関連する情報の送信に使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1c24-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1c24-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b1c24-129">Header files</span></span>

<span data-ttu-id="b1c24-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1c24-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1c24-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1c24-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1c24-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1c24-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b1c24-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1c24-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1c24-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1c24-134">See also</span></span>



[<span data-ttu-id="b1c24-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1c24-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1c24-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1c24-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1c24-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1c24-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1c24-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1c24-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

