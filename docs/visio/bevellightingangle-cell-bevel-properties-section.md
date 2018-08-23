---
title: '[BevelLightingAngle] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 537f5100-a8cf-4e29-81a5-bb71a80a7178
description: 度の傾斜面を基準にして稲妻の角度を決定します。
ms.openlocfilehash: 85610b40010664f30360f2b82252a31fa4129a17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804826"
---
# <a name="bevellightingangle-cell-bevel-properties-section"></a><span data-ttu-id="414e5-103">[BevelLightingAngle] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="414e5-103">BevelLightingAngle Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="414e5-104">度の傾斜面を基準にして稲妻の角度を決定します。</span><span class="sxs-lookup"><span data-stu-id="414e5-104">Determines the angle of lightning in relation to the bevel in degrees.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="414e5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="414e5-105">Remarks</span></span>

<span data-ttu-id="414e5-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelLightingAngle** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="414e5-106">To get a reference to the **BevelLightingAngle** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="414e5-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="414e5-107">Cell name:</span></span>  <br/> | <span data-ttu-id="414e5-108">BevelLightingAngle</span><span class="sxs-lookup"><span data-stu-id="414e5-108">BevelLightingAngle</span></span>  <br/> |
   
<span data-ttu-id="414e5-109">プログラムから、インデックスによって [ **BevelLightingAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="414e5-109">To get a reference to the **BevelLightingAngle** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="414e5-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="414e5-110">Section index:</span></span>  <br/> |<span data-ttu-id="414e5-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="414e5-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="414e5-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="414e5-112">Row index:</span></span>  <br/> |<span data-ttu-id="414e5-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="414e5-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="414e5-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="414e5-114">Cell index:</span></span>  <br/> |<span data-ttu-id="414e5-115">**visBevelLightingAngle**</span><span class="sxs-lookup"><span data-stu-id="414e5-115">**visBevelLightingAngle**</span></span> <br/> |
   

