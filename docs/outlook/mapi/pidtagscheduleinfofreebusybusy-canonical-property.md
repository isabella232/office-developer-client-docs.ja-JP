---
title: PidTagScheduleInfoFreeBusyBusy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338655"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="4a54a-103">PidTagScheduleInfoFreeBusyBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a54a-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="4a54a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a54a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a54a-105">状態が "取り込み中" である時間のブロックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4a54a-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a54a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a54a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a54a-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="4a54a-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="4a54a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4a54a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a54a-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="4a54a-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="4a54a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a54a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a54a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a54a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a54a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4a54a-112">Area:</span></span>  <br/> |<span data-ttu-id="4a54a-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="4a54a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a54a-114">解説</span><span class="sxs-lookup"><span data-stu-id="4a54a-114">Remarks</span></span>

<span data-ttu-id="4a54a-115">このプロパティの書式、計算、および制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) の場合と同じですが、関連付けられている予定表オブジェクトでビジー状態としてマークされている予定を参照します。</span><span class="sxs-lookup"><span data-stu-id="4a54a-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a54a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a54a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a54a-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a54a-117">Protocol specifications</span></span>

<span data-ttu-id="4a54a-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a54a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a54a-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a54a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a54a-120">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a54a-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a54a-121">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="4a54a-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a54a-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4a54a-122">Header files</span></span>

<span data-ttu-id="4a54a-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a54a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a54a-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a54a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a54a-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4a54a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4a54a-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a54a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a54a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a54a-127">See also</span></span>



[<span data-ttu-id="4a54a-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4a54a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a54a-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a54a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a54a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a54a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a54a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a54a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

