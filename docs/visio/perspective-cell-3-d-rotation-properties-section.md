---
title: '[Perspective] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: 度 (0 359.9) で、面内の回転の遠近の角度を決定します。
ms.openlocfilehash: 6ab087b07dceda6e8f02a3ddb49a50d6159366d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805984"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a><span data-ttu-id="7914c-103">[Perspective] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="7914c-103">Perspective Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="7914c-104">度 (0 359.9) で、面内の回転の遠近の角度を決定します。</span><span class="sxs-lookup"><span data-stu-id="7914c-104">Determines the perspective angle for a perspective rotation, in degrees (0 to 359.9)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7914c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="7914c-105">Remarks</span></span>

<span data-ttu-id="7914c-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって**透視投影**] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7914c-106">To get a reference to the **Perspective** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7914c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="7914c-107">Cell name:</span></span>  <br/> |<span data-ttu-id="7914c-108">パースペクティブ</span><span class="sxs-lookup"><span data-stu-id="7914c-108">Perspective</span></span>  <br/> |
   
<span data-ttu-id="7914c-109">プログラムから、インデックスによって [**分析観点**] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7914c-109">To get a reference to the **Perspective** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7914c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7914c-110">Section index:</span></span>  <br/> |<span data-ttu-id="7914c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7914c-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7914c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7914c-112">Row index:</span></span>  <br/> |<span data-ttu-id="7914c-113">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="7914c-113">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="7914c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7914c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="7914c-115">**visPerspective**</span><span class="sxs-lookup"><span data-stu-id="7914c-115">**visPerspective**</span></span> <br/> |
   

