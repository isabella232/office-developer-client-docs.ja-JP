---
title: PidTagParentDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429503"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="1b54d-103">PidTagParentDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b54d-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="1b54d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b54d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b54d-105">検索中にメッセージが見つかったフォルダーの表示名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b54d-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b54d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1b54d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b54d-107">PR_PARENT_DISPLAY、PR_PARENT_DISPLAY_A、PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="1b54d-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="1b54d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1b54d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b54d-109">0x0e05</span><span class="sxs-lookup"><span data-stu-id="1b54d-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="1b54d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1b54d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b54d-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b54d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1b54d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1b54d-112">Area:</span></span>  <br/> |<span data-ttu-id="1b54d-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="1b54d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b54d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1b54d-114">Remarks</span></span>

<span data-ttu-id="1b54d-115">これらのプロパティは、オブジェクトには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="1b54d-115">These properties is not on any object.</span></span> <span data-ttu-id="1b54d-116">検索結果フォルダーの contents テーブルにのみ表示できます。</span><span class="sxs-lookup"><span data-stu-id="1b54d-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="1b54d-117">これらのプロパティと**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) プロパティは相互に関連していません。</span><span class="sxs-lookup"><span data-stu-id="1b54d-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="1b54d-118">これらは完全に異なるコンテキストに属します。</span><span class="sxs-lookup"><span data-stu-id="1b54d-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b54d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b54d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b54d-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1b54d-120">Header files</span></span>

<span data-ttu-id="1b54d-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b54d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b54d-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b54d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b54d-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1b54d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1b54d-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b54d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b54d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b54d-125">See also</span></span>



[<span data-ttu-id="1b54d-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b54d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b54d-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b54d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b54d-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b54d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b54d-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b54d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

