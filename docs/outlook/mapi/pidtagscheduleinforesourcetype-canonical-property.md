---
title: PidTagScheduleInfoResourceType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoResourceType
api_type:
- COM
ms.assetid: 9f253378-0a2d-47e3-82d3-8055b5f776dd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbcc149d6c5b5806a6514da4a3fb8e5615c9bc98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359767"
---
# <a name="pidtagscheduleinforesourcetype-canonical-property"></a><span data-ttu-id="a5c52-103">PidTagScheduleInfoResourceType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5c52-103">PidTagScheduleInfoResourceType Canonical Property</span></span>

  
  
<span data-ttu-id="a5c52-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5c52-105">ゼロ (0) に設定する必要がある値を含みます。</span><span class="sxs-lookup"><span data-stu-id="a5c52-105">Contains a value that must be set to zero (0).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c52-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a5c52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5c52-107">PR_SCHDINFO_RESOURCE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a5c52-107">PR_SCHDINFO_RESOURCE_TYPE</span></span>  <br/> |
|<span data-ttu-id="a5c52-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a5c52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5c52-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="a5c52-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="a5c52-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a5c52-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5c52-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5c52-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5c52-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a5c52-112">Area:</span></span>  <br/> |<span data-ttu-id="a5c52-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="a5c52-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5c52-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a5c52-114">Remarks</span></span>

<span data-ttu-id="a5c52-115">このプロパティは、受信時に送信および無視される場合、ゼロ (0) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5c52-115">This property must be set to zero (0) when sent and ignored upon receipt.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5c52-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a5c52-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5c52-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a5c52-117">Protocol specifications</span></span>

<span data-ttu-id="a5c52-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5c52-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5c52-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a5c52-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5c52-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5c52-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5c52-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="a5c52-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5c52-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a5c52-122">Header files</span></span>

<span data-ttu-id="a5c52-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5c52-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5c52-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5c52-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5c52-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5c52-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a5c52-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a5c52-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5c52-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5c52-127">See also</span></span>



[<span data-ttu-id="a5c52-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a5c52-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5c52-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5c52-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5c52-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a5c52-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5c52-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a5c52-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

