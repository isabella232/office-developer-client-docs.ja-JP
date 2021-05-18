---
title: PidTagagingGranularity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325586"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="f8936-103">PidTagagingGranularity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8936-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="f8936-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8936-105">アイテムがアーカイブされる前にアイテムがフォルダーに残る時間の長さを決定するために使用される時間の単位を表します。</span><span class="sxs-lookup"><span data-stu-id="f8936-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8936-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f8936-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8936-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="f8936-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="f8936-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f8936-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8936-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="f8936-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="f8936-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f8936-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8936-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f8936-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f8936-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f8936-112">Area:</span></span>  <br/> |<span data-ttu-id="f8936-113">その他</span><span class="sxs-lookup"><span data-stu-id="f8936-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8936-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f8936-114">Remarks</span></span>

<span data-ttu-id="f8936-115">指定できる値は **PR_AGING_GRANULARITY** のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f8936-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="f8936-116">**名前**</span><span class="sxs-lookup"><span data-stu-id="f8936-116">**Name**</span></span>|<span data-ttu-id="f8936-117">**値**</span><span class="sxs-lookup"><span data-stu-id="f8936-117">**Value**</span></span>|<span data-ttu-id="f8936-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8936-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8936-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="f8936-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="f8936-120">0</span><span class="sxs-lookup"><span data-stu-id="f8936-120">0</span></span>  <br/> |<span data-ttu-id="f8936-121">**PR_AGING_PERIOD** は月数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="f8936-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="f8936-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="f8936-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="f8936-123">1</span><span class="sxs-lookup"><span data-stu-id="f8936-123">1</span></span>  <br/> |<span data-ttu-id="f8936-124">**PR_AGING_PERIOD** 週数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="f8936-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="f8936-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="f8936-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="f8936-126">2</span><span class="sxs-lookup"><span data-stu-id="f8936-126">2</span></span>  <br/> |<span data-ttu-id="f8936-127">**PR_AGING_PERIOD** は日数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="f8936-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="f8936-128">アイテムがアーカイブされる前にアイテムがフォルダー内に残る時間の長さは、2 つのプロパティ[、PR_AGING_PERIODと](pidtagagingperiod-canonical-property.md)PR_AGING_GRANULARITY。 </span><span class="sxs-lookup"><span data-stu-id="f8936-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="f8936-129">**PR_AGING_PERIOD** は、アイテムがアーカイブされる前にフォルダーに残る時間単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="f8936-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8936-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f8936-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8936-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f8936-131">Protocol specifications</span></span>

<span data-ttu-id="f8936-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8936-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8936-133">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f8936-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8936-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8936-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8936-135">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8936-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="f8936-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8936-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8936-137">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8936-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8936-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f8936-138">Header files</span></span>

<span data-ttu-id="f8936-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8936-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8936-140">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8936-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8936-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8936-141">Mapitags.h</span></span>
  
> <span data-ttu-id="f8936-142">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f8936-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8936-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8936-143">See also</span></span>



[<span data-ttu-id="f8936-144">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f8936-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8936-145">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8936-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8936-146">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8936-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8936-147">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8936-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

