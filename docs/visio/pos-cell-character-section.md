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
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806091"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="8876c-103">[Pos] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="8876c-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="8876c-104">基線に対する、図形のテキストの位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="8876c-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="8876c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8876c-105">**Value**</span></span>|<span data-ttu-id="8876c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8876c-106">**Description**</span></span>|<span data-ttu-id="8876c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="8876c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8876c-108">0</span><span class="sxs-lookup"><span data-stu-id="8876c-108">0</span></span>  <br/> | <span data-ttu-id="8876c-109">標準の位置</span><span class="sxs-lookup"><span data-stu-id="8876c-109">Normal position</span></span>  <br/> |<span data-ttu-id="8876c-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="8876c-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="8876c-111">1</span><span class="sxs-lookup"><span data-stu-id="8876c-111">1</span></span>  <br/> | <span data-ttu-id="8876c-112">上付き</span><span class="sxs-lookup"><span data-stu-id="8876c-112">Superscript</span></span>  <br/> |<span data-ttu-id="8876c-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="8876c-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="8876c-114">2</span><span class="sxs-lookup"><span data-stu-id="8876c-114">2</span></span>  <br/> | <span data-ttu-id="8876c-115">下付き</span><span class="sxs-lookup"><span data-stu-id="8876c-115">Subscript</span></span>  <br/> |<span data-ttu-id="8876c-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="8876c-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8876c-117">備考</span><span class="sxs-lookup"><span data-stu-id="8876c-117">Remarks</span></span>

<span data-ttu-id="8876c-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Pos] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8876c-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8876c-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="8876c-119">Cell name:</span></span>  <br/> | <span data-ttu-id="8876c-120">Char.Pos [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="8876c-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8876c-121">プログラムから、インデックスによって [Pos] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8876c-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8876c-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8876c-122">Section index:</span></span>  <br/> |<span data-ttu-id="8876c-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8876c-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="8876c-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8876c-124">Row index:</span></span>  <br/> |<span data-ttu-id="8876c-125">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="8876c-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8876c-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8876c-126">Cell index:</span></span>  <br/> |<span data-ttu-id="8876c-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="8876c-127">**visCharacterPos**</span></span> <br/> |
   

