---
title: '[LineToLineY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: 図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805714"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="94f15-103">[LineToLineY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="94f15-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="94f15-104">図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="94f15-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94f15-105">注釈</span><span class="sxs-lookup"><span data-stu-id="94f15-105">Remarks</span></span>

<span data-ttu-id="94f15-106">**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="94f15-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="94f15-107">([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="94f15-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="94f15-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [linetoliney] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="94f15-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94f15-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="94f15-109">Cell name:</span></span>  <br/> |<span data-ttu-id="94f15-110">[Linetoliney]</span><span class="sxs-lookup"><span data-stu-id="94f15-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="94f15-111">プログラムから、インデックスによって [linetoliney] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="94f15-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94f15-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="94f15-112">Section index:</span></span>  <br/> |<span data-ttu-id="94f15-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94f15-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="94f15-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="94f15-114">Row index:</span></span>  <br/> |<span data-ttu-id="94f15-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="94f15-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="94f15-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="94f15-116">Cell index:</span></span>  <br/> |<span data-ttu-id="94f15-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="94f15-117">**visPLOLineToLineY**</span></span> <br/> |
   

