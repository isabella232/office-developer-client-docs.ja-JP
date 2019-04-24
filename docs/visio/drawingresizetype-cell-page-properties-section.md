---
title: '[DrawingResizeType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80002
localization_priority: Normal
ms.assetid: 99a5ca0e-5cb4-64cc-8af5-15ac6d02c77f
description: 図面ページのサイズをダイアグラムに合わせて自動的に変更するかどうかを指定します。
ms.openlocfilehash: 6956c1e021ffffdb54f3dfa36270b9df04e892b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316500"
---
# <a name="drawingresizetype-cell-page-properties-section"></a><span data-ttu-id="5cf96-103">[DrawingResizeType] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="5cf96-103">DrawingResizeType Cell (Page Properties Section)</span></span>

<span data-ttu-id="5cf96-104">図面ページのサイズをダイアグラムに合わせて自動的に変更するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5cf96-104">Determines whether the drawing page resizes automatically to fit the diagram.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5cf96-105">解説</span><span class="sxs-lookup"><span data-stu-id="5cf96-105">Remarks</span></span>

<span data-ttu-id="5cf96-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingResizeType] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5cf96-106">To get a reference to the DrawingResizeType cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5cf96-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="5cf96-107">Cell name:</span></span>  <br/> |<span data-ttu-id="5cf96-108">[drawingresizetype]</span><span class="sxs-lookup"><span data-stu-id="5cf96-108">DrawingResizeType</span></span>  <br/> |
   
<span data-ttu-id="5cf96-109">プログラムから、インデックスによって [DrawingResizeType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5cf96-109">To get a reference to the DrawingResizeType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5cf96-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cf96-110">Section index:</span></span>  <br/> |<span data-ttu-id="5cf96-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5cf96-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5cf96-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cf96-112">Row index:</span></span>  <br/> |<span data-ttu-id="5cf96-113">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5cf96-113">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="5cf96-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cf96-114">Cell index:</span></span>  <br/> |<span data-ttu-id="5cf96-115">**visPageDrawResizeType**</span><span class="sxs-lookup"><span data-stu-id="5cf96-115">**visPageDrawResizeType**</span></span> <br/> |
   

