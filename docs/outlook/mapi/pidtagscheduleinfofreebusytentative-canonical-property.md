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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385117"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="47dff-103">PidTagScheduleInfoFreeBusyTentative 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47dff-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="47dff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47dff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47dff-105">空き/予約済み状態の仮の予定の時間のブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="47dff-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47dff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47dff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47dff-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="47dff-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="47dff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="47dff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47dff-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="47dff-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="47dff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47dff-110">Data type:</span></span>  <br/> |<span data-ttu-id="47dff-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="47dff-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="47dff-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="47dff-112">Area:</span></span>  <br/> |<span data-ttu-id="47dff-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="47dff-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47dff-114">備考</span><span class="sxs-lookup"><span data-stu-id="47dff-114">Remarks</span></span>

<span data-ttu-id="47dff-115">このプロパティは、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) の値の数だけの値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="47dff-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="47dff-116">各バイナリ値は、1 か月を表し、 **PR_SCHDINFO_MONTHS_TENTATIVE**で同じインデックス位置の値に対応します。</span><span class="sxs-lookup"><span data-stu-id="47dff-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="47dff-117">バイナリ値は、 **PR_SCHDINFO_MONTHS_TENTATIVE**の値と同じ順序に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="47dff-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="47dff-118">バイナリの値ごとに 1 つまたは複数の 4 バイトのブロックと、それぞれは、最初の 2 バイトの開始時刻と終了時刻をリトル エンディアン形式で 2 番目の 2 バイトで含まれています。</span><span class="sxs-lookup"><span data-stu-id="47dff-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="47dff-119">開始時刻は、午前 0 時、月の最初の日の世界協定時刻 (UTC) と UTC でのイベントの開始時刻との間の分の数です。</span><span class="sxs-lookup"><span data-stu-id="47dff-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="47dff-120">終了時刻は、UTC、月の最初の日の午前 0 時と終了時刻 (utc) イベントの間隔を分単位の数です。</span><span class="sxs-lookup"><span data-stu-id="47dff-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="47dff-121">4 バイトのブロックは、昇順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="47dff-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="47dff-122">連続または重複する時間帯は、ブロックの最初と最後のブロックの終了時刻と終了時刻の開始時刻と開始時刻を 1 つのブロックにマージされます。</span><span class="sxs-lookup"><span data-stu-id="47dff-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="47dff-123">イベントは、複数の月または年の間で分散が場合、は、イベントが 1 か月のいずれか、複数のブロックに分割されます。</span><span class="sxs-lookup"><span data-stu-id="47dff-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="47dff-124">公開の範囲内に仮の予定のイベントがない場合は、し、このプロパティは、 **PR_SCHDINFO_MONTHS_TENTATIVE**設定する必要がないまたは既に存在する場合に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47dff-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="47dff-125">それ以外の場合、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47dff-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47dff-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47dff-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47dff-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47dff-127">Protocol specifications</span></span>

<span data-ttu-id="47dff-128">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47dff-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47dff-129">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47dff-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47dff-130">[[MS OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47dff-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47dff-131">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="47dff-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47dff-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="47dff-132">Header files</span></span>

<span data-ttu-id="47dff-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47dff-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="47dff-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47dff-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="47dff-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47dff-135">Mapitags.h</span></span>
  
> <span data-ttu-id="47dff-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47dff-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47dff-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="47dff-137">See also</span></span>



[<span data-ttu-id="47dff-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47dff-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47dff-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47dff-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47dff-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47dff-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47dff-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47dff-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

