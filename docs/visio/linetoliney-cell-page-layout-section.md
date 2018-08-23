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
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="0b8c4-103">[LineToLineY] セル ([ページ レイアウト] セクション)</span><span class="sxs-lookup"><span data-stu-id="0b8c4-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="0b8c4-104">図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b8c4-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b8c4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0b8c4-105">Remarks</span></span>

<span data-ttu-id="0b8c4-p101">このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="0b8c4-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="0b8c4-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToLineY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0b8c4-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b8c4-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="0b8c4-109">Cell name:</span></span>  <br/> |<span data-ttu-id="0b8c4-110">[Linetoliney]</span><span class="sxs-lookup"><span data-stu-id="0b8c4-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="0b8c4-111">プログラムから、インデックスによって [LineToLineY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b8c4-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b8c4-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b8c4-112">Section index:</span></span>  <br/> |<span data-ttu-id="0b8c4-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b8c4-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0b8c4-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b8c4-114">Row index:</span></span>  <br/> |<span data-ttu-id="0b8c4-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0b8c4-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0b8c4-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b8c4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0b8c4-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="0b8c4-117">**visPLOLineToLineY**</span></span> <br/> |
   

