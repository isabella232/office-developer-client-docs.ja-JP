---
title: '[ShdwOffsetY] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: 図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806473"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="11341-103">[ShdwOffsetY] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="11341-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="11341-104">図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="11341-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11341-105">注釈</span><span class="sxs-lookup"><span data-stu-id="11341-105">Remarks</span></span>

<span data-ttu-id="11341-106">この設定は、[**ページ設定**] ダイアログ ボックスで ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="11341-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="11341-107">この値は、図面の縮尺に依存しません。</span><span class="sxs-lookup"><span data-stu-id="11341-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="11341-108">図面縮尺を変更して、影のオフセットは変わりません。</span><span class="sxs-lookup"><span data-stu-id="11341-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="11341-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwOffsetY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="11341-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11341-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="11341-110">Cell name:</span></span>  <br/> | <span data-ttu-id="11341-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="11341-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="11341-112">プログラムから、インデックスによって [ShdwOffsetY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="11341-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11341-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="11341-113">Section index:</span></span>  <br/> |<span data-ttu-id="11341-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11341-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11341-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="11341-115">Row index:</span></span>  <br/> |<span data-ttu-id="11341-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="11341-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="11341-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="11341-117">Cell index:</span></span>  <br/> |<span data-ttu-id="11341-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="11341-118">**visPageShdwOffsetY**</span></span> <br/> |
   

