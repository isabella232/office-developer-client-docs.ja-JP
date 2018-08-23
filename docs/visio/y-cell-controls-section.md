---
title: '[Y] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Y を表す-座標をローカル座標にある図形のコントロール ハンドルの位置を示します。
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806830"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="09a9b-103">[Y] セル ([コントロール] セクション)</span><span class="sxs-lookup"><span data-stu-id="09a9b-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="09a9b-104">*Y*を表す-座標をローカル座標にある図形のコントロール ハンドルの位置を示します。</span><span class="sxs-lookup"><span data-stu-id="09a9b-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="09a9b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="09a9b-105">Remarks</span></span>

<span data-ttu-id="09a9b-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="09a9b-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09a9b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="09a9b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="09a9b-108">制御します。</span><span class="sxs-lookup"><span data-stu-id="09a9b-108">Controls.</span></span>  <span data-ttu-id="09a9b-109">*名*です。Ywhere を制御します。</span><span class="sxs-lookup"><span data-stu-id="09a9b-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="09a9b-110">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="09a9b-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="09a9b-111">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="09a9b-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09a9b-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="09a9b-112">Section index:</span></span>  <br/> |<span data-ttu-id="09a9b-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="09a9b-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="09a9b-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="09a9b-114">Row index:</span></span>  <br/> |<span data-ttu-id="09a9b-115">**visRowControl** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="09a9b-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="09a9b-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="09a9b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="09a9b-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="09a9b-117">**visCtlY**</span></span> <br/> |
   

