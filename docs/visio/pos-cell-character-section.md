---
title: '[Pos] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: 基線に対する、図形のテキストの位置を指定します。
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414019"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="f1b1e-103">[Pos] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="f1b1e-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="f1b1e-104">基線に対する、図形のテキストの位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1b1e-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="f1b1e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-105">**Value**</span></span>|<span data-ttu-id="f1b1e-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-106">**Description**</span></span>|<span data-ttu-id="f1b1e-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f1b1e-108">0</span><span class="sxs-lookup"><span data-stu-id="f1b1e-108">0</span></span>  <br/> | <span data-ttu-id="f1b1e-109">標準の位置</span><span class="sxs-lookup"><span data-stu-id="f1b1e-109">Normal position</span></span>  <br/> |<span data-ttu-id="f1b1e-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="f1b1e-111">1</span><span class="sxs-lookup"><span data-stu-id="f1b1e-111">1</span></span>  <br/> | <span data-ttu-id="f1b1e-112">Superscript</span><span class="sxs-lookup"><span data-stu-id="f1b1e-112">Superscript</span></span>  <br/> |<span data-ttu-id="f1b1e-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="f1b1e-114">2</span><span class="sxs-lookup"><span data-stu-id="f1b1e-114">2</span></span>  <br/> | <span data-ttu-id="f1b1e-115">Subscript</span><span class="sxs-lookup"><span data-stu-id="f1b1e-115">Subscript</span></span>  <br/> |<span data-ttu-id="f1b1e-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1b1e-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f1b1e-117">Remarks</span></span>

<span data-ttu-id="f1b1e-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Pos] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f1b1e-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1b1e-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="f1b1e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f1b1e-120">Char.Pos[  *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="f1b1e-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f1b1e-121">プログラムから、インデックスによって [Pos] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1b1e-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1b1e-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f1b1e-122">Section index:</span></span>  <br/> |<span data-ttu-id="f1b1e-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="f1b1e-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f1b1e-124">Row index:</span></span>  <br/> |<span data-ttu-id="f1b1e-125">**visRowCharacter**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f1b1e-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f1b1e-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f1b1e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="f1b1e-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="f1b1e-127">**visCharacterPos**</span></span> <br/> |
   

