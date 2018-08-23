---
title: '[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 90ace659-d979-43e1-ac64-25af3ec5d666
description: (0.00 ~ 100.00 の範囲) をポイント単位での図形の影のぼかしのサイズを決定します。
ms.openlocfilehash: 87502e9e34252afa81aca1c480e2b1c61b2effaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806451"
---
# <a name="shapeshdwblur-cell-fill-format-section"></a><span data-ttu-id="ee793-103">[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="ee793-103">ShapeShdwBlur Cell (Fill Format Section)</span></span>

<span data-ttu-id="ee793-104">(0.00 ~ 100.00 の範囲) をポイント単位での図形の影のぼかしのサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee793-104">Determines the size of the blur for a shape's shadow, in points (0.00 to 100.00).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ee793-105">注釈</span><span class="sxs-lookup"><span data-stu-id="ee793-105">Remarks</span></span>

<span data-ttu-id="ee793-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ShapeShdwBlur** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ee793-106">To get a reference to the **ShapeShdwBlur** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee793-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="ee793-107">Cell name:</span></span>  <br/> | <span data-ttu-id="ee793-108">ShapeShdwBlur</span><span class="sxs-lookup"><span data-stu-id="ee793-108">ShapeShdwBlur</span></span>  <br/> |
   
<span data-ttu-id="ee793-109">プログラムから、インデックスによって [ **ShapeShdwBlur** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee793-109">To get a reference to the **ShapeShdwBlur** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee793-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee793-110">Section index:</span></span>  <br/> |<span data-ttu-id="ee793-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee793-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee793-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee793-112">Row index:</span></span>  <br/> |<span data-ttu-id="ee793-113">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ee793-113">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="ee793-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee793-114">Cell index:</span></span>  <br/> |<span data-ttu-id="ee793-115">**visFillShdwBlur**</span><span class="sxs-lookup"><span data-stu-id="ee793-115">**visFillShdwBlur**</span></span> <br/> |
   

