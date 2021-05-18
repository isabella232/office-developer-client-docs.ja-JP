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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303410"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="27f30-103">PidTagScheduleInfoMonthsAway 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27f30-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="27f30-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27f30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27f30-105">空き時間情報 (OOF) の種類の空き時間情報データが空き時間情報メッセージに表示される月の一覧を格納します。</span><span class="sxs-lookup"><span data-stu-id="27f30-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27f30-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="27f30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27f30-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="27f30-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="27f30-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="27f30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27f30-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="27f30-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="27f30-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="27f30-110">Data type:</span></span>  <br/> |<span data-ttu-id="27f30-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="27f30-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="27f30-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="27f30-112">Area:</span></span>  <br/> |<span data-ttu-id="27f30-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="27f30-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27f30-114">注釈</span><span class="sxs-lookup"><span data-stu-id="27f30-114">Remarks</span></span>

<span data-ttu-id="27f30-115">このプロパティの形式、計算、および制約は **、PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative)](pidtagscheduleinfofreebusytentative-canonical-property.md)の形式、計算、および制約と同じですが、関連付けられた予定表オブジェクトの予定 (OOF) を参照します。</span><span class="sxs-lookup"><span data-stu-id="27f30-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27f30-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="27f30-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27f30-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="27f30-117">Protocol specifications</span></span>

<span data-ttu-id="27f30-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27f30-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27f30-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="27f30-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27f30-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27f30-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27f30-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="27f30-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27f30-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="27f30-122">Header files</span></span>

<span data-ttu-id="27f30-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27f30-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="27f30-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="27f30-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="27f30-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27f30-125">Mapitags.h</span></span>
  
> <span data-ttu-id="27f30-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="27f30-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27f30-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="27f30-127">See also</span></span>



[<span data-ttu-id="27f30-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="27f30-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27f30-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="27f30-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27f30-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="27f30-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27f30-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="27f30-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

