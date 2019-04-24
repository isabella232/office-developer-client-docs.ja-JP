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
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355056"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="93427-103">PidTagReplyRecipientEntries 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="93427-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="93427-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93427-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93427-105">応答を取得する受信者のエントリ識別子のサイズ配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="93427-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93427-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="93427-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93427-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="93427-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="93427-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="93427-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93427-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="93427-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="93427-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="93427-110">Data type:</span></span>  <br/> |<span data-ttu-id="93427-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="93427-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="93427-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="93427-112">Area:</span></span>  <br/> |<span data-ttu-id="93427-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="93427-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93427-114">解説</span><span class="sxs-lookup"><span data-stu-id="93427-114">Remarks</span></span>

<span data-ttu-id="93427-115">このプロパティには、 [FLATENTRYLIST](flatentrylist.md)構造体が含まれており、複数値プロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="93427-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="93427-116">このプロパティが存在しない場合、返信は**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティによって識別されるユーザーにのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="93427-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="93427-117">このプロパティと**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) プロパティを定義すると、この2つのプロパティで指定されたすべての受信者に返信が送信されます。</span><span class="sxs-lookup"><span data-stu-id="93427-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="93427-118">トランスポートプロバイダーは、これらのプロパティを使用して、通常の応答ロジックを上書きします。</span><span class="sxs-lookup"><span data-stu-id="93427-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="93427-119">このプロパティまたは**PR_REPLY_RECIPIENT_NAMES**プロパティのいずれかが設定されている場合は、もう一方のプロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93427-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="93427-120">これらのプロパティには、同じ数の受信者が含まれている必要があります。また、これらのプロパティは同じ順序で格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93427-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="93427-121">これらの要件を遵守できないと、予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="93427-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93427-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="93427-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93427-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="93427-123">Protocol specifications</span></span>

<span data-ttu-id="93427-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93427-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93427-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="93427-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93427-126">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93427-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93427-127">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="93427-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="93427-128">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93427-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93427-129">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="93427-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93427-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="93427-130">Header files</span></span>

<span data-ttu-id="93427-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93427-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="93427-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="93427-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="93427-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="93427-133">Mapitags.h</span></span>
  
> <span data-ttu-id="93427-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="93427-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93427-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="93427-135">See also</span></span>



[<span data-ttu-id="93427-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93427-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93427-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="93427-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93427-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="93427-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93427-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="93427-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

