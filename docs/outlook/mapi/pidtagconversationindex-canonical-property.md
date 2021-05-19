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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334721"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="dc285-103">PidTagConversationIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc285-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="dc285-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc285-105">会話スレッド内のこのメッセージの相対位置を示すバイナリ値を含む。</span><span class="sxs-lookup"><span data-stu-id="dc285-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc285-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dc285-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc285-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="dc285-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="dc285-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dc285-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc285-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="dc285-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="dc285-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dc285-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc285-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dc285-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dc285-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="dc285-112">Area:</span></span>  <br/> |<span data-ttu-id="dc285-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="dc285-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc285-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dc285-114">Remarks</span></span>

<span data-ttu-id="dc285-115">会話スレッドは、一連のメッセージと返信を表します。</span><span class="sxs-lookup"><span data-stu-id="dc285-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="dc285-116">このプロパティは、通常、連結されたタイム スタンプ値を使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="dc285-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="dc285-117">この使用は省略可能です [(pidTagConversationTopic](pidtagconversationtopic-canonical-property.md) **)** がPR_CONVERSATION_TOPIC設定されている場合でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc285-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="dc285-118">MAPI は [、会話インデックスを作成または更新する ScCreateConversationIndex](sccreateconversationindex.md) 関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc285-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="dc285-119">この関数は、現在のインデックス値をカウントされたバイト配列として受け取り、タイムスタンプが末尾に連結されたインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="dc285-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="dc285-120">別のメッセージへの返信を表すメッセージは **、ScCreateConversationIndex** を使用してこのプロパティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc285-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="dc285-121">メッセージ ストア プロバイダーには、受信メッセージまたは送信メッセージに **PR_CONVERSATION_INDEXメッセージが** 常に設定されるのを保証するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="dc285-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="dc285-122">これを行うには **、ScCreateConversationIndex** を呼び出し、このプロパティが設定されている場合は既存の値を指定するか、設定されていない場合は NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc285-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="dc285-123">このアクションは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出される前に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc285-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="dc285-124">このプロパティで同じ値を持 **PR_CONVERSATION_TOPIC** メッセージを並べ替え、メッセージの階層的な関係を表示できます。</span><span class="sxs-lookup"><span data-stu-id="dc285-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc285-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dc285-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc285-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="dc285-126">Protocol specifications</span></span>

<span data-ttu-id="dc285-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc285-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc285-128">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="dc285-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc285-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc285-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc285-130">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc285-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc285-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dc285-131">Header files</span></span>

<span data-ttu-id="dc285-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc285-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc285-133">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc285-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc285-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc285-134">Mapitags.h</span></span>
  
> <span data-ttu-id="dc285-135">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="dc285-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc285-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc285-136">See also</span></span>



[<span data-ttu-id="dc285-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="dc285-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc285-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc285-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc285-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="dc285-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc285-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="dc285-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

