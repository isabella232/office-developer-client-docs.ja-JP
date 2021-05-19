---
title: PidTagConversationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334700"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="e520f-103">PidTagConversationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e520f-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="e520f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e520f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e520f-105">IpM の検索時にのみ、Microsoft Outlook会話キーが **格納されます。Post Office** プロトコル (POP3) アカウントのダウンロード履歴を含むメッセージなど、MessageManager メッセージ。</span><span class="sxs-lookup"><span data-stu-id="e520f-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="e520f-106">このプロパティは、このプロパティのMicrosoft Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="e520f-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e520f-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e520f-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e520f-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="e520f-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="e520f-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="e520f-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e520f-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="e520f-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="e520f-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e520f-111">Data type:</span></span>  <br/> |<span data-ttu-id="e520f-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e520f-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e520f-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="e520f-113">Area:</span></span>  <br/> |<span data-ttu-id="e520f-114">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="e520f-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e520f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="e520f-115">Remarks</span></span>

<span data-ttu-id="e520f-116">電子メール メッセージに会話としてアクセスし、メッセージ プロパティを [Transport-Neutral カプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換する場合は、このプロパティを使用しません。代わりに [、PidTagConversationIndex および](pidtagconversationindex-canonical-property.md) [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) 標準プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e520f-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e520f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e520f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e520f-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e520f-118">Protocol specifications</span></span>

<span data-ttu-id="e520f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e520f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e520f-120">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e520f-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e520f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e520f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e520f-122">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e520f-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="e520f-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e520f-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e520f-124">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="e520f-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e520f-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e520f-125">Header files</span></span>

<span data-ttu-id="e520f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e520f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e520f-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e520f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e520f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e520f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e520f-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e520f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e520f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e520f-130">See also</span></span>



[<span data-ttu-id="e520f-131">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="e520f-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="e520f-132">MAPI の特別なフォルダー</span><span class="sxs-lookup"><span data-stu-id="e520f-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="e520f-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e520f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e520f-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e520f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e520f-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e520f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e520f-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e520f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

