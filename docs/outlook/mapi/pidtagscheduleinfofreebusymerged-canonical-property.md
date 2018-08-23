---
title: PidTagScheduleInfoFreeBusyMerged 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b83a4acf30f498a0d17cc2c3c76f40c2c3c4b96
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582015"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="2a1b0-103">PidTagScheduleInfoFreeBusyMerged 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a1b0-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="2a1b0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a1b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a1b0-105">空き時間情報のステータスが設定されている時間が含まれていますをビジー状態または OOF。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a1b0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2a1b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a1b0-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="2a1b0-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="2a1b0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2a1b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a1b0-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="2a1b0-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="2a1b0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2a1b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a1b0-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a1b0-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a1b0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2a1b0-112">Area:</span></span>  <br/> |<span data-ttu-id="2a1b0-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="2a1b0-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a1b0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2a1b0-114">Remarks</span></span>

<span data-ttu-id="2a1b0-115">仮の予定の空き時間情報の種類のイベントは、このプロパティには含まれません。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="2a1b0-116">形式、計算およびこのプロパティの制限は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、不在時は、マークされているか、関連付けられているカレンダーの時間の予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a1b0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2a1b0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a1b0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2a1b0-118">Protocol specifications</span></span>

<span data-ttu-id="2a1b0-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1b0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1b0-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a1b0-121">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1b0-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1b0-122">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a1b0-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2a1b0-123">Header files</span></span>

<span data-ttu-id="2a1b0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a1b0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a1b0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a1b0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a1b0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="2a1b0-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a1b0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a1b0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a1b0-128">See also</span></span>



[<span data-ttu-id="2a1b0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a1b0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a1b0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a1b0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a1b0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a1b0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a1b0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2a1b0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

