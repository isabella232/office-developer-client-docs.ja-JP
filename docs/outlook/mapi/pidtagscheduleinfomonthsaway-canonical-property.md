---
title: PidTagScheduleInfoMonthsAway の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6301cd86a81dfbf38666b6fb3ea326bc1f801490
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803479"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="663c3-103">PidTagScheduleInfoMonthsAway の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="663c3-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="663c3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="663c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="663c3-105">不在時 (OOF) の種類のデータを空き/予約済みの空き時間情報メッセージ内に存在する月の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="663c3-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="663c3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="663c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="663c3-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="663c3-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="663c3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="663c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="663c3-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="663c3-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="663c3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="663c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="663c3-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="663c3-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="663c3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="663c3-112">Area:</span></span>  <br/> |<span data-ttu-id="663c3-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="663c3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="663c3-114">備考</span><span class="sxs-lookup"><span data-stu-id="663c3-114">Remarks</span></span>

<span data-ttu-id="663c3-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、外出中 (OOF) に関連付けられているとマークされている予定を参照してください。カレンダー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="663c3-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="663c3-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="663c3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="663c3-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="663c3-117">Protocol specifications</span></span>

<span data-ttu-id="663c3-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663c3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663c3-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="663c3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="663c3-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="663c3-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="663c3-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="663c3-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="663c3-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="663c3-122">Header files</span></span>

<span data-ttu-id="663c3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="663c3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="663c3-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="663c3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="663c3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="663c3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="663c3-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="663c3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="663c3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="663c3-127">See also</span></span>



[<span data-ttu-id="663c3-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="663c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="663c3-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="663c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="663c3-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="663c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="663c3-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="663c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

