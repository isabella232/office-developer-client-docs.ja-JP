---
title: '[ClippingPath] セル ([外部イメージの情報] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: イメージを限定しているパスの図形座標への参照を格納します。
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805008"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="f716c-103">[ClippingPath] セル ([外部イメージの情報] セクション)</span><span class="sxs-lookup"><span data-stu-id="f716c-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="f716c-104">イメージを限定しているパスの図形座標への参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="f716c-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f716c-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="f716c-105">Remarks</span></span>

<span data-ttu-id="f716c-106">**ClippingPath**セルは、有効なパスをポイントしている場合、パス内にイメージを表示できるように、イメージはクリップされます。</span><span class="sxs-lookup"><span data-stu-id="f716c-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="f716c-107">**ClippingPath**のセルが空か、無効なエントリが含まれている場合、スケールとオフセットの値を使用して四角形のクリップにイメージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f716c-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f716c-108">イメージのシェイプ シートの[[Geometry](geometry-section.md) ] セクションで定義されたパスだけは、 **ClippingPath**セルの有効なエントリです。</span><span class="sxs-lookup"><span data-stu-id="f716c-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="f716c-109">シートの相互参照は、画像クリッピングパスを定義するのには使用できません。</span><span class="sxs-lookup"><span data-stu-id="f716c-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="f716c-110">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ClippingPath** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f716c-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f716c-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="f716c-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f716c-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="f716c-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="f716c-113">プログラムから、インデックスによって [ **ClippingPath** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f716c-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f716c-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f716c-114">Section index:</span></span>  <br/> |<span data-ttu-id="f716c-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f716c-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f716c-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f716c-116">Row index:</span></span>  <br/> |<span data-ttu-id="f716c-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="f716c-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="f716c-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f716c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f716c-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="f716c-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="f716c-120">次の使用例では、テーブルからレコードを削除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="f716c-120">Example</span></span>

<span data-ttu-id="f716c-121">次の操作を実行して、イメージの境界図形を楕円に変更できます。</span><span class="sxs-lookup"><span data-stu-id="f716c-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="f716c-122">描画キャンバスに図を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f716c-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="f716c-123">画像を右クリックし、**シェイプ シートを表示**します。</span><span class="sxs-lookup"><span data-stu-id="f716c-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="f716c-124">シェイプ シート内の任意の場所を右クリックし、 **[セクションの挿入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f716c-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="f716c-125">**セクションの挿入**] ダイアログ ボックスで**ジオメトリ**を選択し、し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f716c-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="f716c-126">新しいジオメトリ セクション (例:"Geometry2"など) では、1 つを除くすべての行を削除します。</span><span class="sxs-lookup"><span data-stu-id="f716c-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="f716c-127">残りの行を右クリックし、**行の種類の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f716c-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="f716c-128">**行の種類の変更**] ダイアログ ボックスでは、**楕円**を選択し、し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f716c-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="f716c-129">**外部イメージ**セクションで、 **ClippingPath**のセルの数式を設定します`="Geometry2.Path"`し、数式を使用します。</span><span class="sxs-lookup"><span data-stu-id="f716c-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

