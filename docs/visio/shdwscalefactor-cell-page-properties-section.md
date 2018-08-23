---
title: '[ShdwScaleFactor] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: 図形の影を拡大または縮小する割合を、パーセントで指定します。
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806458"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="20aac-103">[ShdwScaleFactor] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="20aac-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="20aac-104">図形の影を拡大または縮小する割合を、パーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="20aac-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20aac-105">注釈</span><span class="sxs-lookup"><span data-stu-id="20aac-105">Remarks</span></span>

<span data-ttu-id="20aac-106">各シャドウには、図形のピンに対応する影があり、影の pin 位置があります。</span><span class="sxs-lookup"><span data-stu-id="20aac-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="20aac-107">たとえば、図形の pin は図形の中央には、影の pin 位置は影の中央にポイントをします。</span><span class="sxs-lookup"><span data-stu-id="20aac-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="20aac-108">シンプルな影に縮尺を適用する、拡大率は、影の pin 位置に中心斜体の影に縮尺を適用する、斜めの方向に拡大率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="20aac-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="20aac-109">図形の影の種類は、ページの既定値に設定されている場合は、このパーセンテージが使用される (ShapeShdwType のセルに等しい * * visFSTPageDefault * *)。</span><span class="sxs-lookup"><span data-stu-id="20aac-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals ** visFSTPageDefault ** ).</span></span> 
  
<span data-ttu-id="20aac-110">個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwScaleFactor] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="20aac-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="20aac-111">この値は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**倍率**] ボックスの値に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="20aac-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="20aac-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="20aac-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20aac-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="20aac-113">Cell name:</span></span>  <br/> | <span data-ttu-id="20aac-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="20aac-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="20aac-115">プログラムから、インデックスによって [ShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="20aac-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20aac-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aac-116">Section index:</span></span>  <br/> |<span data-ttu-id="20aac-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20aac-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20aac-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aac-118">Row index:</span></span>  <br/> |<span data-ttu-id="20aac-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="20aac-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="20aac-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aac-120">Cell index:</span></span>  <br/> |<span data-ttu-id="20aac-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="20aac-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

