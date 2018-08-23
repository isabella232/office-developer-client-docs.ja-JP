---
title: '[FillGradientAngle] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf9af5a5-e042-4d56-a29f-341d97cdb97b
description: 角度の直線の方向にグラデーションの塗りつぶしのグラデーションの角度を決定します。
ms.openlocfilehash: 5e819524e993ecb4c7ed35ad56ae9d1e1b35f345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805372"
---
# <a name="fillgradientangle-cell-gradient-properties-section"></a><span data-ttu-id="11b0e-103">[FillGradientAngle] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="11b0e-103">FillGradientAngle Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="11b0e-104">角度の直線の方向にグラデーションの塗りつぶしのグラデーションの角度を決定します。</span><span class="sxs-lookup"><span data-stu-id="11b0e-104">Determines the angle of the fill gradient for gradients with a linear direction, in degrees.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="11b0e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="11b0e-105">Remarks</span></span>

<span data-ttu-id="11b0e-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **FillGradientAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="11b0e-106">To get a reference to the **FillGradientAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11b0e-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="11b0e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="11b0e-108">FillGradientAngle</span><span class="sxs-lookup"><span data-stu-id="11b0e-108">FillGradientAngle</span></span>  <br/> |
   
<span data-ttu-id="11b0e-109">プログラムから、インデックスによって [ **FillGradientAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="11b0e-109">To get a reference to the **FillGradientAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11b0e-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="11b0e-110">Section index:</span></span>  <br/> |<span data-ttu-id="11b0e-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11b0e-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11b0e-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="11b0e-112">Row index:</span></span>  <br/> |<span data-ttu-id="11b0e-113">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="11b0e-113">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="11b0e-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="11b0e-114">Cell index:</span></span>  <br/> |<span data-ttu-id="11b0e-115">**visFillGradientAngle**</span><span class="sxs-lookup"><span data-stu-id="11b0e-115">**visFillGradientAngle**</span></span> <br/> |
   

