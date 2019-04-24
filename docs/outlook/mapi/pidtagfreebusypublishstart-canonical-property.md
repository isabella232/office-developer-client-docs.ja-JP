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
ms.openlocfilehash: 3277ee9d0008954746890f8b33155f4e88f01766
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316164"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="359d9-103">PidTagFreeBusyPublishStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="359d9-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="359d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="359d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="359d9-105">公開範囲の開始時刻を格納します。</span><span class="sxs-lookup"><span data-stu-id="359d9-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="359d9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="359d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="359d9-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="359d9-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="359d9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="359d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="359d9-109">0x684 7</span><span class="sxs-lookup"><span data-stu-id="359d9-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="359d9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="359d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="359d9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="359d9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="359d9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="359d9-112">Area:</span></span>  <br/> |<span data-ttu-id="359d9-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="359d9-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="359d9-114">解説</span><span class="sxs-lookup"><span data-stu-id="359d9-114">Remarks</span></span>

<span data-ttu-id="359d9-115">このプロパティの値は、世界協定時刻 (UTC) の1601年1月1日午前0時からの経過時間 (分単位) です。</span><span class="sxs-lookup"><span data-stu-id="359d9-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="359d9-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="359d9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="359d9-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="359d9-117">Protocol specifications</span></span>

<span data-ttu-id="359d9-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="359d9-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="359d9-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="359d9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="359d9-120">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="359d9-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="359d9-121">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="359d9-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="359d9-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="359d9-122">Header files</span></span>

<span data-ttu-id="359d9-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="359d9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="359d9-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="359d9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="359d9-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="359d9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="359d9-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="359d9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="359d9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="359d9-127">See also</span></span>



[<span data-ttu-id="359d9-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="359d9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="359d9-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="359d9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="359d9-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="359d9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="359d9-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="359d9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

