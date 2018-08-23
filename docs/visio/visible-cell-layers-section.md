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
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806763"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="95ab1-103">[Visible] セル ([レイヤー] セクション)</span><span class="sxs-lookup"><span data-stu-id="95ab1-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="95ab1-104">レイヤーに属している図形が図面ページに表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="95ab1-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="95ab1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="95ab1-105">**Value**</span></span>|<span data-ttu-id="95ab1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="95ab1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95ab1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="95ab1-107">TRUE</span></span>  <br/> |<span data-ttu-id="95ab1-108">図形は表示されます。</span><span class="sxs-lookup"><span data-stu-id="95ab1-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="95ab1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="95ab1-109">FALSE</span></span>  <br/> |<span data-ttu-id="95ab1-110">図形は表示されません。</span><span class="sxs-lookup"><span data-stu-id="95ab1-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95ab1-111">注釈</span><span class="sxs-lookup"><span data-stu-id="95ab1-111">Remarks</span></span>

<span data-ttu-id="95ab1-112">このセルは、[**レイヤー プロパティ**] ダイアログ ボックスの**表示**オプションに対応して ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="95ab1-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="95ab1-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Visible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95ab1-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95ab1-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="95ab1-114">Cell name:</span></span>  <br/> |<span data-ttu-id="95ab1-115">Layers.Visible [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="95ab1-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95ab1-116">プログラムから、インデックスによって [Visible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="95ab1-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95ab1-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ab1-117">Section index:</span></span>  <br/> |<span data-ttu-id="95ab1-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="95ab1-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="95ab1-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ab1-119">Row index:</span></span>  <br/> |<span data-ttu-id="95ab1-120">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="95ab1-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="95ab1-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="95ab1-121">Cell index:</span></span>  <br/> |<span data-ttu-id="95ab1-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="95ab1-122">**visLayerVisible**</span></span> <br/> |
   

