---
title: PidTagScheduleInfoMonthsTentative 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359760"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="2746e-103">PidTagScheduleInfoMonthsTentative 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2746e-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="2746e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2746e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2746e-105">空き時間情報メッセージに仮のマークが付いた月を含む。</span><span class="sxs-lookup"><span data-stu-id="2746e-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2746e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2746e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2746e-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="2746e-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="2746e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2746e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2746e-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="2746e-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="2746e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2746e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2746e-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2746e-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2746e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2746e-112">Area:</span></span>  <br/> |<span data-ttu-id="2746e-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="2746e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2746e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2746e-114">Remarks</span></span>

<span data-ttu-id="2746e-115">このプロパティの値の数は **、0** から発行範囲でカバーされる月数 (PR_FREEBUSY_PUBLISH_START ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) プロパティと PR_FREEBUSY_PUBLISH_END **(** [PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) プロパティの間の期間である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2746e-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="2746e-116">このプロパティの各値には、月と年がエンコードされています。</span><span class="sxs-lookup"><span data-stu-id="2746e-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="2746e-117">これは、年と月がグレゴリオ暦に基づく "年 × 16 + 月" という式を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="2746e-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="2746e-118">値は昇順で並べ替え、リトル エンド形式でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="2746e-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="2746e-119">イベントが複数の月または複数の年にまたがっている場合は、発行範囲に含める各月に 1 つの値が必要です。</span><span class="sxs-lookup"><span data-stu-id="2746e-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="2746e-120">発行範囲に仮イベントがない場合は、このプロパティと **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) を設定したり、既に存在する場合は削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2746e-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="2746e-121">それ以外の場合は、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2746e-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2746e-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2746e-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2746e-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2746e-123">Protocol specifications</span></span>

<span data-ttu-id="2746e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2746e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2746e-125">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2746e-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2746e-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2746e-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2746e-127">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="2746e-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2746e-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2746e-128">Header files</span></span>

<span data-ttu-id="2746e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2746e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2746e-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2746e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="2746e-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2746e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="2746e-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2746e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2746e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="2746e-133">See also</span></span>



[<span data-ttu-id="2746e-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2746e-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2746e-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2746e-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2746e-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2746e-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2746e-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2746e-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

