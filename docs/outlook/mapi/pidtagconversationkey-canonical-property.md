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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389765"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="f926a-103">PidTagConversationKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f926a-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="f926a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f926a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f926a-105">**IPM を検索するときにのみ、Microsoft Outlook で使用される対話鍵が含まれています。MessageManager** Post Office プロトコル (POP3) アカウントのダウンロードの履歴を格納しているメッセージなどのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="f926a-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="f926a-106">Microsoft Exchange Server で、このプロパティは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="f926a-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f926a-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f926a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f926a-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="f926a-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="f926a-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="f926a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f926a-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="f926a-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="f926a-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f926a-111">Data type:</span></span>  <br/> |<span data-ttu-id="f926a-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f926a-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f926a-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="f926a-113">Area:</span></span>  <br/> |<span data-ttu-id="f926a-114">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="f926a-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f926a-115">備考</span><span class="sxs-lookup"><span data-stu-id="f926a-115">Remarks</span></span>

<span data-ttu-id="f926a-116">会話メッセージのプロパティを[トランスポート ニュートラル カプセル化形式 (TNEF)](transport-neutral-encapsulation-format-tnef.md)に変換すると電子メール メッセージにアクセスするときに、このプロパティを使用できません。代わりに、 [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)および[PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)の標準的なプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f926a-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f926a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f926a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f926a-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f926a-118">Protocol specifications</span></span>

<span data-ttu-id="f926a-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f926a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f926a-120">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f926a-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f926a-121">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f926a-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f926a-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f926a-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="f926a-123">[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f926a-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f926a-124">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="f926a-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f926a-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f926a-125">Header files</span></span>

<span data-ttu-id="f926a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f926a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f926a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f926a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f926a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f926a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f926a-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f926a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f926a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f926a-130">See also</span></span>



[<span data-ttu-id="f926a-131">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="f926a-131">IPM Subtree</span></span>](ipm-subtree.md)
  
<span data-ttu-id="f926a-132">[MAPI ���ʂȃt�H���_�[](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="f926a-132">[MAPI Special Folders](mapi-special-folders.md)</span></span>
  
[<span data-ttu-id="f926a-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f926a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f926a-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f926a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f926a-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f926a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f926a-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f926a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

