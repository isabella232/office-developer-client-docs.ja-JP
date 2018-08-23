---
title: '[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: 塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806242"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="67375-103">[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="67375-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="67375-104">塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="67375-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="67375-105">**値**</span><span class="sxs-lookup"><span data-stu-id="67375-105">**Value**</span></span>|<span data-ttu-id="67375-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="67375-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67375-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="67375-107">TRUE</span></span>  <br/> |<span data-ttu-id="67375-108">グラデーションは、周りの回転の暗証番号 (pin)、図形を回転させて、図形を回転します。</span><span class="sxs-lookup"><span data-stu-id="67375-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="67375-109">グラデーションの「上」は、回転ハンドルに平行です。</span><span class="sxs-lookup"><span data-stu-id="67375-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="67375-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="67375-110">FALSE</span></span>  <br/> |<span data-ttu-id="67375-111">回転の暗証番号 (pin) を中心に図形を回転すると、グラデーションは図形を回転しません。</span><span class="sxs-lookup"><span data-stu-id="67375-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="67375-112">グラデーションの「上」は、描画キャンバスに平行です。</span><span class="sxs-lookup"><span data-stu-id="67375-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67375-113">注釈</span><span class="sxs-lookup"><span data-stu-id="67375-113">Remarks</span></span>

<span data-ttu-id="67375-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotateGradientWithShape**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="67375-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67375-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="67375-115">Cell name:</span></span>  <br/> | <span data-ttu-id="67375-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="67375-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="67375-117">プログラムから、インデックスによって [**RotateGradientWithShape**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="67375-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67375-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="67375-118">Section index:</span></span>  <br/> |<span data-ttu-id="67375-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="67375-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="67375-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="67375-120">Row index:</span></span>  <br/> |<span data-ttu-id="67375-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="67375-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="67375-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="67375-122">Cell index:</span></span>  <br/> |<span data-ttu-id="67375-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="67375-123">**visRotateGradientWithShape**</span></span> <br/> |
   

