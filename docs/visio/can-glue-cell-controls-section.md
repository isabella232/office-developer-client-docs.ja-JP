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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423294"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="86514-103">[Can Glue] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="86514-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="86514-104">コントロール ハンドルを他の図形に接着できるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="86514-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="86514-105">**値**</span><span class="sxs-lookup"><span data-stu-id="86514-105">**Value**</span></span>|<span data-ttu-id="86514-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="86514-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="86514-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="86514-107">TRUE</span></span>  <br/> | <span data-ttu-id="86514-108">コントロール ハンドルを接着できます。</span><span class="sxs-lookup"><span data-stu-id="86514-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="86514-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="86514-109">FALSE</span></span>  <br/> | <span data-ttu-id="86514-110">コントロール ハンドルを接着できません。</span><span class="sxs-lookup"><span data-stu-id="86514-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86514-111">注釈</span><span class="sxs-lookup"><span data-stu-id="86514-111">Remarks</span></span>

<span data-ttu-id="86514-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Can Glue] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="86514-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86514-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="86514-113">Cell name:</span></span>  <br/> | <span data-ttu-id="86514-114">コントロール。</span><span class="sxs-lookup"><span data-stu-id="86514-114">Controls.</span></span>  <span data-ttu-id="86514-115">*name*  .CanGluewhere コントロール。</span><span class="sxs-lookup"><span data-stu-id="86514-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="86514-116">*name*  は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="86514-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="86514-117">プログラムから、インデックスによって [Can Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="86514-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86514-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="86514-118">Section index:</span></span>  <br/> |<span data-ttu-id="86514-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="86514-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="86514-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="86514-120">Row index:</span></span>  <br/> |<span data-ttu-id="86514-121">**visRowControl**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="86514-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="86514-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="86514-122">Cell index:</span></span>  <br/> |<span data-ttu-id="86514-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="86514-123">**visCtlGlue**</span></span> <br/> |
   

