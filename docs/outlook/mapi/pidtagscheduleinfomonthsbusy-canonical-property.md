---
title: PidTagScheduleInfoMonthsBusy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08f8f6e016ff08211bc10e80588ab33e83d6441b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359794"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="ffff5-103">PidTagScheduleInfoMonthsBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffff5-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="ffff5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffff5-105">空き時間情報メッセージに、種類が busy の空き時間情報データが存在する月を含みます。</span><span class="sxs-lookup"><span data-stu-id="ffff5-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffff5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ffff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffff5-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="ffff5-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="ffff5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ffff5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ffff5-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="ffff5-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="ffff5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ffff5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ffff5-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ffff5-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ffff5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ffff5-112">Area:</span></span>  <br/> |<span data-ttu-id="ffff5-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="ffff5-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffff5-114">解説</span><span class="sxs-lookup"><span data-stu-id="ffff5-114">Remarks</span></span>

<span data-ttu-id="ffff5-115">このプロパティの書式、計算、および制約は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) の場合と同じですが、関連付けられている予定表オブジェクトでビジー状態としてマークされている予定を参照します。</span><span class="sxs-lookup"><span data-stu-id="ffff5-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffff5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ffff5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffff5-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ffff5-117">Protocol specifications</span></span>

<span data-ttu-id="ffff5-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffff5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffff5-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffff5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffff5-120">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffff5-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffff5-121">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="ffff5-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffff5-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ffff5-122">Header files</span></span>

<span data-ttu-id="ffff5-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffff5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffff5-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffff5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ffff5-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ffff5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ffff5-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffff5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffff5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffff5-127">See also</span></span>



[<span data-ttu-id="ffff5-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ffff5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffff5-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffff5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffff5-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffff5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffff5-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffff5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

