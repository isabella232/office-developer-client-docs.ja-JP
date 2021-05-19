---
title: '[LineJumpFactorX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: '[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。'
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424995"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="fe57a-104">[LineJumpFactorX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="fe57a-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="fe57a-p102">[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fe57a-p102">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe57a-107">注釈</span><span class="sxs-lookup"><span data-stu-id="fe57a-107">Remarks</span></span>

<span data-ttu-id="fe57a-108">このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="fe57a-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="fe57a-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineJumpFactorX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe57a-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe57a-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="fe57a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="fe57a-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="fe57a-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="fe57a-112">プログラムから、インデックスによって [LineJumpFactorX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe57a-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe57a-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe57a-113">Section index:</span></span>  <br/> |<span data-ttu-id="fe57a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe57a-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fe57a-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe57a-115">Row index:</span></span>  <br/> |<span data-ttu-id="fe57a-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="fe57a-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="fe57a-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe57a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fe57a-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="fe57a-118">**visPLOJumpFactorX**</span></span> <br/> |
   

