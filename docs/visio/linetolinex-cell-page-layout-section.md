---
title: '[LineToLineX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: 図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416329"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="b5cc5-103">[LineToLineX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="b5cc5-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="b5cc5-104">図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5cc5-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5cc5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="b5cc5-105">Remarks</span></span>

<span data-ttu-id="b5cc5-p101">このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="b5cc5-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="b5cc5-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToLineX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b5cc5-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5cc5-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b5cc5-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="b5cc5-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="b5cc5-111">プログラムから、インデックスによって [LineToLineX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5cc5-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5cc5-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-112">Section index:</span></span>  <br/> |<span data-ttu-id="b5cc5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5cc5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b5cc5-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-114">Row index:</span></span>  <br/> |<span data-ttu-id="b5cc5-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b5cc5-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b5cc5-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b5cc5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b5cc5-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="b5cc5-117">**visPLOLineToLineX**</span></span> <br/> |
   

