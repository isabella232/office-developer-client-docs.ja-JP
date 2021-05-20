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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436266"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="a8ae2-103">[ShapeShdwScaleFactor] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="a8ae2-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="a8ae2-104">図形の影を拡大または縮小できる割合を、パーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8ae2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a8ae2-105">Remarks</span></span>

<span data-ttu-id="a8ae2-106">各シャドウには影付きピンの位置があります。これは、図形のピンに対応するシャドウ上のポイントです。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="a8ae2-107">たとえば、図形のピンが図形の中央にある場合、影付きピンの位置は影の中心のポイントになります。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="a8ae2-108">単純な影にスケールを適用する場合、倍率は影付きピンの位置の中央に配置されます。斜めの影にスケールを適用すると、斜め方向に倍率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="a8ae2-109">この値をページのすべての図形に設定するには、[Page Properties] セクションで [ShdwScaleFactor] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="a8ae2-110">この値は、[**影**] ダイアログ ボックスの [**倍率**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="a8ae2-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ae2-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="a8ae2-112">Cell name:</span></span>  <br/> |<span data-ttu-id="a8ae2-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="a8ae2-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="a8ae2-114">プログラムから、インデックスによって [ShapeShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8ae2-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ae2-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8ae2-115">Section index:</span></span>  <br/> |<span data-ttu-id="a8ae2-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8ae2-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a8ae2-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8ae2-117">Row index:</span></span>  <br/> |<span data-ttu-id="a8ae2-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="a8ae2-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="a8ae2-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8ae2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a8ae2-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="a8ae2-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

