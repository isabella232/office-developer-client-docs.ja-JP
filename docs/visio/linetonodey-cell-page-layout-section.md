---
title: '[LineToNodeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251650
localization_priority: Normal
ms.assetid: 49d649e8-1603-192b-2984-e5d0b713da89
description: 図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。
ms.openlocfilehash: 2a5e4469fae2fb3142db2745f26c2009d42c0d2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432332"
---
# <a name="linetonodey-cell-page-layout-section"></a><span data-ttu-id="d1fe9-103">[LineToNodeY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1fe9-103">LineToNodeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="d1fe9-104">図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fe9-104">Determines the vertical clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1fe9-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d1fe9-105">Remarks</span></span>

<span data-ttu-id="d1fe9-p101">このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d1fe9-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="d1fe9-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToNodeY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1fe9-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1fe9-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1fe9-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d1fe9-110">LineToNodeY</span><span class="sxs-lookup"><span data-stu-id="d1fe9-110">LineToNodeY</span></span>  <br/> |
   
<span data-ttu-id="d1fe9-111">プログラムから、インデックスによって [LineToNodeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fe9-111">To get a reference to the LineToNodeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1fe9-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fe9-112">Section index:</span></span>  <br/> |<span data-ttu-id="d1fe9-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1fe9-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d1fe9-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fe9-114">Row index:</span></span>  <br/> |<span data-ttu-id="d1fe9-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d1fe9-115">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="d1fe9-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1fe9-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d1fe9-117">**visPLOLineToNodeY**</span><span class="sxs-lookup"><span data-stu-id="d1fe9-117">**visPLOLineToNodeY**</span></span> <br/> |
   

