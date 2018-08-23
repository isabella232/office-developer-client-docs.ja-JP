---
title: '[ShapeShdwScaleFactor] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: 図形の影を拡大または縮小できる割合を、パーセントで指定します。
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806438"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="68297-103">[ShapeShdwScaleFactor] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="68297-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="68297-104">図形の影を拡大または縮小できる割合を、パーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="68297-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68297-105">注釈</span><span class="sxs-lookup"><span data-stu-id="68297-105">Remarks</span></span>

<span data-ttu-id="68297-106">各シャドウには、図形のピンに対応する影があり、影の pin 位置があります。</span><span class="sxs-lookup"><span data-stu-id="68297-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="68297-107">たとえば、図形の pin は図形の中央には、影の pin 位置は影の中央にポイントをします。</span><span class="sxs-lookup"><span data-stu-id="68297-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="68297-108">シンプルな影に縮尺を適用する、拡大率は、影の pin 位置に中心斜体の影に縮尺を適用する、斜めの方向に拡大率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="68297-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="68297-109">この値をページのすべての図形に設定するには、[Page Properties] セクションで [ShdwScaleFactor] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="68297-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="68297-110">この値は、[**影**] ダイアログ ボックスの [**倍率**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="68297-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="68297-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="68297-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68297-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="68297-112">Cell name:</span></span>  <br/> |<span data-ttu-id="68297-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="68297-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="68297-114">プログラムから、インデックスによって [ShapeShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="68297-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68297-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="68297-115">Section index:</span></span>  <br/> |<span data-ttu-id="68297-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68297-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="68297-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="68297-117">Row index:</span></span>  <br/> |<span data-ttu-id="68297-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="68297-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="68297-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="68297-119">Cell index:</span></span>  <br/> |<span data-ttu-id="68297-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="68297-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

