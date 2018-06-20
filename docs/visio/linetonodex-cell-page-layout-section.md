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
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="a0fc5-103">[LineToNodeX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="a0fc5-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a0fc5-104">図面ページにあるすべてのコネクタと図形間の水平方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0fc5-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0fc5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a0fc5-105">Remarks</span></span>

<span data-ttu-id="a0fc5-106">**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0fc5-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="a0fc5-107">([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="a0fc5-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a0fc5-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineToNodeY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a0fc5-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0fc5-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="a0fc5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a0fc5-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="a0fc5-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="a0fc5-111">プログラムから、インデックスによって [LineToNodeX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0fc5-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0fc5-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0fc5-112">Section index:</span></span>  <br/> |<span data-ttu-id="a0fc5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0fc5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0fc5-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0fc5-114">Row index:</span></span>  <br/> |<span data-ttu-id="a0fc5-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a0fc5-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a0fc5-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0fc5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a0fc5-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="a0fc5-117">**visPLOLineToNodeX**</span></span> <br/> |
   

