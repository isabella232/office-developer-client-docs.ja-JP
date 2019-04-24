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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349162"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="4cfd8-103">[ShapeShdwScaleFactor] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="4cfd8-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="4cfd8-104">図形の影を拡大または縮小できる割合を、パーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cfd8-105">解説</span><span class="sxs-lookup"><span data-stu-id="4cfd8-105">Remarks</span></span>

<span data-ttu-id="4cfd8-106">各影には影付きのピン位置があります。これは、図形の pin に対応する影上の点です。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="4cfd8-107">たとえば、図形のピンが図形の中央にある場合、影付きのピン位置は影の中心点になります。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="4cfd8-108">単純な影に倍率を適用すると、倍率は、影付きのピン位置に揃えられます。斜体の影に倍率を適用すると、斜体の方向に倍率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="4cfd8-109">この値をページのすべての図形に設定するには、[Page Properties] セクションで [ShdwScaleFactor] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="4cfd8-110">この値は、[**影**] ダイアログ ボックスの [**倍率**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="4cfd8-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cfd8-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="4cfd8-112">Cell name:</span></span>  <br/> |<span data-ttu-id="4cfd8-113">[shapeshdwscalefactor]</span><span class="sxs-lookup"><span data-stu-id="4cfd8-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="4cfd8-114">プログラムから、インデックスによって [ShapeShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cfd8-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cfd8-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4cfd8-115">Section index:</span></span>  <br/> |<span data-ttu-id="4cfd8-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4cfd8-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4cfd8-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4cfd8-117">Row index:</span></span>  <br/> |<span data-ttu-id="4cfd8-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="4cfd8-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="4cfd8-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4cfd8-119">Cell index:</span></span>  <br/> |<span data-ttu-id="4cfd8-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="4cfd8-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

