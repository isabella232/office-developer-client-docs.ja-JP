---
title: PidTagConversationIndex 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bddb667cba99e240a6ce182c9c1c8ed47f467e15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802630"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="ded1c-103">PidTagConversationIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ded1c-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="ded1c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ded1c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ded1c-105">会話スレッド内でこのメッセージの相対的な位置を示すバイナリ値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ded1c-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ded1c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ded1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ded1c-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="ded1c-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="ded1c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ded1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ded1c-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="ded1c-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="ded1c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ded1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ded1c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ded1c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ded1c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ded1c-112">Area:</span></span>  <br/> |<span data-ttu-id="ded1c-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="ded1c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ded1c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ded1c-114">Remarks</span></span>

<span data-ttu-id="ded1c-115">会話スレッドは、メッセージと返信の系列を表します。</span><span class="sxs-lookup"><span data-stu-id="ded1c-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="ded1c-116">通常連結されたタイムスタンプ値を使用してこのプロパティが実装されます。</span><span class="sxs-lookup"><span data-stu-id="ded1c-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="ded1c-117">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) が設定されている場合でもの使用はオプションですが。</span><span class="sxs-lookup"><span data-stu-id="ded1c-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="ded1c-118">MAPI には、作成または会話のインデックスを更新する[ScCreateConversationIndex](sccreateconversationindex.md)関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="ded1c-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="ded1c-119">関数は、長さのバイト配列として現在のインデックス値を受け取るし、最後に連結するタイムスタンプを持つインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="ded1c-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="ded1c-120">別のメッセージへの応答を表すメッセージは、このプロパティを更新するのには**ScCreateConversationIndex**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ded1c-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="ded1c-121">メッセージ ストア プロバイダーでは、 **PR_CONVERSATION_INDEX**は常に受信または送信メッセージに対して設定することを保証オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ded1c-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="ded1c-122">この**ScCreateConversationIndex**では、このプロパティが設定されている場合は、既存の値または NULL でない場合のいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ded1c-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="ded1c-123">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に、このアクションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ded1c-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="ded1c-124">**PR_CONVERSATION_TOPIC**に対して同じ値を持つすべてのメッセージは、メッセージの階層関係を表示するには、このプロパティで並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="ded1c-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ded1c-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ded1c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ded1c-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ded1c-126">Protocol specifications</span></span>

<span data-ttu-id="ded1c-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ded1c-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ded1c-128">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ded1c-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ded1c-129">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ded1c-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ded1c-130">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ded1c-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ded1c-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ded1c-131">Header files</span></span>

<span data-ttu-id="ded1c-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ded1c-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="ded1c-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ded1c-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="ded1c-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ded1c-134">Mapitags.h</span></span>
  
> <span data-ttu-id="ded1c-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ded1c-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ded1c-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ded1c-136">See also</span></span>



[<span data-ttu-id="ded1c-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ded1c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ded1c-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ded1c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ded1c-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ded1c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ded1c-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ded1c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

