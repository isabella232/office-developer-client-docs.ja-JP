---
title: PidTagConversationTopic の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2e656679fcf76992ec0b648274bd5ffa673b4007
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802636"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="7a7cb-103">PidTagConversationTopic の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7cb-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="7a7cb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a7cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a7cb-105">会話スレッドの最初のメッセージのトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a7cb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a7cb-107">PR_CONVERSATION_TOPIC、PR_CONVERSATION_TOPIC_A、PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="7a7cb-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="7a7cb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a7cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a7cb-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="7a7cb-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="7a7cb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a7cb-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a7cb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7a7cb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7a7cb-112">Area:</span></span>  <br/> |<span data-ttu-id="7a7cb-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="7a7cb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a7cb-114">備考</span><span class="sxs-lookup"><span data-stu-id="7a7cb-114">Remarks</span></span>

<span data-ttu-id="7a7cb-115">会話スレッドは、メッセージと返信の系列を表します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="7a7cb-116">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティには通常、スレッドの最初のメッセージのこれらのプロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="7a7cb-117">スレッド内の後続のメッセージは、変更することがなく同じトピックを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="7a7cb-118">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティでは、後続のメッセージと返信の順序関係を示します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="7a7cb-119">使用はオプションですが、これらのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="7a7cb-120">メッセージ ストア プロバイダーでは、これらのプロパティは常に受信または送信メッセージに対して設定することを保証オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="7a7cb-121">これらのプロパティが既に設定されている場合それらを変更しないようにします。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="7a7cb-122">それ以外の場合は、 **PR_NORMALIZED_SUBJECT**に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="7a7cb-123">したアクションは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7a7cb-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a7cb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a7cb-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7a7cb-125">Protocol specifications</span></span>

<span data-ttu-id="7a7cb-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a7cb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a7cb-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a7cb-128">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a7cb-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a7cb-129">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a7cb-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a7cb-130">Header files</span></span>

<span data-ttu-id="7a7cb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a7cb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a7cb-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a7cb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a7cb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="7a7cb-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a7cb-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a7cb-135">See also</span></span>



[<span data-ttu-id="7a7cb-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7cb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a7cb-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a7cb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a7cb-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7a7cb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a7cb-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7a7cb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

