---
title: '[Perspective] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: 遠近角度の角度を度 (0 ~ 359.9) で指定します。
ms.openlocfilehash: 4cbefc2fa147a418fa792542e1dc57c39ab2490c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422531"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a><span data-ttu-id="fd317-103">[Perspective] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="fd317-103">Perspective Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="fd317-104">遠近角度の角度を度 (0 ~ 359.9) で指定します。</span><span class="sxs-lookup"><span data-stu-id="fd317-104">Determines the perspective angle for a perspective rotation, in degrees (0 to 359.9)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd317-105">注釈</span><span class="sxs-lookup"><span data-stu-id="fd317-105">Remarks</span></span>

<span data-ttu-id="fd317-106">別の数式、Cell要素 **の N** 属性の値、**または CellsU** プロパティを使用したプログラムから、名前によって [パースペクティブ] セルへの参照を取得するには、次の値を **使用** します。</span><span class="sxs-lookup"><span data-stu-id="fd317-106">To get a reference to the **Perspective** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd317-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="fd317-107">Cell name:</span></span>  <br/> |<span data-ttu-id="fd317-108">Perspective</span><span class="sxs-lookup"><span data-stu-id="fd317-108">Perspective</span></span>  <br/> |
   
<span data-ttu-id="fd317-109">プログラムからインデックスによって **[パース** ペクティブ] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd317-109">To get a reference to the **Perspective** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd317-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd317-110">Section index:</span></span>  <br/> |<span data-ttu-id="fd317-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd317-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fd317-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd317-112">Row index:</span></span>  <br/> |<span data-ttu-id="fd317-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="fd317-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="fd317-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd317-114">Cell index:</span></span>  <br/> |<span data-ttu-id="fd317-115">**visPerspective**</span><span class="sxs-lookup"><span data-stu-id="fd317-115">**visPerspective**</span></span> <br/> |
   

