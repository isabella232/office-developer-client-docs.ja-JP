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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ccee84b8e548ee656366d07c81927a701e9b70f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802816"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="69b33-103">PidTagFreeBusyPublishStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69b33-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="69b33-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69b33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69b33-105">公開の範囲の開始時刻が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69b33-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69b33-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="69b33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69b33-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="69b33-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="69b33-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="69b33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69b33-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="69b33-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="69b33-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="69b33-110">Data type:</span></span>  <br/> |<span data-ttu-id="69b33-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69b33-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69b33-112">領域:</span><span class="sxs-lookup"><span data-stu-id="69b33-112">Area:</span></span>  <br/> |<span data-ttu-id="69b33-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="69b33-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69b33-114">注釈</span><span class="sxs-lookup"><span data-stu-id="69b33-114">Remarks</span></span>

<span data-ttu-id="69b33-115">このプロパティの値は、1601 年 1 月 1 日世界協定時刻 (UTC) で、午前 0 時以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="69b33-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69b33-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69b33-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69b33-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="69b33-117">Protocol specifications</span></span>

<span data-ttu-id="69b33-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69b33-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69b33-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="69b33-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69b33-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69b33-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69b33-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="69b33-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69b33-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="69b33-122">Header files</span></span>

<span data-ttu-id="69b33-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69b33-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="69b33-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69b33-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="69b33-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69b33-125">Mapitags.h</span></span>
  
> <span data-ttu-id="69b33-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69b33-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69b33-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="69b33-127">See also</span></span>



[<span data-ttu-id="69b33-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69b33-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69b33-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69b33-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69b33-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69b33-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69b33-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69b33-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

