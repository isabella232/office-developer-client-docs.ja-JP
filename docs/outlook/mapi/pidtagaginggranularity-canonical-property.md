---
title: PidTagAgingGranularity の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 09a79a68d7619ded9edf3ec4ac67733bdec1e32c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802448"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="56520-103">PidTagAgingGranularity の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="56520-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="56520-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56520-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56520-105">アイテムをアーカイブする前に、アイテムがフォルダーに残って時間の長さを決定するために使用される時間の単位を表します。</span><span class="sxs-lookup"><span data-stu-id="56520-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56520-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="56520-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56520-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="56520-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="56520-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="56520-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56520-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="56520-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="56520-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="56520-110">Data type:</span></span>  <br/> |<span data-ttu-id="56520-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="56520-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="56520-112">領域:</span><span class="sxs-lookup"><span data-stu-id="56520-112">Area:</span></span>  <br/> |<span data-ttu-id="56520-113">その他</span><span class="sxs-lookup"><span data-stu-id="56520-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56520-114">備考</span><span class="sxs-lookup"><span data-stu-id="56520-114">Remarks</span></span>

<span data-ttu-id="56520-115">**PR_AGING_GRANULARITY**の有効な値には、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="56520-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="56520-116">**名前**</span><span class="sxs-lookup"><span data-stu-id="56520-116">**Name**</span></span>|<span data-ttu-id="56520-117">**値**</span><span class="sxs-lookup"><span data-stu-id="56520-117">**Value**</span></span>|<span data-ttu-id="56520-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="56520-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56520-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="56520-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="56520-120">0</span><span class="sxs-lookup"><span data-stu-id="56520-120">0</span></span>  <br/> |<span data-ttu-id="56520-121">**PR_AGING_PERIOD**は、月の数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="56520-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="56520-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="56520-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="56520-123">1</span><span class="sxs-lookup"><span data-stu-id="56520-123">1</span></span>  <br/> |<span data-ttu-id="56520-124">**PR_AGING_PERIOD**は、週数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="56520-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="56520-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="56520-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="56520-126">2</span><span class="sxs-lookup"><span data-stu-id="56520-126">2</span></span>  <br/> |<span data-ttu-id="56520-127">**PR_AGING_PERIOD**は、日数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="56520-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="56520-128">アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さは、 [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)と**PR_AGING_GRANULARITY**の 2 つのプロパティによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="56520-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="56520-129">**PR_AGING_PERIOD**では、アーカイブする前に、アイテムがフォルダーに残っている時間の単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="56520-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56520-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="56520-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56520-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="56520-131">Protocol specifications</span></span>

<span data-ttu-id="56520-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56520-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56520-133">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="56520-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56520-134">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56520-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56520-135">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="56520-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="56520-136">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56520-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56520-137">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="56520-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56520-138">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="56520-138">Header files</span></span>

<span data-ttu-id="56520-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56520-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="56520-140">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="56520-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="56520-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56520-141">Mapitags.h</span></span>
  
> <span data-ttu-id="56520-142">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56520-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56520-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="56520-143">See also</span></span>



[<span data-ttu-id="56520-144">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="56520-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56520-145">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="56520-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56520-146">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="56520-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56520-147">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="56520-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

