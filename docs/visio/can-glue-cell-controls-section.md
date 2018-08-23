---
title: '[Can Glue] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: コントロール ハンドルを他の図形に接着できるかを指定します。
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804930"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="ee09e-103">[Can Glue] セル ([コントロール] セクション)</span><span class="sxs-lookup"><span data-stu-id="ee09e-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="ee09e-104">コントロール ハンドルを他の図形に接着できるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee09e-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="ee09e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ee09e-105">**Value**</span></span>|<span data-ttu-id="ee09e-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ee09e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ee09e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ee09e-107">TRUE</span></span>  <br/> | <span data-ttu-id="ee09e-108">コントロール ハンドルを接着できます。</span><span class="sxs-lookup"><span data-stu-id="ee09e-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="ee09e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ee09e-109">FALSE</span></span>  <br/> | <span data-ttu-id="ee09e-110">コントロール ハンドルを接着できません。</span><span class="sxs-lookup"><span data-stu-id="ee09e-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee09e-111">備考</span><span class="sxs-lookup"><span data-stu-id="ee09e-111">Remarks</span></span>

<span data-ttu-id="ee09e-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Can Glue] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee09e-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee09e-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="ee09e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ee09e-114">制御します。</span><span class="sxs-lookup"><span data-stu-id="ee09e-114">Controls.</span></span>  <span data-ttu-id="ee09e-115">*名*です。CanGluewhere を制御します。</span><span class="sxs-lookup"><span data-stu-id="ee09e-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="ee09e-116">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="ee09e-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="ee09e-117">プログラムから、インデックスによって [Can Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee09e-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee09e-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee09e-118">Section index:</span></span>  <br/> |<span data-ttu-id="ee09e-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="ee09e-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="ee09e-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee09e-120">Row index:</span></span>  <br/> |<span data-ttu-id="ee09e-121">**visRowControl** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="ee09e-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="ee09e-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ee09e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ee09e-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="ee09e-123">**visCtlGlue**</span></span> <br/> |
   

