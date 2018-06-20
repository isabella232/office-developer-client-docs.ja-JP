---
title: PidTagConversationKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4aec52497e02e99423fa50f378cd35dbf366c37c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802633"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="b89ca-103">PidTagConversationKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b89ca-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="b89ca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b89ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b89ca-105">**IPM を検索するときにのみ、Microsoft Outlook で使用される対話鍵が含まれています。MessageManager** Post Office プロトコル (POP3) アカウントのダウンロードの履歴を格納しているメッセージなどのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="b89ca-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="b89ca-106">Microsoft Exchange Server で、このプロパティは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="b89ca-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b89ca-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b89ca-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b89ca-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="b89ca-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="b89ca-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="b89ca-109">Identifier:</span></span>  <br/> |<span data-ttu-id="b89ca-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="b89ca-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="b89ca-111">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b89ca-111">Data type:</span></span>  <br/> |<span data-ttu-id="b89ca-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b89ca-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b89ca-113">領域:</span><span class="sxs-lookup"><span data-stu-id="b89ca-113">Area:</span></span>  <br/> |<span data-ttu-id="b89ca-114">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="b89ca-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b89ca-115">備考</span><span class="sxs-lookup"><span data-stu-id="b89ca-115">Remarks</span></span>

<span data-ttu-id="b89ca-116">会話メッセージのプロパティを[トランスポート ニュートラル カプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換すると電子メール メッセージにアクセスするときに、このプロパティを使用できません。代わりに、 [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)および[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)の標準的なプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b89ca-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b89ca-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b89ca-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b89ca-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b89ca-118">Protocol specifications</span></span>

<span data-ttu-id="b89ca-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b89ca-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b89ca-120">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b89ca-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b89ca-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b89ca-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b89ca-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b89ca-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="b89ca-123">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b89ca-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b89ca-124">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="b89ca-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b89ca-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b89ca-125">Header files</span></span>

<span data-ttu-id="b89ca-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b89ca-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b89ca-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b89ca-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b89ca-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b89ca-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b89ca-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b89ca-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b89ca-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="b89ca-130">See also</span></span>



[<span data-ttu-id="b89ca-131">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="b89ca-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="b89ca-132">MAPI の特別なフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="b89ca-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="b89ca-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b89ca-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b89ca-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b89ca-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b89ca-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b89ca-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b89ca-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b89ca-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

