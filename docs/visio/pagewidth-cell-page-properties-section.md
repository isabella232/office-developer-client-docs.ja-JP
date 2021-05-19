---
title: '[PageWidth] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: 印刷ページの幅を図面単位で指定します。
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434271"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="1039a-103">[PageWidth] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="1039a-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="1039a-104">印刷ページの幅を図面単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="1039a-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1039a-105">注釈</span><span class="sxs-lookup"><span data-stu-id="1039a-105">Remarks</span></span>

<span data-ttu-id="1039a-106">[ページ設定] ダイアログ ボックスの[ページ サイズ] タブ ([デザイン] タブの[ページ設定] 矢印をクリック) でページ幅を設定したり、マウスを使用して手動でページのサイズを変更したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1039a-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="1039a-107">これを行うには、Ctrl キーを押しながらページの端をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="1039a-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="1039a-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1039a-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1039a-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="1039a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="1039a-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="1039a-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="1039a-111">プログラムから、インデックスによって [PageWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1039a-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1039a-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1039a-112">Section index:</span></span>  <br/> |<span data-ttu-id="1039a-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1039a-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1039a-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1039a-114">Row index:</span></span>  <br/> |<span data-ttu-id="1039a-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="1039a-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="1039a-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1039a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1039a-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="1039a-117">**visPageWidth**</span></span> <br/> |
   

