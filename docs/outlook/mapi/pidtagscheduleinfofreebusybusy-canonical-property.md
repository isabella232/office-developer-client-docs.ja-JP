---
title: PidTagScheduleInfoFreeBusyBusy の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e0c59b569f4f01584fd65a7c3e13d6daac69d8a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803471"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="76ee0-103">PidTagScheduleInfoFreeBusyBusy の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="76ee0-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="76ee0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76ee0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76ee0-105">状態がビジー状態である時間のブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76ee0-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76ee0-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="76ee0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76ee0-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="76ee0-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="76ee0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="76ee0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76ee0-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="76ee0-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="76ee0-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="76ee0-110">Data type:</span></span>  <br/> |<span data-ttu-id="76ee0-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="76ee0-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="76ee0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="76ee0-112">Area:</span></span>  <br/> |<span data-ttu-id="76ee0-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="76ee0-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76ee0-114">備考</span><span class="sxs-lookup"><span data-stu-id="76ee0-114">Remarks</span></span>

<span data-ttu-id="76ee0-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの使用中としてマークされている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76ee0-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76ee0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76ee0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76ee0-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="76ee0-117">Protocol specifications</span></span>

<span data-ttu-id="76ee0-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ee0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ee0-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="76ee0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76ee0-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ee0-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ee0-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="76ee0-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76ee0-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76ee0-122">Header files</span></span>

<span data-ttu-id="76ee0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76ee0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="76ee0-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76ee0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="76ee0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76ee0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="76ee0-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76ee0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76ee0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="76ee0-127">See also</span></span>



[<span data-ttu-id="76ee0-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ee0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76ee0-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="76ee0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76ee0-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="76ee0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76ee0-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="76ee0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

