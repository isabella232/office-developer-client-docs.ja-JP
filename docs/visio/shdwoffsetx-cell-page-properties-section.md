---
title: '[ShdwOffsetX] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: 図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806456"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="bca64-103">[ShdwOffsetX] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="bca64-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="bca64-104">図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="bca64-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bca64-105">注釈</span><span class="sxs-lookup"><span data-stu-id="bca64-105">Remarks</span></span>

<span data-ttu-id="bca64-106">この設定は、[**ページ設定**] ダイアログ ボックスで ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="bca64-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="bca64-107">この値は、図面の縮尺に依存しません。</span><span class="sxs-lookup"><span data-stu-id="bca64-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="bca64-108">図面縮尺を変更して、影のオフセットは変わりません。</span><span class="sxs-lookup"><span data-stu-id="bca64-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="bca64-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwOffsetX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bca64-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bca64-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bca64-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bca64-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="bca64-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="bca64-112">プログラムから、インデックスによって [ShdwOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bca64-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bca64-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bca64-113">Section index:</span></span>  <br/> |<span data-ttu-id="bca64-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bca64-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bca64-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bca64-115">Row index:</span></span>  <br/> |<span data-ttu-id="bca64-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bca64-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="bca64-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bca64-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bca64-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="bca64-118">**visPageShdwOffsetX**</span></span> <br/> |
   

