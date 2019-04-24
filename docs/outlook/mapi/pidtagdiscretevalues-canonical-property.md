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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360824"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="33668-103">PidTagDiscreteValues 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33668-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="33668-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33668-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33668-105">リスト全体ではなく、配布リストの個々のメンバーにのみ配信不能レポートが適用される場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33668-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33668-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="33668-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33668-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="33668-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="33668-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="33668-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33668-109">0x0e0e</span><span class="sxs-lookup"><span data-stu-id="33668-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="33668-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="33668-110">Data type:</span></span>  <br/> |<span data-ttu-id="33668-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="33668-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="33668-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="33668-112">Area:</span></span>  <br/> |<span data-ttu-id="33668-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="33668-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33668-114">解説</span><span class="sxs-lookup"><span data-stu-id="33668-114">Remarks</span></span>

<span data-ttu-id="33668-115">このプロパティは、メッセージが配布リストの1つ以上のメンバーに配信できなかった場合に、配信不能レポート内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="33668-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="33668-116">この目的は、再送信の試行を、配布リスト全体ではなく、個々のメンバーのみに制限することです。</span><span class="sxs-lookup"><span data-stu-id="33668-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="33668-117">配信不能レポートの recipient テーブルには、そのメッセージが配信できなかったすべての受信者のエントリと、それが属する配布リスト (存在する場合) のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="33668-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="33668-118">トランスポートプロバイダーは、各配布リストエントリに対してこのプロパティを TRUE に設定し、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、および**PR_SEARCH_KEY**をコピーする必要があります ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を配布リストから**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))、および**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) プロパティを使用して、配布リストのメンバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="33668-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="33668-119">配布リスト以外の配信不能レポート受信者エントリに対して**PR_DISCRETE_VALUES**を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="33668-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33668-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="33668-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="33668-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="33668-121">Header files</span></span>

<span data-ttu-id="33668-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33668-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="33668-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="33668-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="33668-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="33668-124">Mapitags.h</span></span>
  
> <span data-ttu-id="33668-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33668-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33668-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="33668-126">See also</span></span>



[<span data-ttu-id="33668-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="33668-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33668-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33668-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33668-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33668-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33668-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33668-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

