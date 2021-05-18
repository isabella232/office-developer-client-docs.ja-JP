---
title: '[Visible] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: レイヤーに属している図形が図面ページに表示されるかどうかを指定します。
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405451"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="58abc-103">[Visible] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="58abc-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="58abc-104">レイヤーに属している図形が図面ページに表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="58abc-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="58abc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="58abc-105">**Value**</span></span>|<span data-ttu-id="58abc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="58abc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58abc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="58abc-107">TRUE</span></span>  <br/> |<span data-ttu-id="58abc-108">図形は表示されます。</span><span class="sxs-lookup"><span data-stu-id="58abc-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="58abc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="58abc-109">FALSE</span></span>  <br/> |<span data-ttu-id="58abc-110">図形は表示されません。</span><span class="sxs-lookup"><span data-stu-id="58abc-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58abc-111">注釈</span><span class="sxs-lookup"><span data-stu-id="58abc-111">Remarks</span></span>

<span data-ttu-id="58abc-112">このセルは、[レイヤープロパティ] ダイアログ ボックスの [表示]オプションに対応します([ホーム] タブの [編集] グループで、[レイヤー] をクリックし、[レイヤー プロパティ] を **クリックします**)。 </span><span class="sxs-lookup"><span data-stu-id="58abc-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="58abc-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Visible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="58abc-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58abc-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="58abc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="58abc-115">Layers.Visible[ *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="58abc-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="58abc-116">プログラムから、インデックスによって [Visible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="58abc-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58abc-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="58abc-117">Section index:</span></span>  <br/> |<span data-ttu-id="58abc-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="58abc-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="58abc-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="58abc-119">Row index:</span></span>  <br/> |<span data-ttu-id="58abc-120">**visRowLayer**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="58abc-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="58abc-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="58abc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="58abc-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="58abc-122">**visLayerVisible**</span></span> <br/> |
   

