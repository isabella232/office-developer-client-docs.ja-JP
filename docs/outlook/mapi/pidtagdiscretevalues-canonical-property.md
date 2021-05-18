---
title: PidTagDiscreteValues 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404842"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="d7253-103">PidTagDiscreteValues 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7253-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="d7253-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7253-105">配信以外のレポートがリスト全体ではなく配布リストの個別のメンバーにのみ適用される場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="d7253-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7253-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d7253-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7253-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="d7253-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="d7253-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d7253-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7253-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="d7253-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="d7253-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d7253-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7253-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d7253-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d7253-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d7253-112">Area:</span></span>  <br/> |<span data-ttu-id="d7253-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="d7253-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7253-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d7253-114">Remarks</span></span>

<span data-ttu-id="d7253-115">このプロパティは、配布リストの 1 つ以上のメンバーにメッセージを配信できない場合に、配信以外のレポート内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7253-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="d7253-116">その目的は、再送信の試行を、配布リスト全体ではなく、個々のメンバーにのみ制限する目的です。</span><span class="sxs-lookup"><span data-stu-id="d7253-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="d7253-117">配信されないレポートの受信者テーブルには、メッセージを配信できないすべての受信者のエントリと、メッセージが属する配布リスト (その場合) のエントリが含まれる。</span><span class="sxs-lookup"><span data-stu-id="d7253-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="d7253-118">トランスポート プロバイダーは、配布リスト エントリごとにこのプロパティを TRUE に設定する必要があります。 配布リストから **PR_DISPLAY_NAME** [(PidTagDisplayName)、PR_ENTRYID](pidtagdisplayname-canonical-property.md)[(PidTagEntryId)、](pidtagentryid-canonical-property.md)および **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)を配布リストから **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName)](pidtagoriginaldisplayname-canonical-property.md) **、PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)、](pidtagoriginalentryid-canonical-property.md)および PR_ORIGINAL_SEARCH_KEY **(** [PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) プロパティをその配布リストの各メンバーにコピーする必要があります。 </span><span class="sxs-lookup"><span data-stu-id="d7253-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="d7253-119">**PR_DISCRETE_VALUES、** 配布リスト以外の配信レポート受信者エントリに対して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7253-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d7253-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d7253-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d7253-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d7253-121">Header files</span></span>

<span data-ttu-id="d7253-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7253-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7253-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7253-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7253-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7253-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d7253-125">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d7253-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7253-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7253-126">See also</span></span>



[<span data-ttu-id="d7253-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d7253-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7253-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7253-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7253-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d7253-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7253-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d7253-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

