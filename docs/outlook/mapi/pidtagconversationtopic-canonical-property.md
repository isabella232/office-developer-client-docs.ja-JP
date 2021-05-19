---
title: PidTagConversationTopic 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334686"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="d9e98-103">PidTagConversationTopic 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9e98-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="d9e98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9e98-105">会話スレッドの最初のメッセージのトピックを含む。</span><span class="sxs-lookup"><span data-stu-id="d9e98-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9e98-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d9e98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9e98-107">PR_CONVERSATION_TOPIC、PR_CONVERSATION_TOPIC_A、PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="d9e98-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="d9e98-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d9e98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9e98-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="d9e98-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="d9e98-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d9e98-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9e98-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9e98-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d9e98-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d9e98-112">Area:</span></span>  <br/> |<span data-ttu-id="d9e98-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d9e98-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9e98-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d9e98-114">Remarks</span></span>

<span data-ttu-id="d9e98-115">会話スレッドは、一連のメッセージと返信を表します。</span><span class="sxs-lookup"><span data-stu-id="d9e98-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="d9e98-116">これらのプロパティは、スレッド内の最初のメッセージに対して設定され、通常は PR_NORMALIZED_SUBJECT **(** [PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティに設定されます。</span><span class="sxs-lookup"><span data-stu-id="d9e98-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="d9e98-117">スレッド内の後続のメッセージでは、変更せずに同じトピックを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e98-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="d9e98-118">プロパティ **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティは、後続のメッセージと返信の順序関係を示します。</span><span class="sxs-lookup"><span data-stu-id="d9e98-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="d9e98-119">これらのプロパティが設定されている場合でも、その使用はオプションです。</span><span class="sxs-lookup"><span data-stu-id="d9e98-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="d9e98-120">メッセージ ストア プロバイダーには、これらのプロパティが常に受信メッセージまたは送信メッセージに設定されるのを保証するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="d9e98-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="d9e98-121">これらのプロパティが既に設定されている場合は、変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e98-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="d9e98-122">指定しない場合は、これらの値を [PR_NORMALIZED_SUBJECT] **に設定できます**。</span><span class="sxs-lookup"><span data-stu-id="d9e98-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="d9e98-123">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に、すべてのアクションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e98-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9e98-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d9e98-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9e98-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d9e98-125">Protocol specifications</span></span>

<span data-ttu-id="d9e98-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9e98-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9e98-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="d9e98-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9e98-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9e98-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9e98-129">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9e98-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9e98-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d9e98-130">Header files</span></span>

<span data-ttu-id="d9e98-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9e98-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9e98-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9e98-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9e98-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9e98-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d9e98-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d9e98-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9e98-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9e98-135">See also</span></span>



[<span data-ttu-id="d9e98-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d9e98-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9e98-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9e98-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9e98-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d9e98-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9e98-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d9e98-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

