---
title: PidTagAgingPeriod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360117"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="3ea91-103">PidTagAgingPeriod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea91-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="3ea91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ea91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ea91-105">アイテムがアーカイブされる前にアイテムがフォルダー内に残っている時間の長さを判断するために使用される時間単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3ea91-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3ea91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ea91-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="3ea91-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="3ea91-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3ea91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ea91-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="3ea91-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="3ea91-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3ea91-110">Property type:</span></span>  <br/> |<span data-ttu-id="3ea91-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3ea91-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3ea91-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3ea91-112">Area:</span></span>  <br/> |<span data-ttu-id="3ea91-113">その他</span><span class="sxs-lookup"><span data-stu-id="3ea91-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ea91-114">解説</span><span class="sxs-lookup"><span data-stu-id="3ea91-114">Remarks</span></span>

<span data-ttu-id="3ea91-115">アイテムがアーカイブされる前にそのアイテムがフォルダー内に残っている時間の長さは、 **PR_AGING_PERIOD**と**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** の2つのプロパティによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="3ea91-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="3ea91-116">**PR_AGING_GRANULARITY**は、この時間の長さを決定するときに、 **PR_AGING_PERIOD**が表される時間単位を表します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="3ea91-117">**PR_AGING_GRANULARITY**に使用できる値は、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3ea91-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="3ea91-118">**[名前]**</span><span class="sxs-lookup"><span data-stu-id="3ea91-118">**Name**</span></span>|<span data-ttu-id="3ea91-119">**[説明]**</span><span class="sxs-lookup"><span data-stu-id="3ea91-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ea91-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="3ea91-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="3ea91-121">**PR_AGING_PERIOD**は、月単位で定義されます。</span><span class="sxs-lookup"><span data-stu-id="3ea91-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="3ea91-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="3ea91-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="3ea91-123">**PR_AGING_PERIOD**は、週数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="3ea91-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="3ea91-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="3ea91-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="3ea91-125">**PR_AGING_PERIOD**は、日数で定義されています。</span><span class="sxs-lookup"><span data-stu-id="3ea91-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="3ea91-126">たとえば、アイテムがフォルダー内に2週間だけある場合に、フォルダーがアイテムをアーカイブすると、 **PR_AGING_GRANULARITY**は**AG_WEEKS**になり、 **PR_AGING_PERIOD**は2になります。</span><span class="sxs-lookup"><span data-stu-id="3ea91-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3ea91-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3ea91-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ea91-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3ea91-128">Protocol specifications</span></span>

<span data-ttu-id="3ea91-129">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea91-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea91-130">プロパティセットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="3ea91-131">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea91-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea91-132">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="3ea91-133">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea91-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea91-134">電子メールメッセージオブジェクトに対して許可されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ea91-135">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3ea91-135">Header files</span></span>

<span data-ttu-id="3ea91-136">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ea91-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ea91-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3ea91-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ea91-138">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3ea91-138">Mapitags.h</span></span>
  
> <span data-ttu-id="3ea91-139">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ea91-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ea91-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ea91-140">See also</span></span>



[<span data-ttu-id="3ea91-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea91-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ea91-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea91-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ea91-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3ea91-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ea91-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3ea91-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

