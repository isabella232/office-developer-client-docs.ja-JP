---
title: PidTagFreeBusyPublishEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316185"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="e06fc-103">PidTagFreeBusyPublishEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e06fc-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="e06fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e06fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e06fc-105">公開範囲の終了時刻を含みます。</span><span class="sxs-lookup"><span data-stu-id="e06fc-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e06fc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e06fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e06fc-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="e06fc-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="e06fc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e06fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e06fc-109">0x684 8</span><span class="sxs-lookup"><span data-stu-id="e06fc-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="e06fc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e06fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="e06fc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e06fc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e06fc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e06fc-112">Area:</span></span>  <br/> |<span data-ttu-id="e06fc-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="e06fc-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e06fc-114">解説</span><span class="sxs-lookup"><span data-stu-id="e06fc-114">Remarks</span></span>

<span data-ttu-id="e06fc-115">このプロパティの値は、 **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) の値を発行範囲の開始日に追加することによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="e06fc-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="e06fc-116">この値は、世界協定時刻 (UTC) の1601年1月1日午前0時からの経過時間 (分単位) として表されます。</span><span class="sxs-lookup"><span data-stu-id="e06fc-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e06fc-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e06fc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e06fc-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e06fc-118">Protocol specifications</span></span>

<span data-ttu-id="e06fc-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e06fc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e06fc-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e06fc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e06fc-121">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e06fc-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e06fc-122">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="e06fc-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e06fc-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e06fc-123">Header files</span></span>

<span data-ttu-id="e06fc-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e06fc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e06fc-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e06fc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e06fc-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e06fc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e06fc-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e06fc-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e06fc-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e06fc-128">See also</span></span>



[<span data-ttu-id="e06fc-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e06fc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e06fc-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e06fc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e06fc-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e06fc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e06fc-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e06fc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

