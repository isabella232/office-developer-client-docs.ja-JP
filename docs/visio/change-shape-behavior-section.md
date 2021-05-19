---
title: '[図形の動作の変更] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: 置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[図形の動作の変更] セクションのセルの値は、図形の置換操作時に読み込まれます。
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418667"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="cf8d5-104">[図形の動作の変更] セクション</span><span class="sxs-lookup"><span data-stu-id="cf8d5-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="cf8d5-p102">置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[**図形の動作の変更**] セクションのセルの値は、図形の置換操作時に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="cf8d5-p102">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation. The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf8d5-107">注釈</span><span class="sxs-lookup"><span data-stu-id="cf8d5-107">Remarks</span></span>

<span data-ttu-id="cf8d5-p103">[**図形の動作の変更**] セクションのセルを設定することで、図形の置換操作時に、置換後の図形の一定のプロパティが変更されないようにできます。保護されていないプロパティは、この操作時に古い図形のローカルな図形値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="cf8d5-p103">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation. Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="cf8d5-110">マスター シェイプの置換動作設定を変更するには、マスター シェイプを編集します ([シェイプ] ウィンドウで図形を右クリックし、[マスター シェイプの編集] をポイントし、[マスター シェイプの編集] をクリックします)、マスター シェイプシートの[ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md) [、ReplaceLockFormat、ReplaceLockShapeData、](replacelockformat-cell-change-shape-behavior-section.md)[および ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md)セルの値を変更します。  [](replacelockshapedata-cell-change-shape-behavior-section.md)</span><span class="sxs-lookup"><span data-stu-id="cf8d5-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cf8d5-111">Microsoft Visio 2013 の組み込みのステンシルに含まれる図形の図形置換動作を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="cf8d5-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="cf8d5-112">組み込みの Visio図形の図形置換動作を変更するには、新しいステンシルを作成し、変更する図形を新しいステンシルに追加します。</span><span class="sxs-lookup"><span data-stu-id="cf8d5-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

