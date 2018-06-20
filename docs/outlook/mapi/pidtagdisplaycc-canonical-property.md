---
title: PidTagDisplayCc の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6257557a8848c1abbaf8ceb15f719c50e4fec8c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802701"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="8ed4e-103">PidTagDisplayCc の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8ed4e-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="8ed4e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ed4e-105">ASCII のリスト セミコロン (;)、カーボン コピー (CC) メッセージの受信者の表示名にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed4e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ed4e-107">PR_DISPLAY_CC、PR_DISPLAY_CC_A、PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="8ed4e-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="8ed4e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8ed4e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ed4e-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="8ed4e-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="8ed4e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ed4e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ed4e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8ed4e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8ed4e-112">Area:</span></span>  <br/> |<span data-ttu-id="8ed4e-113">Message</span><span class="sxs-lookup"><span data-stu-id="8ed4e-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed4e-114">備考</span><span class="sxs-lookup"><span data-stu-id="8ed4e-114">Remarks</span></span>

<span data-ttu-id="8ed4e-115">メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="8ed4e-116">メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="8ed4e-117">値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)へのすべての呼び出しの時点で同期されます。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="8ed4e-118">カーボン コピー受信者、メッセージがない場合は、メッセージ ・ ストアは S_OK とこれらのプロパティに空の文字列の戻り値を持つ、 [IMAPIProp::GetProps](imapiprop-getprops.md)の呼び出しに応答します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="8ed4e-119">ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="8ed4e-120">すべての名前をローカライズすることがあります。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="8ed4e-121">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC**、およびプロパティの**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の名を区切るために使用される文字にセミコロンがあります。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="8ed4e-122">MAPI 受信者の名前にセミコロンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="8ed4e-123">クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前にこのプロパティのローカライズされた区切り記号で発生した各セミコロンを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="8ed4e-124">メッセージを転送するには、クライアントでは、カーボン コピー受信者行の区切り文字に変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="8ed4e-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8ed4e-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ed4e-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8ed4e-126">Protocol specifications</span></span>

<span data-ttu-id="8ed4e-127">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed4e-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ed4e-128">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ed4e-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8ed4e-129">Header files</span></span>

<span data-ttu-id="8ed4e-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ed4e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ed4e-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ed4e-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ed4e-132">Mapitags.h</span></span>
  
> <span data-ttu-id="8ed4e-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed4e-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ed4e-134">See also</span></span>



[<span data-ttu-id="8ed4e-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8ed4e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ed4e-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8ed4e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ed4e-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8ed4e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ed4e-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8ed4e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

