---
title: PidTagReplyRecipientNames の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5abbe14576bec9f03f0b1bf5578b68032f95f8a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803331"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="ef38b-103">PidTagReplyRecipientNames の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ef38b-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="ef38b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef38b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef38b-105">応答を取得するのには受信者の表示名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ef38b-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef38b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ef38b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef38b-107">PR_REPLY_RECIPIENT_NAMES、PR_REPLY_RECIPIENT_NAMES_A、PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="ef38b-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="ef38b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ef38b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef38b-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="ef38b-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="ef38b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef38b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef38b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ef38b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ef38b-112">Area:</span></span>  <br/> |<span data-ttu-id="ef38b-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="ef38b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef38b-114">備考</span><span class="sxs-lookup"><span data-stu-id="ef38b-114">Remarks</span></span>

<span data-ttu-id="ef38b-115">これらのプロパティには、セミコロンで区切られた表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ef38b-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="ef38b-116">このプロパティが存在しない場合は、返信は**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) のプロパティで指定されたユーザーにのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="ef38b-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="ef38b-117">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) とこれらのプロパティが定義されている場合、これら 2 つのプロパティで識別される受信者全員に返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="ef38b-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="ef38b-118">トランスポート プロバイダーは、通常の応答のロジックをオーバーライドするのには、これらのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="ef38b-119">**PR_REPLY_RECIPIENT_ENTRIES**またはこれらのプロパティのいずれかが設定されている場合も、他のプロパティを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ef38b-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="ef38b-120">これらのプロパティは、同じ数の受信者を含める必要があり、同じ順序でそれらに含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef38b-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="ef38b-121">これらの要件を遵守すると、可能性が予期しない結果です。</span><span class="sxs-lookup"><span data-stu-id="ef38b-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ef38b-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ef38b-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef38b-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ef38b-123">Protocol specifications</span></span>

<span data-ttu-id="ef38b-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef38b-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef38b-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef38b-126">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef38b-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef38b-127">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="ef38b-128">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef38b-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef38b-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef38b-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ef38b-130">Header files</span></span>

<span data-ttu-id="ef38b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef38b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef38b-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ef38b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef38b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef38b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ef38b-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ef38b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef38b-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef38b-135">See also</span></span>



[<span data-ttu-id="ef38b-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ef38b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef38b-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ef38b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef38b-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ef38b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef38b-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ef38b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

