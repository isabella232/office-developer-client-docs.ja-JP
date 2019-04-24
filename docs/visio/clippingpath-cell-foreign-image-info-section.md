---
title: '[ClippingPath] セル ([外部イメージの情報] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: イメージを限定しているパスの図形座標への参照を格納します。
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341861"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="dcfa7-103">[ClippingPath] セル ([外部イメージの情報] セクション)</span><span class="sxs-lookup"><span data-stu-id="dcfa7-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="dcfa7-104">イメージを限定しているパスの図形座標への参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dcfa7-105">解説</span><span class="sxs-lookup"><span data-stu-id="dcfa7-105">Remarks</span></span>

<span data-ttu-id="dcfa7-106">[**ClippingPath**] セルが有効なパスを示している場合、イメージがクリップされるため、イメージはパス内で描画されます。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="dcfa7-107">[**ClippingPath**] セルが空か、無効なエントリが格納されている場合は、イメージは、スケール値とオフセット値を使用した角形のクリップで描画されます。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dcfa7-108">イメージのシェイプシートの [ [Geometry](geometry-section.md) ] セクションで定義されているパスのみが、 **[clippingpath]** セルの有効なエントリです。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="dcfa7-109">イメージのクリッピング パスの定義に、シート間参照は使用できません。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="dcfa7-110">別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**ClippingPath**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcfa7-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="dcfa7-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dcfa7-112">[clippingpath]</span><span class="sxs-lookup"><span data-stu-id="dcfa7-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="dcfa7-113">プログラムから、インデックスによって [**ClippingPath**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcfa7-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcfa7-114">Section index:</span></span>  <br/> |<span data-ttu-id="dcfa7-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dcfa7-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dcfa7-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcfa7-116">Row index:</span></span>  <br/> |<span data-ttu-id="dcfa7-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="dcfa7-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="dcfa7-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dcfa7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dcfa7-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="dcfa7-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="dcfa7-120">例</span><span class="sxs-lookup"><span data-stu-id="dcfa7-120">Example</span></span>

<span data-ttu-id="dcfa7-121">次の操作を実行して、イメージの境界図形を楕円に変更できます。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="dcfa7-122">描画キャンバスに図を挿入します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="dcfa7-123">図を右クリックして、[**シェイプシートの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="dcfa7-124">シェイプシート上を右クリックして、[**Insert Section**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="dcfa7-125">[**セクションの挿入**] ダイアログ ボックスで、[**図形座標**] を選択して [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="dcfa7-126">[新しい Geometry] セクション (例: "Geometry2") で、1行を除くすべてを削除します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="dcfa7-127">残りの行を右クリックして、[**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="dcfa7-128">[**図形要素の変更**] ダイアログ ボックスで、[**楕円**] を選択して [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="dcfa7-129">[**外部イメージ**] セクションで、 **[clippingpath]** セルの数式をに`="Geometry2.Path"`設定して、その数式を確定します。</span><span class="sxs-lookup"><span data-stu-id="dcfa7-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

