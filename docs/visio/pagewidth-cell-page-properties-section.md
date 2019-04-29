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
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="aabcb-103">[PageWidth] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="aabcb-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="aabcb-104">印刷ページの幅を図面単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="aabcb-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aabcb-105">注釈</span><span class="sxs-lookup"><span data-stu-id="aabcb-105">Remarks</span></span>

<span data-ttu-id="aabcb-106">ページの幅は、[**ページ設定**] ダイアログボックス ([**デザイン**] タブで [**ページ設定**] 矢印をクリック) の [**ページサイズ**] タブで設定するか、またはマウスでページのサイズを手動で変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="aabcb-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="aabcb-107">これを行うには、CTRL キーを押しながらページの端をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="aabcb-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="aabcb-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="aabcb-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aabcb-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="aabcb-109">Cell name:</span></span>  <br/> |<span data-ttu-id="aabcb-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="aabcb-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="aabcb-111">プログラムから、インデックスによって [PageWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="aabcb-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aabcb-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="aabcb-112">Section index:</span></span>  <br/> |<span data-ttu-id="aabcb-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aabcb-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="aabcb-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="aabcb-114">Row index:</span></span>  <br/> |<span data-ttu-id="aabcb-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="aabcb-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="aabcb-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="aabcb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="aabcb-117">**vispagewidth**</span><span class="sxs-lookup"><span data-stu-id="aabcb-117">**visPageWidth**</span></span> <br/> |
   

