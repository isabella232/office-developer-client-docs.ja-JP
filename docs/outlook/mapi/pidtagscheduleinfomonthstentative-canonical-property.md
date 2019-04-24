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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359760"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="53f11-103">PidTagScheduleInfoMonthsTentative 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53f11-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="53f11-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53f11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53f11-105">空き時間情報メッセージで仮の予定としてマークされた月を含みます。</span><span class="sxs-lookup"><span data-stu-id="53f11-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53f11-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="53f11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53f11-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="53f11-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="53f11-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="53f11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53f11-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="53f11-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="53f11-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="53f11-110">Data type:</span></span>  <br/> |<span data-ttu-id="53f11-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="53f11-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="53f11-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="53f11-112">Area:</span></span>  <br/> |<span data-ttu-id="53f11-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="53f11-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53f11-114">解説</span><span class="sxs-lookup"><span data-stu-id="53f11-114">Remarks</span></span>

<span data-ttu-id="53f11-115">このプロパティの値の数は、0から、公開範囲で指定されている月数 ( **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) と PR_FREEBUSY_PUBLISH_END の間の期間) にする必要があります。 \*\*\*\*([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="53f11-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="53f11-116">このプロパティの各値には、月と年がエンコードされています。</span><span class="sxs-lookup"><span data-stu-id="53f11-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="53f11-117">これは、"year × 16 + 月" という式を使用して計算されます。ここでは、年と月はグレゴリオ暦に基づいています。</span><span class="sxs-lookup"><span data-stu-id="53f11-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="53f11-118">値は昇順で並べ替えられ、リトルエンディアン形式でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="53f11-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="53f11-119">イベントが複数の月または複数年にわたる場合は、発行範囲に含まれる各月に1つの値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="53f11-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="53f11-120">発行範囲に一時的なイベントがない場合は、このプロパティと**PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) を設定しないでください。または、既に存在する場合は削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53f11-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="53f11-121">それ以外の場合は、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53f11-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53f11-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="53f11-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53f11-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="53f11-123">Protocol specifications</span></span>

<span data-ttu-id="53f11-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53f11-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53f11-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="53f11-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53f11-126">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53f11-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53f11-127">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="53f11-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53f11-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="53f11-128">Header files</span></span>

<span data-ttu-id="53f11-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53f11-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="53f11-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="53f11-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="53f11-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="53f11-131">Mapitags.h</span></span>
  
> <span data-ttu-id="53f11-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53f11-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53f11-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="53f11-133">See also</span></span>



[<span data-ttu-id="53f11-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="53f11-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53f11-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53f11-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53f11-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="53f11-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53f11-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="53f11-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

