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
ms.openlocfilehash: aa6476eab9d5bcf7aab12235fd23f0f5675d6ad5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805709"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="15079-103">[LineToLineX] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="15079-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="15079-104">図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。</span><span class="sxs-lookup"><span data-stu-id="15079-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15079-105">注釈</span><span class="sxs-lookup"><span data-stu-id="15079-105">Remarks</span></span>

<span data-ttu-id="15079-106">**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="15079-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="15079-107">([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="15079-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="15079-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [linetolinex] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="15079-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15079-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="15079-109">Cell name:</span></span>  <br/> |<span data-ttu-id="15079-110">[Linetolinex]</span><span class="sxs-lookup"><span data-stu-id="15079-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="15079-111">プログラムから、インデックスによって [linetolinex] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="15079-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15079-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15079-112">Section index:</span></span>  <br/> |<span data-ttu-id="15079-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15079-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="15079-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15079-114">Row index:</span></span>  <br/> |<span data-ttu-id="15079-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="15079-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="15079-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15079-116">Cell index:</span></span>  <br/> |<span data-ttu-id="15079-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="15079-117">**visPLOLineToLineX**</span></span> <br/> |
   

