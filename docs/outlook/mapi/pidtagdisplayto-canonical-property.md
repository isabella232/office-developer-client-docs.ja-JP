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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396044"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="ec67e-103">PidTagDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec67e-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="ec67e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec67e-105">プライマリ (する、セミコロン (;)、メッセージの受信者) の表示名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec67e-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec67e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ec67e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec67e-107">PR_DISPLAY_TO、PR_DISPLAY_TO_A、PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="ec67e-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="ec67e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ec67e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec67e-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="ec67e-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="ec67e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ec67e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec67e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec67e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ec67e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ec67e-112">Area:</span></span>  <br/> |<span data-ttu-id="ec67e-113">Message</span><span class="sxs-lookup"><span data-stu-id="ec67e-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec67e-114">備考</span><span class="sxs-lookup"><span data-stu-id="ec67e-114">Remarks</span></span>

<span data-ttu-id="ec67e-115">メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="ec67e-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="ec67e-116">メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="ec67e-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="ec67e-117">値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しごとの時間に同期されます。</span><span class="sxs-lookup"><span data-stu-id="ec67e-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="ec67e-118">プライマリ受信者、メッセージがない場合は、メッセージ ・ ストア応答、 [IMAPIProp::GetProps](imapiprop-getprops.md)呼び出しの戻り値が S_OK と空の文字列の**PR_DISPLAY_TO**にします。</span><span class="sxs-lookup"><span data-stu-id="ec67e-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="ec67e-119">ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="ec67e-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="ec67e-120">すべての名前をローカライズすることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec67e-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="ec67e-121">セミコロンで**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、およびプロパティの**PR_DISPLAY_TO**名を区切るために使用される文字があります。</span><span class="sxs-lookup"><span data-stu-id="ec67e-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="ec67e-122">MAPI 受信者の名前にセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ec67e-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="ec67e-123">クライアントで発生した各セミコロンを付ける必要があります**PR_DISPLAY_TO**とユーザー ・ インタ フェースの情報を表示する前にローカライズされた区切り記号に関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ec67e-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="ec67e-124">メッセージを転送するには、クライアントでは、プライマリ受信者行の区切り文字に変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ec67e-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="ec67e-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ec67e-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec67e-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ec67e-126">Protocol specifications</span></span>

<span data-ttu-id="ec67e-127">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec67e-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec67e-128">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec67e-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec67e-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ec67e-129">Header files</span></span>

<span data-ttu-id="ec67e-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec67e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec67e-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec67e-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec67e-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec67e-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ec67e-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec67e-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec67e-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec67e-134">See also</span></span>



[<span data-ttu-id="ec67e-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec67e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec67e-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec67e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec67e-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec67e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec67e-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ec67e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

