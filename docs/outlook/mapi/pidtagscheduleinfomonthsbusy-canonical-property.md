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
ms.openlocfilehash: 7723897c6d249bbb53a0de5aa68ad8d1bc79830f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563728"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="bcbef-103">PidTagScheduleInfoMonthsBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcbef-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="bcbef-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcbef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcbef-105">ビジー状態の種類のデータを空き/予約済みの空き時間情報メッセージ内に存在する月が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bcbef-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcbef-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bcbef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcbef-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="bcbef-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="bcbef-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bcbef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcbef-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="bcbef-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="bcbef-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bcbef-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcbef-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="bcbef-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="bcbef-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bcbef-112">Area:</span></span>  <br/> |<span data-ttu-id="bcbef-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="bcbef-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcbef-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bcbef-114">Remarks</span></span>

<span data-ttu-id="bcbef-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの使用中としてマークされている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcbef-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcbef-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bcbef-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcbef-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bcbef-117">Protocol specifications</span></span>

<span data-ttu-id="bcbef-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcbef-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcbef-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcbef-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcbef-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcbef-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcbef-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="bcbef-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcbef-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bcbef-122">Header files</span></span>

<span data-ttu-id="bcbef-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcbef-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcbef-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcbef-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcbef-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcbef-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bcbef-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bcbef-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcbef-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcbef-127">See also</span></span>



[<span data-ttu-id="bcbef-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcbef-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcbef-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcbef-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcbef-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bcbef-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcbef-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bcbef-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

