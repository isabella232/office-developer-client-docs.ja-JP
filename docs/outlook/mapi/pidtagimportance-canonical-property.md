---
title: PidTagImportance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802852"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="4f972-103">PidTagImportance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f972-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="4f972-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f972-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f972-105">メッセージの重要度のメッセージの送信者の意見を示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f972-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f972-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4f972-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f972-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="4f972-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="4f972-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4f972-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f972-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="4f972-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="4f972-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4f972-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f972-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f972-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f972-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4f972-112">Area:</span></span>  <br/> |<span data-ttu-id="4f972-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="4f972-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f972-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4f972-114">Remarks</span></span>

<span data-ttu-id="4f972-115">このプロパティは、 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) は混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="4f972-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="4f972-116">重要性は、優先順位は、順序や速度のメッセージがメッセージング システムのソフトウェアが送信することを示します。 ユーザーに値を示します。</span><span class="sxs-lookup"><span data-stu-id="4f972-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="4f972-117">高い優先度は、通常より高いコストを示します。</span><span class="sxs-lookup"><span data-stu-id="4f972-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="4f972-118">重要度が高く通常は、ユーザー インターフェイスで別のディスプレイに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4f972-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="4f972-119">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4f972-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="4f972-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="4f972-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="4f972-121">メッセージには重要度が低い。</span><span class="sxs-lookup"><span data-stu-id="4f972-121">The message has low importance.</span></span>
    
<span data-ttu-id="4f972-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="4f972-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="4f972-123">メッセージには重要度が高い。</span><span class="sxs-lookup"><span data-stu-id="4f972-123">The message has high importance.</span></span>
    
<span data-ttu-id="4f972-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="4f972-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="4f972-125">メッセージには、通常の重要性があります。</span><span class="sxs-lookup"><span data-stu-id="4f972-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4f972-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4f972-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f972-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4f972-127">Protocol specifications</span></span>

<span data-ttu-id="4f972-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f972-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f972-129">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f972-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f972-130">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f972-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f972-131">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4f972-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f972-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4f972-132">Header files</span></span>

<span data-ttu-id="4f972-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f972-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f972-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f972-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f972-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f972-135">Mapitags.h</span></span>
  
> <span data-ttu-id="4f972-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f972-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f972-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f972-137">See also</span></span>



[<span data-ttu-id="4f972-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f972-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f972-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f972-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f972-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f972-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f972-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f972-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

