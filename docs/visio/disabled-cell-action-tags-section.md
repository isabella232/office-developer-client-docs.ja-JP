---
title: '[Disabled] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: 図面ウィンドウに、アクション タグを表示するかどうかを示します。
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805226"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="ccc8c-103">[Disabled] セル ([操作タグ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ccc8c-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="ccc8c-104">図面ウィンドウに、アクション タグを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ccc8c-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="ccc8c-106">**値**</span><span class="sxs-lookup"><span data-stu-id="ccc8c-106">**Value**</span></span>|<span data-ttu-id="ccc8c-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="ccc8c-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ccc8c-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="ccc8c-108">TRUE</span></span>  <br/> | <span data-ttu-id="ccc8c-109">アクション タグは無効です。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="ccc8c-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="ccc8c-110">FALSE</span></span>  <br/> | <span data-ttu-id="ccc8c-111">アクション タグは有効です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccc8c-112">備考</span><span class="sxs-lookup"><span data-stu-id="ccc8c-112">Remarks</span></span>

<span data-ttu-id="ccc8c-113">アクション タグを無効にすると、有効にするまで表示されません。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="ccc8c-114">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccc8c-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="ccc8c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ccc8c-116">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-116">SmartTags.</span></span>  <span data-ttu-id="ccc8c-117">*名*です。無効になっているスマート タグです。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="ccc8c-118">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="ccc8c-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="ccc8c-119">プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ccc8c-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccc8c-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ccc8c-120">Section index:</span></span>  <br/> |<span data-ttu-id="ccc8c-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="ccc8c-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="ccc8c-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ccc8c-122">Row index:</span></span>  <br/> |<span data-ttu-id="ccc8c-123">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="ccc8c-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ccc8c-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ccc8c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ccc8c-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="ccc8c-125">**visSmartTagDisabled**</span></span> <br/> |
   

