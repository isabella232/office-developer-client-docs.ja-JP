---
title: PidTagScheduleInfoFreeBusymerged 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338718"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="3eb00-103">PidTagScheduleInfoFreeBusymerged 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb00-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="3eb00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3eb00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3eb00-105">空き時間情報の状態がビジー状態または OOF に設定されている時間を含みます。</span><span class="sxs-lookup"><span data-stu-id="3eb00-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3eb00-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3eb00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3eb00-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="3eb00-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="3eb00-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3eb00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3eb00-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="3eb00-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="3eb00-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3eb00-110">Data type:</span></span>  <br/> |<span data-ttu-id="3eb00-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3eb00-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3eb00-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3eb00-112">Area:</span></span>  <br/> |<span data-ttu-id="3eb00-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="3eb00-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb00-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3eb00-114">Remarks</span></span>

<span data-ttu-id="3eb00-115">空き時間情報の種類 (仮) のイベントは、このプロパティには含まれません。</span><span class="sxs-lookup"><span data-stu-id="3eb00-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="3eb00-116">このプロパティの形式、計算、および制限は **、PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) の形式、計算、および制限と同じですが、関連付けられた予定表で OOF またはビジーとマークされている予定を参照します。</span><span class="sxs-lookup"><span data-stu-id="3eb00-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3eb00-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3eb00-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3eb00-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3eb00-118">Protocol specifications</span></span>

<span data-ttu-id="3eb00-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb00-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb00-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3eb00-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3eb00-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb00-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb00-122">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="3eb00-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3eb00-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3eb00-123">Header files</span></span>

<span data-ttu-id="3eb00-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3eb00-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3eb00-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3eb00-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3eb00-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3eb00-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3eb00-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3eb00-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eb00-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3eb00-128">See also</span></span>



[<span data-ttu-id="3eb00-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb00-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3eb00-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eb00-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3eb00-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3eb00-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3eb00-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3eb00-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

