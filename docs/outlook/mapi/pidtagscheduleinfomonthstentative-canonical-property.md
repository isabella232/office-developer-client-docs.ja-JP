---
title: PidTagScheduleInfoMonthsTentative の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803477"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="518e4-103">PidTagScheduleInfoMonthsTentative の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="518e4-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="518e4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="518e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="518e4-105">仮の予定の空き時間情報メッセージにマークされている月が含まれています。</span><span class="sxs-lookup"><span data-stu-id="518e4-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="518e4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="518e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="518e4-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="518e4-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="518e4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="518e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="518e4-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="518e4-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="518e4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="518e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="518e4-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="518e4-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="518e4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="518e4-112">Area:</span></span>  <br/> |<span data-ttu-id="518e4-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="518e4-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="518e4-114">備考</span><span class="sxs-lookup"><span data-stu-id="518e4-114">Remarks</span></span>

<span data-ttu-id="518e4-115">このプロパティの値の数が 0 と**PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) と**PR_FREEBUSY_PUBLISH_END の間の期間は、公開の範囲は、対象とする月の数との間にする必要があります。**([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="518e4-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="518e4-116">このプロパティの各値は、月と年のことでエンコードが。</span><span class="sxs-lookup"><span data-stu-id="518e4-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="518e4-117">これは、グレゴリオ暦の年と月を基づく年 × 16 + 月の式を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="518e4-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="518e4-118">値は昇順で並べ替えられます、リトル エンディアン形式でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="518e4-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="518e4-119">イベントは、複数の月または複数年にわたって分散は、公開の範囲に該当する月の 1 つの値が必要があります。</span><span class="sxs-lookup"><span data-stu-id="518e4-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="518e4-120">公開の範囲内に仮の予定のイベントがない場合は、し、このプロパティは、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) 設定する必要がないまたは既に存在する場合に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="518e4-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="518e4-121">それ以外の場合、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="518e4-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="518e4-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="518e4-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="518e4-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="518e4-123">Protocol specifications</span></span>

<span data-ttu-id="518e4-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="518e4-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="518e4-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="518e4-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="518e4-126">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="518e4-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="518e4-127">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="518e4-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="518e4-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="518e4-128">Header files</span></span>

<span data-ttu-id="518e4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="518e4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="518e4-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="518e4-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="518e4-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="518e4-131">Mapitags.h</span></span>
  
> <span data-ttu-id="518e4-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="518e4-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="518e4-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="518e4-133">See also</span></span>



[<span data-ttu-id="518e4-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="518e4-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="518e4-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="518e4-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="518e4-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="518e4-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="518e4-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="518e4-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

