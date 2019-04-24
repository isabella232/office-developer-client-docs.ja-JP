---
title: PidTagOriginalSentRepresentingSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340979"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="5e43f-103">PidTagOriginalSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e43f-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5e43f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e43f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e43f-105">元のメッセージが送信されたメッセージングユーザーの検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e43f-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e43f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5e43f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e43f-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5e43f-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5e43f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5e43f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e43f-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="5e43f-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="5e43f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5e43f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e43f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e43f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e43f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5e43f-112">Area:</span></span>  <br/> |<span data-ttu-id="5e43f-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="5e43f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e43f-114">解説</span><span class="sxs-lookup"><span data-stu-id="5e43f-114">Remarks</span></span>

<span data-ttu-id="5e43f-115">このプロパティは、元のメッセージの送信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="5e43f-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="5e43f-116">会話スレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e43f-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="5e43f-117">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、最初にメッセージを送信するときに、このプロパティを**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e43f-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="5e43f-118">一度設定すると、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="5e43f-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5e43f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5e43f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e43f-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5e43f-120">Protocol specifications</span></span>

<span data-ttu-id="5e43f-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e43f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e43f-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e43f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e43f-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e43f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e43f-124">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e43f-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e43f-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5e43f-125">Header files</span></span>

<span data-ttu-id="5e43f-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e43f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e43f-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e43f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e43f-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="5e43f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5e43f-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e43f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e43f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e43f-130">See also</span></span>



[<span data-ttu-id="5e43f-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5e43f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e43f-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e43f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e43f-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5e43f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e43f-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5e43f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

