---
title: PidTagOriginalSenderEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342617"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="5f5bb-103">PidTagOriginalSenderEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f5bb-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5f5bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f5bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f5bb-105">メッセージの最初のバージョンの送信者 (転送または返信前のメッセージ) のエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f5bb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f5bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f5bb-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5f5bb-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5f5bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5f5bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f5bb-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="5f5bb-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="5f5bb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f5bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f5bb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f5bb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f5bb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5f5bb-112">Area:</span></span>  <br/> |<span data-ttu-id="5f5bb-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="5f5bb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f5bb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5f5bb-114">Remarks</span></span>

<span data-ttu-id="5f5bb-115">このプロパティは、メッセージの元の送信者のアドレス プロパティの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="5f5bb-116">メッセージの最初の送信時に、クライアント アプリケーションは、このプロパティを PR_SENDER_ENTRYID ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティ **の値** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5f5bb-117">メッセージが転送または返信された場合は、変更されません。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f5bb-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f5bb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f5bb-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5f5bb-119">Protocol specifications</span></span>

<span data-ttu-id="5f5bb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f5bb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f5bb-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f5bb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f5bb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f5bb-123">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f5bb-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5f5bb-124">Header files</span></span>

<span data-ttu-id="5f5bb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f5bb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f5bb-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f5bb-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f5bb-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5f5bb-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5f5bb-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f5bb-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f5bb-129">See also</span></span>



[<span data-ttu-id="5f5bb-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5f5bb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f5bb-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f5bb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f5bb-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5f5bb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f5bb-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5f5bb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

