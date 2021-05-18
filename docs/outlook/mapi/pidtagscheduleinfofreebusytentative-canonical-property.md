---
title: PidTagScheduleInfoFreeBusyTentative 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359775"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="296dd-103">PidTagScheduleInfoFreeBusyTentative 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="296dd-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="296dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="296dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="296dd-105">空き時間情報の状態が暫定的な時間のブロックを含む。</span><span class="sxs-lookup"><span data-stu-id="296dd-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="296dd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="296dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="296dd-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="296dd-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="296dd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="296dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="296dd-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="296dd-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="296dd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="296dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="296dd-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="296dd-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="296dd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="296dd-112">Area:</span></span>  <br/> |<span data-ttu-id="296dd-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="296dd-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="296dd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="296dd-114">Remarks</span></span>

<span data-ttu-id="296dd-115">このプロパティの値の数は、PR_SCHDINFO_MONTHS_TENTATIVE **(** [PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="296dd-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="296dd-116">各バイナリ値は月を表し、同じインデックスの値に **対応** PR_SCHDINFO_MONTHS_TENTATIVE。</span><span class="sxs-lookup"><span data-stu-id="296dd-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="296dd-117">バイナリ値は、バイナリの値と同じ順序で並 **べPR_SCHDINFO_MONTHS_TENTATIVE。**</span><span class="sxs-lookup"><span data-stu-id="296dd-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="296dd-118">各バイナリ値には 1 つ以上の 4 バイト ブロックが含まれます。各ブロックには、最初の 2 バイトの開始時刻と、2 番目の 2 バイトの終了時刻がリトル エンド形式で含まれます。</span><span class="sxs-lookup"><span data-stu-id="296dd-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="296dd-119">開始時刻は、月の最初の日の午前 0 時の協定世界時 (UTC) から UTC でのイベントの開始時刻の間の分数です。</span><span class="sxs-lookup"><span data-stu-id="296dd-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="296dd-120">終了時刻は、月の最初の日の午前 0 時 UTC から UTC でのイベントの終了時刻の間の分数です。</span><span class="sxs-lookup"><span data-stu-id="296dd-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="296dd-121">4 バイト ブロックは昇順に並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="296dd-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="296dd-122">連続または重複する時間ブロックは、最初のブロックの開始時刻として開始時刻を、最後のブロックの終了時刻として終了時刻として 1 つのブロックに結合されます。</span><span class="sxs-lookup"><span data-stu-id="296dd-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="296dd-123">イベントが複数の月または年にまたがっている場合、イベントは月ごとに 1 つ、複数のブロックに分割されます。</span><span class="sxs-lookup"><span data-stu-id="296dd-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="296dd-124">発行範囲に仮イベントがない場合は、このプロパティと PR_SCHDINFO_MONTHS_TENTATIVE を設定しないか、既に存在する場合は削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="296dd-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="296dd-125">それ以外の場合は、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="296dd-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="296dd-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="296dd-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="296dd-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="296dd-127">Protocol specifications</span></span>

<span data-ttu-id="296dd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296dd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296dd-129">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="296dd-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="296dd-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296dd-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296dd-131">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="296dd-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="296dd-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="296dd-132">Header files</span></span>

<span data-ttu-id="296dd-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="296dd-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="296dd-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="296dd-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="296dd-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="296dd-135">Mapitags.h</span></span>
  
> <span data-ttu-id="296dd-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="296dd-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="296dd-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="296dd-137">See also</span></span>



[<span data-ttu-id="296dd-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="296dd-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="296dd-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="296dd-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="296dd-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="296dd-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="296dd-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="296dd-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

