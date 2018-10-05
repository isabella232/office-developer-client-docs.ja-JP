---
title: PidTagAgingGranularity 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390437"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="21b00-103">PidTagAgingGranularity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="21b00-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="21b00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21b00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21b00-105">アイテムをアーカイブする前に、アイテムがフォルダーに残って時間の長さを決定するために使用される時間の単位を表します。</span><span class="sxs-lookup"><span data-stu-id="21b00-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21b00-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="21b00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21b00-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="21b00-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="21b00-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="21b00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21b00-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="21b00-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="21b00-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="21b00-110">Data type:</span></span>  <br/> |<span data-ttu-id="21b00-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="21b00-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="21b00-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="21b00-112">Area:</span></span>  <br/> |<span data-ttu-id="21b00-113">その他</span><span class="sxs-lookup"><span data-stu-id="21b00-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21b00-114">備考</span><span class="sxs-lookup"><span data-stu-id="21b00-114">Remarks</span></span>

<span data-ttu-id="21b00-115">**PR_AGING_GRANULARITY**の有効な値には、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="21b00-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="21b00-116">**名前**</span><span class="sxs-lookup"><span data-stu-id="21b00-116">**Name**</span></span>|<span data-ttu-id="21b00-117">**値**</span><span class="sxs-lookup"><span data-stu-id="21b00-117">**Value**</span></span>|<span data-ttu-id="21b00-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="21b00-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21b00-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="21b00-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="21b00-120">0</span><span class="sxs-lookup"><span data-stu-id="21b00-120">0</span></span>  <br/> |<span data-ttu-id="21b00-121">**PR_AGING_PERIOD**は、月の数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="21b00-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="21b00-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="21b00-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="21b00-123">1</span><span class="sxs-lookup"><span data-stu-id="21b00-123">1</span></span>  <br/> |<span data-ttu-id="21b00-124">**PR_AGING_PERIOD**は、週数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="21b00-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="21b00-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="21b00-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="21b00-126">2</span><span class="sxs-lookup"><span data-stu-id="21b00-126">2</span></span>  <br/> |<span data-ttu-id="21b00-127">**PR_AGING_PERIOD**は、日数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="21b00-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="21b00-128">アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さは、 [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)と**PR_AGING_GRANULARITY**の 2 つのプロパティによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="21b00-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="21b00-129">**PR_AGING_PERIOD**では、アーカイブする前に、アイテムがフォルダーに残っている時間の単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="21b00-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="21b00-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="21b00-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21b00-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="21b00-131">Protocol specifications</span></span>

<span data-ttu-id="21b00-132">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21b00-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21b00-133">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="21b00-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21b00-134">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21b00-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21b00-135">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="21b00-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="21b00-136">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21b00-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21b00-137">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="21b00-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21b00-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="21b00-138">Header files</span></span>

<span data-ttu-id="21b00-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21b00-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="21b00-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="21b00-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="21b00-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21b00-141">Mapitags.h</span></span>
  
> <span data-ttu-id="21b00-142">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21b00-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21b00-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="21b00-143">See also</span></span>



[<span data-ttu-id="21b00-144">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21b00-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21b00-145">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21b00-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21b00-146">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21b00-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21b00-147">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21b00-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

