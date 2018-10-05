---
title: PidTagScheduleInfoMonthsMerged 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383822"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="d2132-103">PidTagScheduleInfoMonthsMerged 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2132-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="d2132-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2132-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2132-105">メッセージ タイプを使用中の空き時間情報データや、不在 (時 OOF) の月の空き時間メッセージにリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2132-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2132-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d2132-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2132-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="d2132-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="d2132-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d2132-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2132-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="d2132-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="d2132-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d2132-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2132-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d2132-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d2132-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d2132-112">Area:</span></span>  <br/> |<span data-ttu-id="d2132-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="d2132-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2132-114">備考</span><span class="sxs-lookup"><span data-stu-id="d2132-114">Remarks</span></span>

<span data-ttu-id="d2132-115">仮の予定の空き時間情報の種類のイベントは、このプロパティには含まれません。</span><span class="sxs-lookup"><span data-stu-id="d2132-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="d2132-116">構文と形式およびこのプロパティの制約は、 **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの不在時または取り込み中にマークされている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2132-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2132-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d2132-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2132-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d2132-118">Protocol specifications</span></span>

<span data-ttu-id="d2132-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2132-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2132-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2132-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2132-121">[[MS OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2132-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2132-122">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="d2132-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2132-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d2132-123">Header files</span></span>

<span data-ttu-id="d2132-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2132-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2132-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2132-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2132-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2132-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d2132-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2132-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2132-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2132-128">See also</span></span>



[<span data-ttu-id="d2132-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2132-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2132-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2132-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2132-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2132-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2132-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2132-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

