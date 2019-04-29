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
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434845"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="9c310-104">[Snap] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="9c310-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="9c310-p102">レイヤーに割り当てられた図形に他の図形をスナップできるかどうかを指定します。レイヤーに割り当てられた図形に他の図形をスナップすることはできますが、他の図形にレイヤーに割り当てられた図形をスナップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9c310-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="9c310-107">**値**</span><span class="sxs-lookup"><span data-stu-id="9c310-107">**Value**</span></span>|<span data-ttu-id="9c310-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c310-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c310-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="9c310-109">TRUE</span></span>  <br/> |<span data-ttu-id="9c310-110">レイヤー上の図形に他の図形をスナップできます。</span><span class="sxs-lookup"><span data-stu-id="9c310-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="9c310-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="9c310-111">FALSE</span></span>  <br/> |<span data-ttu-id="9c310-112">レイヤー上の図形に他の図形をスナップできません。</span><span class="sxs-lookup"><span data-stu-id="9c310-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c310-113">注釈</span><span class="sxs-lookup"><span data-stu-id="9c310-113">Remarks</span></span>

<span data-ttu-id="9c310-114">このセルの値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**スナップ**] オプションを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="9c310-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="9c310-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Snap] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c310-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c310-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="9c310-116">Cell name:</span></span>  <br/> |<span data-ttu-id="9c310-117">階層. スナップ [ *i* ] = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="9c310-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9c310-118">プログラムから、インデックスによって [Snap] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c310-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c310-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c310-119">Section index:</span></span>  <br/> |<span data-ttu-id="9c310-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="9c310-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="9c310-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c310-121">Row index:</span></span>  <br/> |<span data-ttu-id="9c310-122">**visRowLayer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="9c310-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9c310-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c310-123">Cell index:</span></span>  <br/> |<span data-ttu-id="9c310-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="9c310-124">**visLayerSnap**</span></span> <br/> |
   

