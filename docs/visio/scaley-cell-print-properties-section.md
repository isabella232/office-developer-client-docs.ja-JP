---
title: '[ScaleY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: '[プリンター] ページで、図面ページの表示倍率の割合を指定します。'
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806347"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="d64ca-103">[ScaleY] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="d64ca-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="d64ca-104">[プリンター] ページで、図面ページの表示倍率の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="d64ca-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d64ca-105">備考</span><span class="sxs-lookup"><span data-stu-id="d64ca-105">Remarks</span></span>

<span data-ttu-id="d64ca-106">[Onpage] セルの値が FALSE である場合にのみ、この値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d64ca-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="d64ca-107">ScaleX と ScaleY のセルは、同じ値が、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブの **[拡大/縮小**設定の値に対応して常にある ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="d64ca-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="d64ca-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって scaley] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d64ca-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d64ca-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d64ca-109">Cell name:</span></span>  <br/> |<span data-ttu-id="d64ca-110">Scaley]</span><span class="sxs-lookup"><span data-stu-id="d64ca-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="d64ca-111">プログラムから、インデックスによって [scaley] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d64ca-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d64ca-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d64ca-112">Section index:</span></span>  <br/> |<span data-ttu-id="d64ca-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d64ca-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d64ca-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d64ca-114">Row index:</span></span>  <br/> |<span data-ttu-id="d64ca-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d64ca-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="d64ca-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d64ca-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d64ca-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="d64ca-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

