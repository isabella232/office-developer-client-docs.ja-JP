---
title: '[Snap] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: レイヤーに割り当てられた図形に他の図形をスナップできるかどうかを指定します。レイヤーに割り当てられた図形に他の図形をスナップすることはできますが、他の図形にレイヤーに割り当てられた図形をスナップすることはできません。
ms.openlocfilehash: 7fc684afb67d0454ea5907c08f4f7644d97c7f74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806514"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="be3e6-104">[Snap] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="be3e6-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="be3e6-p102">レイヤーに割り当てられた図形に他の図形をスナップできるかどうかを指定します。レイヤーに割り当てられた図形に他の図形をスナップすることはできますが、他の図形にレイヤーに割り当てられた図形をスナップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="be3e6-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="be3e6-107">**値**</span><span class="sxs-lookup"><span data-stu-id="be3e6-107">**Value**</span></span>|<span data-ttu-id="be3e6-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="be3e6-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be3e6-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="be3e6-109">TRUE</span></span>  <br/> |<span data-ttu-id="be3e6-110">レイヤー上の図形に他の図形をスナップできます。</span><span class="sxs-lookup"><span data-stu-id="be3e6-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="be3e6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3e6-111">FALSE</span></span>  <br/> |<span data-ttu-id="be3e6-112">レイヤー上の図形に他の図形をスナップできません。</span><span class="sxs-lookup"><span data-stu-id="be3e6-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be3e6-113">注釈</span><span class="sxs-lookup"><span data-stu-id="be3e6-113">Remarks</span></span>

<span data-ttu-id="be3e6-114">**[レイヤー プロパティ**] ダイアログ ボックスで、[**スナップ**] オプションを使用してこのセルの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="be3e6-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="be3e6-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって snap] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="be3e6-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be3e6-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="be3e6-116">Cell name:</span></span>  <br/> |<span data-ttu-id="be3e6-117">Layers.Snap [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="be3e6-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="be3e6-118">プログラムから、インデックスによって [snap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="be3e6-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be3e6-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="be3e6-119">Section index:</span></span>  <br/> |<span data-ttu-id="be3e6-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="be3e6-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="be3e6-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="be3e6-121">Row index:</span></span>  <br/> |<span data-ttu-id="be3e6-122">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="be3e6-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="be3e6-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="be3e6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="be3e6-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="be3e6-124">**visLayerSnap**</span></span> <br/> |
   

