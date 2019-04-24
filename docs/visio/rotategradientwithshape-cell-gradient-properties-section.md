---
title: '[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: 塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315660"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="755d4-103">[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="755d4-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="755d4-104">塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="755d4-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="755d4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="755d4-105">**Value**</span></span>|<span data-ttu-id="755d4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="755d4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="755d4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="755d4-107">TRUE</span></span>  <br/> |<span data-ttu-id="755d4-108">図形が回転ピンを中心に回転するとき、グラデーションは図形に合わせて回転します。</span><span class="sxs-lookup"><span data-stu-id="755d4-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="755d4-109">グラデーションの "上部" は、回転ハンドルに対して平行です。</span><span class="sxs-lookup"><span data-stu-id="755d4-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="755d4-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="755d4-110">FALSE</span></span>  <br/> |<span data-ttu-id="755d4-111">図形が回転ピンを中心に回転するとき、グラデーションは図形に合せて回転しません。</span><span class="sxs-lookup"><span data-stu-id="755d4-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="755d4-112">グラデーションの "上部" は、描画キャンバスに対して平行です。</span><span class="sxs-lookup"><span data-stu-id="755d4-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="755d4-113">解説</span><span class="sxs-lookup"><span data-stu-id="755d4-113">Remarks</span></span>

<span data-ttu-id="755d4-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotateGradientWithShape**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="755d4-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="755d4-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="755d4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="755d4-116">[rotategradientwithshape]</span><span class="sxs-lookup"><span data-stu-id="755d4-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="755d4-117">プログラムから、インデックスによって [**RotateGradientWithShape**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="755d4-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="755d4-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="755d4-118">Section index:</span></span>  <br/> |<span data-ttu-id="755d4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="755d4-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="755d4-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="755d4-120">Row index:</span></span>  <br/> |<span data-ttu-id="755d4-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="755d4-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="755d4-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="755d4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="755d4-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="755d4-123">**visRotateGradientWithShape**</span></span> <br/> |
   

