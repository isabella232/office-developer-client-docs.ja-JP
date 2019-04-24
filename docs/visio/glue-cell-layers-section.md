---
title: '[Glue] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: レイヤーに属している図形が接着可能かどうかを指定します。
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332810"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="39f15-103">[Glue] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="39f15-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="39f15-104">レイヤーに属している図形が接着可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="39f15-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="39f15-105">**値**</span><span class="sxs-lookup"><span data-stu-id="39f15-105">**Value**</span></span>|<span data-ttu-id="39f15-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="39f15-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39f15-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="39f15-107">TRUE</span></span>  <br/> |<span data-ttu-id="39f15-108">接着できます。</span><span class="sxs-lookup"><span data-stu-id="39f15-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="39f15-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="39f15-109">FALSE</span></span>  <br/> |<span data-ttu-id="39f15-110">接着できません。</span><span class="sxs-lookup"><span data-stu-id="39f15-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39f15-111">解説</span><span class="sxs-lookup"><span data-stu-id="39f15-111">Remarks</span></span>

<span data-ttu-id="39f15-112">このセルは、[**レイヤープロパティ**] ダイアログボックス ([**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックし、[**レイヤープロパティ**] をクリック) の [**接着**] オプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="39f15-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="39f15-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Glue] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="39f15-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39f15-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="39f15-114">Cell name:</span></span>  <br/> |<span data-ttu-id="39f15-115">レイヤー. グルー [ *i* ] = \*\* <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="39f15-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="39f15-116">プログラムから、インデックスによって [Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="39f15-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39f15-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="39f15-117">Section index:</span></span>  <br/> |<span data-ttu-id="39f15-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="39f15-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="39f15-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="39f15-119">Row index:</span></span>  <br/> |<span data-ttu-id="39f15-120">**visRowLayer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="39f15-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="39f15-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="39f15-121">Cell index:</span></span>  <br/> |<span data-ttu-id="39f15-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="39f15-122">**visLayerGlue**</span></span> <br/> |
   

