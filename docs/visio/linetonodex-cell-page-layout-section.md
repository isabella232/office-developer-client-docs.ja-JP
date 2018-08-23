---
title: '[LineToNodeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: 図面ページにあるすべてのコネクタと図形間の水平方向のクリアランスを指定します。
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805718"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="a017f-103">[LineToNodeX] セル ([ページ レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="a017f-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a017f-104">図面ページにあるすべてのコネクタと図形間の水平方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a017f-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a017f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a017f-105">Remarks</span></span>

<span data-ttu-id="a017f-p101">このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a017f-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a017f-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToNodeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a017f-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a017f-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="a017f-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a017f-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="a017f-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="a017f-111">プログラムから、インデックスによって [LineToNodeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a017f-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a017f-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a017f-112">Section index:</span></span>  <br/> |<span data-ttu-id="a017f-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a017f-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a017f-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a017f-114">Row index:</span></span>  <br/> |<span data-ttu-id="a017f-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a017f-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a017f-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a017f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a017f-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="a017f-117">**visPLOLineToNodeX**</span></span> <br/> |
   

