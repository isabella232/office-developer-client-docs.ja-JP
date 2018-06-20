---
title: '[図形の動作の変更] セクション'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: 置換操作の実行中に置換後の図形に、古い図形から転送されるプロパティが決まります。 値図形の置換操作の実行中にマスター シェイプの図形の動作の変更] セクションのセルの置換後の図形を読み取る。
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804984"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="9d925-104">[図形の動作の変更] セクション</span><span class="sxs-lookup"><span data-stu-id="9d925-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="9d925-105">置換操作の実行中に置換後の図形に、古い図形から転送されるプロパティが決まります。</span><span class="sxs-lookup"><span data-stu-id="9d925-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="9d925-106">値図形の置換操作の実行中にマスター シェイプの**図形の動作の変更**] セクションのセルの置換後の図形を読み取る。</span><span class="sxs-lookup"><span data-stu-id="9d925-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9d925-107">備考</span><span class="sxs-lookup"><span data-stu-id="9d925-107">Remarks</span></span>

<span data-ttu-id="9d925-108">**図形動作の変更**] セクションで、セルを設定することにより置換操作の実行中に置換後の図形の特定のプロパティは変更されないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9d925-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="9d925-109">保護されていないプロパティは、操作中に、古い図形から図形のローカル値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="9d925-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="9d925-110">置換を変更することができます、マスターを編集することにより図形のマスター シェイプの動作の設定の図形 ([**図形**] ウィンドウで、図形を右クリックし、**マスター シェイプの編集**] をポイントし、[**マスター シェイプの編集**] をクリックして)、[の値を変更してReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md)、 [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md)、 [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)、および[ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md)のマスター シェイプの [シェイプ シートのセルです。</span><span class="sxs-lookup"><span data-stu-id="9d925-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9d925-111">Microsoft Visio 2013 で組み込みのステンシルに含まれている図形の図形の置換動作を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d925-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="9d925-112">組み込みの Visio の図形の図形の置換動作を変更するに新しいステンシルを作成し、新しいステンシルを変更する図形を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d925-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

