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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340979"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="ad30f-103">PidTagOriginalSentRepresentingSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad30f-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ad30f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad30f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad30f-105">元のメッセージが送信されたメッセージング ユーザーの検索キーを格納します。</span><span class="sxs-lookup"><span data-stu-id="ad30f-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad30f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ad30f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad30f-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ad30f-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ad30f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ad30f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad30f-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="ad30f-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="ad30f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ad30f-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad30f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ad30f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ad30f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ad30f-112">Area:</span></span>  <br/> |<span data-ttu-id="ad30f-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="ad30f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad30f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ad30f-114">Remarks</span></span>

<span data-ttu-id="ad30f-115">このプロパティは、メッセージの元の送信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ad30f-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="ad30f-116">会話スレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad30f-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="ad30f-117">別のクライアントに代わってメッセージを送信するクライアント アプリケーションは、このプロパティをメッセージの最初の送信時に **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad30f-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="ad30f-118">一度設定した場合は、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ad30f-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad30f-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ad30f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad30f-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ad30f-120">Protocol specifications</span></span>

<span data-ttu-id="ad30f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad30f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad30f-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ad30f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad30f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad30f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad30f-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad30f-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad30f-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ad30f-125">Header files</span></span>

<span data-ttu-id="ad30f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad30f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad30f-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad30f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad30f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad30f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ad30f-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ad30f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad30f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad30f-130">See also</span></span>



[<span data-ttu-id="ad30f-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ad30f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad30f-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad30f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad30f-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ad30f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad30f-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ad30f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

