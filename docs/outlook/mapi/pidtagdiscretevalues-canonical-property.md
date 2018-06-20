---
title: PidTagDiscreteValues の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802708"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="e9ce4-103">PidTagDiscreteValues の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ce4-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="e9ce4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9ce4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9ce4-105">配信不能レポートは、リスト全体ではなく、配布リストのみを個別のメンバーを適用する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9ce4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9ce4-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="e9ce4-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="e9ce4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e9ce4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9ce4-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="e9ce4-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="e9ce4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9ce4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e9ce4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e9ce4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e9ce4-112">Area:</span></span>  <br/> |<span data-ttu-id="e9ce4-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9ce4-114">備考</span><span class="sxs-lookup"><span data-stu-id="e9ce4-114">Remarks</span></span>

<span data-ttu-id="e9ce4-115">配布リストの 1 つまたは複数のメンバーにメッセージを配信できませんでしたと、配信不能レポート内でこのプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="e9ce4-116">その目的は、再送信を制限しようとすると個々 のメンバーだけと、配布リストではなく、全体としてです。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="e9ce4-117">配信不能レポートの受信者テーブルが含まれていますエントリにはユーザーのメッセージ配信できませんでした、すべての受信者および配布リストで、該当する場合、所属しています。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="e9ce4-118">トランスポート プロバイダーは、各配布リストのエントリの場合は TRUE にこのプロパティを設定する必要があり。、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) および**PR_SEARCH_KEY** ([をコピーする必要があります。PidTagSearchKey](pidtagsearchkey-canonical-property.md)) **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) および**PR_ORIGINAL_SEARCH_KEY** ([の配布リストからPidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) その配布リストの各メンバーのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="e9ce4-119">配信不能レポートの受信者のエントリ、配布リスト以外の**PR_DISCRETE_VALUES**を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9ce4-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9ce4-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e9ce4-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9ce4-121">Header files</span></span>

<span data-ttu-id="e9ce4-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9ce4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9ce4-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9ce4-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9ce4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e9ce4-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9ce4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9ce4-126">See also</span></span>



[<span data-ttu-id="e9ce4-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ce4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9ce4-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9ce4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9ce4-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e9ce4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9ce4-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e9ce4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

