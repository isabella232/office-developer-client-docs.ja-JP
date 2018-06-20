---
title: '[D] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: 数式を入力またはテストするために使用できる、スクラッチ セルです。
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805150"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="c93f8-103">[D] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="c93f8-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="c93f8-104">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="c93f8-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c93f8-105">備考</span><span class="sxs-lookup"><span data-stu-id="c93f8-105">Remarks</span></span>

<span data-ttu-id="c93f8-106">[D] セルにアクセスするには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c93f8-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="c93f8-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c93f8-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c93f8-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="c93f8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c93f8-109">Connections.D [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="c93f8-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c93f8-110">プログラムから、インデックスによって [D] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c93f8-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c93f8-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c93f8-111">Section index:</span></span>  <br/> |<span data-ttu-id="c93f8-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="c93f8-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="c93f8-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c93f8-113">Row index:</span></span>  <br/> |<span data-ttu-id="c93f8-114">**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="c93f8-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c93f8-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c93f8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c93f8-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="c93f8-116">**visCnnctD**</span></span> <br/> |
   

