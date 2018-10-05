---
title: PidTagOriginalSentRepresentingEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eaf91472794c5188a63897bccaa900c4882407bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395225"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="72959-103">PidTagOriginalSentRepresentingEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72959-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="72959-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72959-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72959-105">元のメッセージが送信されたメッセージのユーザーのエントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="72959-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72959-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="72959-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72959-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="72959-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="72959-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="72959-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72959-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="72959-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="72959-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="72959-110">Data type:</span></span>  <br/> |<span data-ttu-id="72959-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="72959-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="72959-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="72959-112">Area:</span></span>  <br/> |<span data-ttu-id="72959-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="72959-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72959-114">備考</span><span class="sxs-lookup"><span data-stu-id="72959-114">Remarks</span></span>

<span data-ttu-id="72959-115">このプロパティは、メッセージの表示元の送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="72959-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="72959-116">会話のスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="72959-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="72959-117">別のクライアントの代わりにメッセージを送信するクライアント アプリケーションは、メッセージの最初の提出書類に**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72959-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="72959-118">設定すると、そのことはありません変更してください。</span><span class="sxs-lookup"><span data-stu-id="72959-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72959-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="72959-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72959-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="72959-120">Protocol specifications</span></span>

<span data-ttu-id="72959-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72959-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72959-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="72959-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72959-123">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72959-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72959-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="72959-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72959-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="72959-125">Header files</span></span>

<span data-ttu-id="72959-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72959-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="72959-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="72959-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="72959-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72959-128">Mapitags.h</span></span>
  
> <span data-ttu-id="72959-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="72959-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72959-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="72959-130">See also</span></span>



[<span data-ttu-id="72959-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="72959-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72959-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="72959-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72959-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="72959-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72959-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="72959-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

