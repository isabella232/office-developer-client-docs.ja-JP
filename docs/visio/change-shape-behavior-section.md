---
title: '[図形の動作の変更] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: 置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。 置換後のマスター シェイプの、[図形の動作の変更] セクションのセルの値は、図形の置換操作時に読み込まれます。
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341924"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="8c3d7-104">[図形の動作の変更] セクション</span><span class="sxs-lookup"><span data-stu-id="8c3d7-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="8c3d7-p102">置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[**図形の動作の変更**] セクションのセルの値は、図形の置換操作時に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="8c3d7-p102">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation. The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8c3d7-107">解説</span><span class="sxs-lookup"><span data-stu-id="8c3d7-107">Remarks</span></span>

<span data-ttu-id="8c3d7-p103">[**図形の動作の変更**] セクションのセルを設定することで、図形の置換操作時に、置換後の図形の一定のプロパティが変更されないようにできます。保護されていないプロパティは、この操作時に古い図形のローカルな図形値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="8c3d7-p103">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation. Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="8c3d7-110">マスターシェイプの置換動作の設定を変更するには、マスターシェイプを編集します ([**図形**] ウィンドウで、図形を右クリックし、[**マスター**シェイプの編集] をポイントして、[**マスターシェイプの編集**] をクリックし、次の[値を変更します)。](replacecopycells-cell-change-shape-behavior-section.md)マスターシェイプシートの [replacecopycells]、 [replacelockformat](replacelockformat-cell-change-shape-behavior-section.md)、 [replacelockformat データ](replacelockshapedata-cell-change-shape-behavior-section.md)、および[replacelockformat](replacelocktext-cell-change-shape-behavior-section.md)セル。</span><span class="sxs-lookup"><span data-stu-id="8c3d7-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8c3d7-111">Microsoft Visio 2013 の組み込みステンシルに含まれる図形の図形の置換動作を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8c3d7-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="8c3d7-112">組み込みの Visio 図形の図形の置換動作を変更するには、新しいステンシルを作成し、変更する図形を新しいステンシルに追加します。</span><span class="sxs-lookup"><span data-stu-id="8c3d7-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

