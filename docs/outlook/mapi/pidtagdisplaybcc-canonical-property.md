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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360817"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="0e5a8-103">PidTagDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e5a8-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="0e5a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5a8-105">ブラインド カーボン コピー (BCC) メッセージ受信者の表示名の ASCII リストをセミコロン (;)) で区切って含;)。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e5a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0e5a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e5a8-107">PR_DISPLAY_BCC、PR_DISPLAY_BCC_A、PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="0e5a8-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="0e5a8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0e5a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e5a8-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="0e5a8-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="0e5a8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0e5a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e5a8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e5a8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0e5a8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0e5a8-112">Area:</span></span>  <br/> |<span data-ttu-id="0e5a8-113">メッセージ</span><span class="sxs-lookup"><span data-stu-id="0e5a8-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e5a8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0e5a8-114">Remarks</span></span>

<span data-ttu-id="0e5a8-115">メッセージ ストアは [、IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを使用して、メッセージ オブジェクトのこれらのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="0e5a8-116">また、メッセージ ストアは、メッセージの最後に保存された状態を常に反映するように、これらのプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="0e5a8-117">値は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出すごとに同期されます。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="0e5a8-118">メッセージにブラインド カーボン コピー受信者がない場合、メッセージ ストアは、S_OK の戻り値と PR_DISPLAY_BCC の空の文字列を持つ [IMAPIProp::GetProps](imapiprop-getprops.md) 呼び **出しに応答する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="0e5a8-119">ローカライズの必要性が考えられるため、MAPI には、すべての受信者名に関する次のガイドラインが記載されています。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="0e5a8-120">すべての名前をローカライズできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="0e5a8-121">**セミコロンは、PR_DISPLAY_BCC 、PR_DISPLAY_CC**([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)プロパティ、およびPR_DISPLAY_TO **(** [PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) プロパティの名前を区切る文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="0e5a8-122">MAPI では、受信者名内でセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="0e5a8-123">クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前に、このプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="0e5a8-124">メッセージを転送する場合、クライアントはブラインド カーボン コピー受信者行の区切り文字を変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0e5a8-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0e5a8-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e5a8-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0e5a8-126">Protocol specifications</span></span>

<span data-ttu-id="0e5a8-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e5a8-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e5a8-128">クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e5a8-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0e5a8-129">Header files</span></span>

<span data-ttu-id="0e5a8-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e5a8-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e5a8-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e5a8-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e5a8-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0e5a8-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="0e5a8-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e5a8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e5a8-134">See also</span></span>



[<span data-ttu-id="0e5a8-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0e5a8-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e5a8-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e5a8-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e5a8-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0e5a8-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e5a8-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0e5a8-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

