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
description: 図形のコントロールハンドルの位置を示す y 座標を、ローカル座標で表します。
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407950"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="01c30-103">[Y] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="01c30-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="01c30-104">図形のコントロールハンドルの位置を示す*y*座標を、ローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="01c30-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01c30-105">注釈</span><span class="sxs-lookup"><span data-stu-id="01c30-105">Remarks</span></span>

<span data-ttu-id="01c30-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="01c30-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01c30-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="01c30-107">Cell name:</span></span>  <br/> | <span data-ttu-id="01c30-108">管理.</span><span class="sxs-lookup"><span data-stu-id="01c30-108">Controls.</span></span>  <span data-ttu-id="01c30-109">*名前*です。ywhere コントロール</span><span class="sxs-lookup"><span data-stu-id="01c30-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="01c30-110">*name*は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="01c30-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="01c30-111">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="01c30-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01c30-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="01c30-112">Section index:</span></span>  <br/> |<span data-ttu-id="01c30-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="01c30-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="01c30-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="01c30-114">Row index:</span></span>  <br/> |<span data-ttu-id="01c30-115">**visRowControl** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="01c30-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="01c30-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="01c30-116">Cell index:</span></span>  <br/> |<span data-ttu-id="01c30-117">**visctly**</span><span class="sxs-lookup"><span data-stu-id="01c30-117">**visCtlY**</span></span> <br/> |
   

