---
title: PidTagScheduleInfoFreeBusyMerged の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0e1fbab53589a4ebf8681d5fe738ad625d31c18f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803468"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="c0fc6-103">PidTagScheduleInfoFreeBusyMerged の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c0fc6-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="c0fc6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0fc6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0fc6-105">空き時間情報のステータスが設定されている時間が含まれていますをビジー状態または OOF。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0fc6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0fc6-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="c0fc6-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="c0fc6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c0fc6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0fc6-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="c0fc6-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="c0fc6-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0fc6-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c0fc6-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c0fc6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c0fc6-112">Area:</span></span>  <br/> |<span data-ttu-id="c0fc6-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="c0fc6-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0fc6-114">備考</span><span class="sxs-lookup"><span data-stu-id="c0fc6-114">Remarks</span></span>

<span data-ttu-id="c0fc6-115">仮の予定の空き時間情報の種類のイベントは、このプロパティには含まれません。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="c0fc6-116">形式、計算およびこのプロパティの制限は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、不在時は、マークされているか、関連付けられているカレンダーの時間の予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c0fc6-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c0fc6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0fc6-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c0fc6-118">Protocol specifications</span></span>

<span data-ttu-id="c0fc6-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0fc6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0fc6-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0fc6-121">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0fc6-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0fc6-122">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0fc6-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c0fc6-123">Header files</span></span>

<span data-ttu-id="c0fc6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0fc6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0fc6-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0fc6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0fc6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c0fc6-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0fc6-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0fc6-128">See also</span></span>



[<span data-ttu-id="c0fc6-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0fc6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0fc6-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0fc6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0fc6-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c0fc6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0fc6-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c0fc6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

