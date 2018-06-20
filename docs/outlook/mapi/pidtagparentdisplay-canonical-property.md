---
title: PidTagParentDisplay の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803161"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="35a4c-103">PidTagParentDisplay の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35a4c-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="35a4c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35a4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35a4c-105">検索時にメッセージがあるフォルダーの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35a4c-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35a4c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="35a4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35a4c-107">PR_PARENT_DISPLAY、PR_PARENT_DISPLAY_A、PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="35a4c-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="35a4c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35a4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35a4c-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="35a4c-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="35a4c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="35a4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="35a4c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35a4c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35a4c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="35a4c-112">Area:</span></span>  <br/> |<span data-ttu-id="35a4c-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="35a4c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35a4c-114">備考</span><span class="sxs-lookup"><span data-stu-id="35a4c-114">Remarks</span></span>

<span data-ttu-id="35a4c-115">これらのプロパティは、任意のオブジェクトではありません。</span><span class="sxs-lookup"><span data-stu-id="35a4c-115">These properties is not on any object.</span></span> <span data-ttu-id="35a4c-116">のみ検索結果フォルダーの内容の表に表示されることができます。</span><span class="sxs-lookup"><span data-stu-id="35a4c-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="35a4c-117">これらのプロパティおよびプロパティの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) は、互いに関係ありません。</span><span class="sxs-lookup"><span data-stu-id="35a4c-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="35a4c-118">まったく異なるコンテキストに属しているとします。</span><span class="sxs-lookup"><span data-stu-id="35a4c-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35a4c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35a4c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35a4c-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="35a4c-120">Header files</span></span>

<span data-ttu-id="35a4c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35a4c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="35a4c-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35a4c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="35a4c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35a4c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="35a4c-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35a4c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35a4c-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="35a4c-125">See also</span></span>



[<span data-ttu-id="35a4c-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35a4c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35a4c-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="35a4c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35a4c-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="35a4c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35a4c-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="35a4c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

