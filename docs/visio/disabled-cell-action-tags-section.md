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
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="e985c-103">[Disabled] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="e985c-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="e985c-104">図面ウィンドウに、アクション タグを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e985c-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e985c-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="e985c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="e985c-106">**値**</span><span class="sxs-lookup"><span data-stu-id="e985c-106">**Value**</span></span>|<span data-ttu-id="e985c-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="e985c-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e985c-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="e985c-108">TRUE</span></span>  <br/> | <span data-ttu-id="e985c-109">アクション タグは無効です。</span><span class="sxs-lookup"><span data-stu-id="e985c-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="e985c-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="e985c-110">FALSE</span></span>  <br/> | <span data-ttu-id="e985c-111">アクション タグは有効です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="e985c-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e985c-112">備考</span><span class="sxs-lookup"><span data-stu-id="e985c-112">Remarks</span></span>

<span data-ttu-id="e985c-113">アクション タグを無効にすると、有効にするまで表示されません。</span><span class="sxs-lookup"><span data-stu-id="e985c-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="e985c-114">取得する、[Disabled] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e985c-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e985c-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="e985c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="e985c-116">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="e985c-116">SmartTags.</span></span>  <span data-ttu-id="e985c-117">*名*です。無効になっているスマート タグです。</span><span class="sxs-lookup"><span data-stu-id="e985c-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="e985c-118">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="e985c-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="e985c-119">プログラムから、インデックスによって [Disabled] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e985c-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e985c-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e985c-120">Section index:</span></span>  <br/> |<span data-ttu-id="e985c-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="e985c-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="e985c-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e985c-122">Row index:</span></span>  <br/> |<span data-ttu-id="e985c-123">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="e985c-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e985c-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e985c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="e985c-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="e985c-125">**visSmartTagDisabled**</span></span> <br/> |
   

