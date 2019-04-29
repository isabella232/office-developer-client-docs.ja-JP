---
title: '[X] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: 図形のコントロールハンドルの位置を示す x 座標を、ローカル座標で表します。
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406452"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="c607e-103">[X] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="c607e-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="c607e-104">図形のコントロールハンドルの位置を示す*x*座標を、ローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="c607e-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c607e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c607e-105">Remarks</span></span>

<span data-ttu-id="c607e-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c607e-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c607e-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="c607e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="c607e-108">管理.</span><span class="sxs-lookup"><span data-stu-id="c607e-108">Controls.</span></span>  <span data-ttu-id="c607e-109">*名前*です。X どこにコントロールを配置します。</span><span class="sxs-lookup"><span data-stu-id="c607e-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="c607e-110">*name*は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="c607e-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="c607e-111">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c607e-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c607e-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c607e-112">Section index:</span></span>  <br/> |<span data-ttu-id="c607e-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="c607e-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="c607e-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c607e-114">Row index:</span></span>  <br/> |<span data-ttu-id="c607e-115">**visRowControl** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="c607e-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c607e-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c607e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c607e-117">**visctlx**</span><span class="sxs-lookup"><span data-stu-id="c607e-117">**visCtlX**</span></span> <br/> |
   

