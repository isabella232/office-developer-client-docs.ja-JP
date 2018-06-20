---
title: PidTagAgingPeriod の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1fd1b06bbaa10c2d7c71ee4c161fd6a980da1865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802436"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="e1867-103">PidTagAgingPeriod の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e1867-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="e1867-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1867-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1867-105">アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さを決定するために使用する時間単位数を表します。</span><span class="sxs-lookup"><span data-stu-id="e1867-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e1867-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e1867-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1867-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="e1867-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="e1867-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e1867-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1867-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="e1867-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="e1867-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="e1867-110">Property type:</span></span>  <br/> |<span data-ttu-id="e1867-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1867-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1867-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e1867-112">Area:</span></span>  <br/> |<span data-ttu-id="e1867-113">その他</span><span class="sxs-lookup"><span data-stu-id="e1867-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1867-114">備考</span><span class="sxs-lookup"><span data-stu-id="e1867-114">Remarks</span></span>

<span data-ttu-id="e1867-115">アイテムをアーカイブする前に、アイテムがフォルダーに残っている時間の長さは、 **PR_AGING_PERIOD**と**[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** の 2 つのプロパティによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="e1867-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="e1867-116">**PR_AGING_GRANULARITY**は、 **PR_AGING_PERIOD**が表現する、この期間を決定する際に時間の単位を表します。</span><span class="sxs-lookup"><span data-stu-id="e1867-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="e1867-117">**PR_AGING_GRANULARITY**の有効な値には、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e1867-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="e1867-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="e1867-118">**Name**</span></span>|<span data-ttu-id="e1867-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e1867-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1867-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="e1867-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="e1867-121">**PR_AGING_PERIOD**は、月の数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e1867-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="e1867-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="e1867-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="e1867-123">**PR_AGING_PERIOD**は、週数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e1867-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="e1867-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="e1867-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="e1867-125">**PR_AGING_PERIOD**は、日数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e1867-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="e1867-126">たとえば、アイテムのフォルダーに、2 週間後で**PR_AGING_GRANULARITY**された後にのみアイテムがフォルダーのアーカイブの場合**AG_WEEKS**と**PR_AGING_PERIOD**は 2 です。</span><span class="sxs-lookup"><span data-stu-id="e1867-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1867-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e1867-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1867-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e1867-128">Protocol specifications</span></span>

<span data-ttu-id="e1867-129">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1867-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1867-130">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e1867-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="e1867-131">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1867-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1867-132">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="e1867-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="e1867-133">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1867-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1867-134">プロパティおよび電子メール メッセージのオブジェクトに対して許可される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1867-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1867-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e1867-135">Header files</span></span>

<span data-ttu-id="e1867-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1867-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1867-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e1867-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1867-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1867-138">Mapitags.h</span></span>
  
> <span data-ttu-id="e1867-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1867-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1867-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1867-140">See also</span></span>



[<span data-ttu-id="e1867-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1867-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1867-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1867-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1867-143">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e1867-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1867-144">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e1867-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

