---
title: '[LineJumpFactorY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: '[LineToLineY] セルの値を基準にして、ページ上にある垂直方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。'
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805721"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="c9e92-104">[LineJumpFactorY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="c9e92-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="c9e92-p102">[LineToLineY] セルの値を基準にして、ページ上にある垂直方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9e92-p102">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9e92-107">注釈</span><span class="sxs-lookup"><span data-stu-id="c9e92-107">Remarks</span></span>

<span data-ttu-id="c9e92-108">**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="c9e92-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="c9e92-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineJumpFactorY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c9e92-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9e92-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="c9e92-110">Cell name:</span></span>  <br/> |<span data-ttu-id="c9e92-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="c9e92-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="c9e92-112">プログラムから、インデックスによって [LineJumpFactorY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c9e92-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9e92-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e92-113">Section index:</span></span>  <br/> |<span data-ttu-id="c9e92-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9e92-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9e92-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e92-115">Row index:</span></span>  <br/> |<span data-ttu-id="c9e92-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c9e92-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="c9e92-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c9e92-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c9e92-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="c9e92-118">**visPLOJumpFactorY**</span></span> <br/> |
   

