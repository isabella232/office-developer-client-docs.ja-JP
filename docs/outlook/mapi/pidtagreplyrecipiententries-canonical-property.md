---
title: PidTagReplyRecipientEntries 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803330"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="70872-103">PidTagReplyRecipientEntries 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70872-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="70872-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70872-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70872-105">応答を取得するのには受信者のエントリ id のサイズの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="70872-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70872-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="70872-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70872-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="70872-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="70872-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="70872-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70872-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="70872-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="70872-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="70872-110">Data type:</span></span>  <br/> |<span data-ttu-id="70872-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70872-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70872-112">領域:</span><span class="sxs-lookup"><span data-stu-id="70872-112">Area:</span></span>  <br/> |<span data-ttu-id="70872-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="70872-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70872-114">注釈</span><span class="sxs-lookup"><span data-stu-id="70872-114">Remarks</span></span>

<span data-ttu-id="70872-115">このプロパティは、 [FLATENTRYLIST](flatentrylist.md)構造体を格納し、複数値を持つプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="70872-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="70872-116">このプロパティが存在しない場合は、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) のプロパティで指定されたユーザーのみに返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="70872-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="70872-117">これと**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) のプロパティが定義されている場合、これら 2 つのプロパティで識別される受信者全員に返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="70872-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="70872-118">トランスポート プロバイダーは、通常の応答のロジックをオーバーライドするのには、これらのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="70872-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="70872-119">このプロパティまたは**PR_REPLY_RECIPIENT_NAMES**プロパティが設定されている場合も、他のプロパティを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="70872-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="70872-120">これらのプロパティは、同じ数の受信者を含める必要があり、同じ順序でそれらに含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70872-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="70872-121">これらの要件を遵守すると、可能性が予期しない結果です。</span><span class="sxs-lookup"><span data-stu-id="70872-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70872-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="70872-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70872-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="70872-123">Protocol specifications</span></span>

<span data-ttu-id="70872-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70872-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70872-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="70872-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70872-126">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70872-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70872-127">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="70872-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="70872-128">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70872-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70872-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="70872-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70872-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="70872-130">Header files</span></span>

<span data-ttu-id="70872-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70872-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="70872-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="70872-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="70872-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70872-133">Mapitags.h</span></span>
  
> <span data-ttu-id="70872-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="70872-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70872-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="70872-135">See also</span></span>



[<span data-ttu-id="70872-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="70872-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70872-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="70872-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70872-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="70872-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70872-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="70872-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

