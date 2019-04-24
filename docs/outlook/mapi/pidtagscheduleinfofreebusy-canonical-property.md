---
title: PidTagScheduleInfoFreeBusy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusy
api_type:
- COM
ms.assetid: 54e65b23-7c5f-4ef3-9e32-329f5f461e1e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 018e3e907e6ff2250b4c0e5322af52b37d8e2817
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330073"
---
# <a name="pidtagscheduleinfofreebusy-canonical-property"></a><span data-ttu-id="45f50-103">PidTagScheduleInfoFreeBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45f50-103">PidTagScheduleInfoFreeBusy Canonical Property</span></span>

  
  
<span data-ttu-id="45f50-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45f50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45f50-105">古い情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45f50-105">Contains obsolete information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45f50-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="45f50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45f50-107">PR_SCHDINFO_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="45f50-107">PR_SCHDINFO_FREEBUSY</span></span>  <br/> |
|<span data-ttu-id="45f50-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="45f50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45f50-109">0x686c</span><span class="sxs-lookup"><span data-stu-id="45f50-109">0x686C</span></span>  <br/> |
|<span data-ttu-id="45f50-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="45f50-110">Data type:</span></span>  <br/> |<span data-ttu-id="45f50-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45f50-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45f50-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="45f50-112">Area:</span></span>  <br/> |<span data-ttu-id="45f50-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="45f50-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45f50-114">解説</span><span class="sxs-lookup"><span data-stu-id="45f50-114">Remarks</span></span>

<span data-ttu-id="45f50-115">このプロパティは設定しないでください。無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45f50-115">This property should not be set and must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45f50-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="45f50-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45f50-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="45f50-117">Protocol specifications</span></span>

<span data-ttu-id="45f50-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45f50-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45f50-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="45f50-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45f50-120">[[OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45f50-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45f50-121">ユーザーまたはリソースの空き時間情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="45f50-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45f50-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="45f50-122">Header files</span></span>

<span data-ttu-id="45f50-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45f50-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="45f50-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="45f50-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="45f50-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="45f50-125">Mapitags.h</span></span>
  
> <span data-ttu-id="45f50-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45f50-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45f50-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="45f50-127">See also</span></span>



[<span data-ttu-id="45f50-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="45f50-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45f50-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="45f50-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45f50-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="45f50-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45f50-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="45f50-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

