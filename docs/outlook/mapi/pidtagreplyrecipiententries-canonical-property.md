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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355056"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="35ee5-103">PidTagReplyRecipientEntries 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35ee5-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="35ee5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35ee5-105">返信を取得する受信者のエントリ識別子のサイズの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="35ee5-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35ee5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="35ee5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35ee5-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="35ee5-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="35ee5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35ee5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35ee5-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="35ee5-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="35ee5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="35ee5-110">Data type:</span></span>  <br/> |<span data-ttu-id="35ee5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="35ee5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="35ee5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="35ee5-112">Area:</span></span>  <br/> |<span data-ttu-id="35ee5-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="35ee5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35ee5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="35ee5-114">Remarks</span></span>

<span data-ttu-id="35ee5-115">このプロパティには [FLATENTRYLIST](flatentrylist.md) 構造体が含まれるので、複数値プロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="35ee5-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="35ee5-116">このプロパティが存在しない場合は、PR_SENDER_ENTRYID ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティによって **識別された** ユーザーにのみ返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="35ee5-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="35ee5-117">このプロパティと **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) プロパティが定義されている場合、この 2 つのプロパティで識別される受信者全員に返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="35ee5-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="35ee5-118">トランスポート プロバイダーは、これらのプロパティを使用して、通常の応答ロジックをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="35ee5-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="35ee5-119">このプロパティまたは PR_REPLY_RECIPIENT_NAMES プロパティ **が** 設定されている場合は、他のプロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35ee5-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="35ee5-120">これらのプロパティには同じ数の受信者が含まれている必要があります。また、それらのプロパティには同じ順序で含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="35ee5-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="35ee5-121">これらの要件を満たさないと、予期しない結果が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="35ee5-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35ee5-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35ee5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35ee5-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="35ee5-123">Protocol specifications</span></span>

<span data-ttu-id="35ee5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35ee5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35ee5-125">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="35ee5-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35ee5-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35ee5-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35ee5-127">電子メール メッセージで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="35ee5-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="35ee5-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35ee5-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35ee5-129">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="35ee5-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35ee5-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="35ee5-130">Header files</span></span>

<span data-ttu-id="35ee5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35ee5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="35ee5-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35ee5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="35ee5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35ee5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="35ee5-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="35ee5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35ee5-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="35ee5-135">See also</span></span>



[<span data-ttu-id="35ee5-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="35ee5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35ee5-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35ee5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35ee5-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="35ee5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35ee5-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="35ee5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

