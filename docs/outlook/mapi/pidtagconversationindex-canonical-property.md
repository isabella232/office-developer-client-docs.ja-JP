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
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334721"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="01f03-103">PidTagConversationIndex 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="01f03-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="01f03-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f03-105">会話スレッド内でこのメッセージの相対位置を示すバイナリ値を格納します。</span><span class="sxs-lookup"><span data-stu-id="01f03-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f03-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="01f03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01f03-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="01f03-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="01f03-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="01f03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01f03-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="01f03-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="01f03-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="01f03-110">Data type:</span></span>  <br/> |<span data-ttu-id="01f03-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="01f03-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="01f03-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="01f03-112">Area:</span></span>  <br/> |<span data-ttu-id="01f03-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="01f03-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01f03-114">解説</span><span class="sxs-lookup"><span data-stu-id="01f03-114">Remarks</span></span>

<span data-ttu-id="01f03-115">会話スレッドは、一連のメッセージと返信を表します。</span><span class="sxs-lookup"><span data-stu-id="01f03-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="01f03-116">このプロパティは、通常、連結されたタイムスタンプ値を使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="01f03-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="01f03-117">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) が設定されている場合でも、この use はオプションです。</span><span class="sxs-lookup"><span data-stu-id="01f03-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="01f03-118">MAPI では、スレッドインデックスを作成または更新する[ScCreateConversationIndex](sccreateconversationindex.md)関数が提供されています。</span><span class="sxs-lookup"><span data-stu-id="01f03-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="01f03-119">関数は、現在のインデックス値を、カウントされたバイト配列として取得し、最後にタイムスタンプが連結されたインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="01f03-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="01f03-120">他のメッセージへの返信を表すメッセージでは、 **ScCreateConversationIndex**を使用してこのプロパティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f03-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="01f03-121">メッセージストアプロバイダーには、 **PR_CONVERSATION_INDEX**が受信または送信メッセージで常に設定されることを保証するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="01f03-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="01f03-122">これを行うには、このプロパティが設定されている場合は既存の値、そうでない場合は NULL を使用して、 **ScCreateConversationIndex**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01f03-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="01f03-123">このアクションは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出される前に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f03-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="01f03-124">**PR_CONVERSATION_TOPIC**の同じ値を持つすべてのメッセージをこのプロパティで並べ替えて、メッセージの階層的な関係を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="01f03-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01f03-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="01f03-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01f03-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="01f03-126">Protocol specifications</span></span>

<span data-ttu-id="01f03-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01f03-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01f03-128">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="01f03-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01f03-129">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01f03-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01f03-130">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="01f03-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01f03-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="01f03-131">Header files</span></span>

<span data-ttu-id="01f03-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01f03-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="01f03-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="01f03-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="01f03-134">Mapitags</span><span class="sxs-lookup"><span data-stu-id="01f03-134">Mapitags.h</span></span>
  
> <span data-ttu-id="01f03-135">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="01f03-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01f03-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="01f03-136">See also</span></span>



[<span data-ttu-id="01f03-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="01f03-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01f03-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="01f03-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01f03-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="01f03-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01f03-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="01f03-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

