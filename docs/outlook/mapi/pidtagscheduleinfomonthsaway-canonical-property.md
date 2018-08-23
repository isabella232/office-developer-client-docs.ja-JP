---
title: PidTagScheduleInfoMonthsAway 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8caf16bad26eef10d7686d66c5a17320de5e3bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588105"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="1be60-103">PidTagScheduleInfoMonthsAway 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1be60-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="1be60-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1be60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1be60-105">不在時 (OOF) の種類のデータを空き/予約済みの空き時間情報メッセージ内に存在する月の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1be60-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1be60-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1be60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1be60-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="1be60-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="1be60-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1be60-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1be60-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="1be60-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="1be60-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1be60-110">Data type:</span></span>  <br/> |<span data-ttu-id="1be60-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="1be60-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="1be60-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1be60-112">Area:</span></span>  <br/> |<span data-ttu-id="1be60-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="1be60-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1be60-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1be60-114">Remarks</span></span>

<span data-ttu-id="1be60-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、外出中 (OOF) に関連付けられているとマークされている予定を参照してください。カレンダー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="1be60-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1be60-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1be60-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1be60-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1be60-117">Protocol specifications</span></span>

<span data-ttu-id="1be60-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1be60-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1be60-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1be60-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1be60-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1be60-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1be60-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="1be60-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1be60-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1be60-122">Header files</span></span>

<span data-ttu-id="1be60-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1be60-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1be60-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1be60-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1be60-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1be60-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1be60-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1be60-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1be60-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1be60-127">See also</span></span>



[<span data-ttu-id="1be60-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1be60-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1be60-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1be60-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1be60-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1be60-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1be60-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1be60-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

