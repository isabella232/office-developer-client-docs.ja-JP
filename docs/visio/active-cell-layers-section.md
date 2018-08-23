---
title: '[Active] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804758"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="6e0a9-104">[Active] セル ([レイヤー] セクション)</span><span class="sxs-lookup"><span data-stu-id="6e0a9-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="6e0a9-p102">レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6e0a9-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="6e0a9-107">**値**</span><span class="sxs-lookup"><span data-stu-id="6e0a9-107">**Value**</span></span>|<span data-ttu-id="6e0a9-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="6e0a9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e0a9-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6e0a9-109">TRUE</span></span>  <br/> |<span data-ttu-id="6e0a9-110">
          レイヤーはアクティブです。
</span><span class="sxs-lookup"><span data-stu-id="6e0a9-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="6e0a9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6e0a9-111">FALSE</span></span>  <br/> |<span data-ttu-id="6e0a9-112">
          レイヤーはアクティブではありません。
</span><span class="sxs-lookup"><span data-stu-id="6e0a9-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e0a9-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6e0a9-113">Remarks</span></span>

<span data-ttu-id="6e0a9-114">このセルの値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**アクティブ**] の設定に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="6e0a9-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="6e0a9-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Active] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6e0a9-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e0a9-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="6e0a9-116">Cell name:</span></span>  <br/> |<span data-ttu-id="6e0a9-117">Layers.Active [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6e0a9-118">プログラムから、インデックスによって [Active] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e0a9-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e0a9-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e0a9-119">Section index:</span></span>  <br/> |<span data-ttu-id="6e0a9-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="6e0a9-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="6e0a9-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e0a9-121">Row index:</span></span>  <br/> |<span data-ttu-id="6e0a9-122">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="6e0a9-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6e0a9-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6e0a9-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6e0a9-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="6e0a9-124">**visLayerActive**</span></span> <br/> |
   

