---
title: '[図形の動作の変更] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: 置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[図形の動作の変更] セクションのセルの値は、図形の置換操作時に読み込まれます。
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804984"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="09a0e-104">[図形動作の変更] セクション</span><span class="sxs-lookup"><span data-stu-id="09a0e-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="09a0e-p102">置換操作時に、古い図形から置換後の図形に転送されるプロパティを決定します。置換後のマスター シェイプの、[**図形の動作の変更**] セクションのセルの値は、図形の置換操作時に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="09a0e-p102">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation. The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="09a0e-107">注釈</span><span class="sxs-lookup"><span data-stu-id="09a0e-107">Remarks</span></span>

<span data-ttu-id="09a0e-p103">[**図形の動作の変更**] セクションのセルを設定することで、図形の置換操作時に、置換後の図形の一定のプロパティが変更されないようにできます。保護されていないプロパティは、この操作時に古い図形のローカルな図形値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="09a0e-p103">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation. Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="09a0e-110">置換を変更することができます、マスターを編集することにより図形のマスター シェイプの動作の設定の図形 ([**図形**] ウィンドウで、図形を右クリックし、**マスター シェイプの編集**] をポイントし、[**マスター シェイプの編集**] をクリックして)、[の値を変更してReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md)、 [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md)、 [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)、および[ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md)のマスター シェイプの [シェイプ シートのセルです。</span><span class="sxs-lookup"><span data-stu-id="09a0e-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="09a0e-111">Microsoft Visio 2013 で組み込みのステンシルに含まれている図形の図形の置換動作を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="09a0e-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="09a0e-112">組み込みの Visio の図形の図形の置換動作を変更するに新しいステンシルを作成し、新しいステンシルを変更する図形を追加します。</span><span class="sxs-lookup"><span data-stu-id="09a0e-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

