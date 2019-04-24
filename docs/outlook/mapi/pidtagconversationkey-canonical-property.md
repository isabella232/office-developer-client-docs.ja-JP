---
title: PidTagConversationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334700"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="d7779-103">PidTagConversationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7779-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="d7779-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7779-105">IPM を検索するときにのみ、Microsoft Outlook で使用される会話キーが含まれ**ます。MessageManager**メッセージ (Post Office Protocol (POP3) アカウントのダウンロード履歴が含まれているメッセージなど)。</span><span class="sxs-lookup"><span data-stu-id="d7779-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="d7779-106">このプロパティは、Microsoft Exchange Server では廃止されました。</span><span class="sxs-lookup"><span data-stu-id="d7779-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7779-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d7779-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7779-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="d7779-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="d7779-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="d7779-109">Identifier:</span></span>  <br/> |<span data-ttu-id="d7779-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="d7779-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="d7779-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d7779-111">Data type:</span></span>  <br/> |<span data-ttu-id="d7779-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7779-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7779-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="d7779-113">Area:</span></span>  <br/> |<span data-ttu-id="d7779-114">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="d7779-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7779-115">解説</span><span class="sxs-lookup"><span data-stu-id="d7779-115">Remarks</span></span>

<span data-ttu-id="d7779-116">会話として電子メールメッセージにアクセスし、メッセージのプロパティを[トランスポートに中立的なカプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換する場合は、このプロパティを使用しないでください。代わりに、 [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)プロパティと[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)標準プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d7779-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d7779-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d7779-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7779-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d7779-118">Protocol specifications</span></span>

<span data-ttu-id="d7779-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7779-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7779-120">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7779-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7779-121">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7779-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7779-122">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7779-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="d7779-123">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7779-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7779-124">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="d7779-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7779-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d7779-125">Header files</span></span>

<span data-ttu-id="d7779-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7779-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7779-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7779-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7779-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d7779-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d7779-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7779-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7779-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7779-130">See also</span></span>



[<span data-ttu-id="d7779-131">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="d7779-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="d7779-132">MAPI の特殊フォルダー</span><span class="sxs-lookup"><span data-stu-id="d7779-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="d7779-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d7779-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7779-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7779-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7779-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7779-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7779-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7779-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

