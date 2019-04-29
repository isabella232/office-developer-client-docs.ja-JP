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
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439668"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="0c1b1-103">[Disabled] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="0c1b1-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="0c1b1-104">図面ウィンドウに、アクション タグを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0c1b1-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="0c1b1-106">**値**</span><span class="sxs-lookup"><span data-stu-id="0c1b1-106">**Value**</span></span>|<span data-ttu-id="0c1b1-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="0c1b1-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0c1b1-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c1b1-108">TRUE</span></span>  <br/> | <span data-ttu-id="0c1b1-109">アクション タグは無効です。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="0c1b1-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="0c1b1-110">FALSE</span></span>  <br/> | <span data-ttu-id="0c1b1-111">アクション タグは有効です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c1b1-112">注釈</span><span class="sxs-lookup"><span data-stu-id="0c1b1-112">Remarks</span></span>

<span data-ttu-id="0c1b1-113">アクション タグを無効にすると、有効にするまで表示されません。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="0c1b1-114">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c1b1-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0c1b1-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0c1b1-116">タグ.</span><span class="sxs-lookup"><span data-stu-id="0c1b1-116">SmartTags.</span></span>  <span data-ttu-id="0c1b1-117">*名前*です。無効 (スマートタグ)</span><span class="sxs-lookup"><span data-stu-id="0c1b1-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="0c1b1-118">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0c1b1-119">プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c1b1-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c1b1-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-120">Section index:</span></span>  <br/> |<span data-ttu-id="0c1b1-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0c1b1-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0c1b1-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-122">Row index:</span></span>  <br/> |<span data-ttu-id="0c1b1-123">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0c1b1-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0c1b1-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c1b1-124">Cell index:</span></span>  <br/> |<span data-ttu-id="0c1b1-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="0c1b1-125">**visSmartTagDisabled**</span></span> <br/> |
   

