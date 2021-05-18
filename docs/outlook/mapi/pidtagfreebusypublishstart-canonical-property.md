---
title: PidTagFreeBusyPublishStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishStart
api_type:
- HeaderDef
ms.assetid: d059f913-3d61-4bec-8215-5b07f0fba488
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3277ee9d0008954746890f8b33155f4e88f01766
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316164"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="8d829-103">PidTagFreeBusyPublishStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d829-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="8d829-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d829-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d829-105">発行範囲の開始時刻を格納します。</span><span class="sxs-lookup"><span data-stu-id="8d829-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d829-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8d829-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d829-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="8d829-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="8d829-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d829-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d829-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="8d829-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="8d829-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8d829-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d829-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d829-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d829-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8d829-112">Area:</span></span>  <br/> |<span data-ttu-id="8d829-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="8d829-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d829-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8d829-114">Remarks</span></span>

<span data-ttu-id="8d829-115">このプロパティの値は、協定世界時 (UTC) の 1601 年 1 月 1 日午前 0 時からの分数です。</span><span class="sxs-lookup"><span data-stu-id="8d829-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d829-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d829-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d829-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d829-117">Protocol specifications</span></span>

<span data-ttu-id="8d829-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d829-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d829-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="8d829-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d829-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d829-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d829-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="8d829-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d829-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d829-122">Header files</span></span>

<span data-ttu-id="8d829-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d829-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d829-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d829-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d829-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d829-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8d829-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8d829-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d829-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d829-127">See also</span></span>



[<span data-ttu-id="8d829-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d829-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d829-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d829-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d829-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8d829-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d829-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8d829-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

