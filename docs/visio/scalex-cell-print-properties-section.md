---
title: '[ScaleX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: '[プリンター] ページで、図面ページの表示倍率の割合を指定します。'
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806351"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="fb609-103">[ScaleX] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="fb609-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="fb609-104">[プリンター] ページで、図面ページの表示倍率の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb609-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb609-105">備考</span><span class="sxs-lookup"><span data-stu-id="fb609-105">Remarks</span></span>

<span data-ttu-id="fb609-106">[Onpage] セルの値が FALSE である場合にのみ、この値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb609-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="fb609-107">ScaleX と ScaleY のセルは、同じ値が、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブの **[拡大/縮小**設定の値に対応して常にある ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。</span><span class="sxs-lookup"><span data-stu-id="fb609-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="fb609-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [scalex] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="fb609-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb609-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fb609-109">Cell name:</span></span>  <br/> |<span data-ttu-id="fb609-110">[Scalex]</span><span class="sxs-lookup"><span data-stu-id="fb609-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="fb609-111">プログラムから、インデックスによって [scalex] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb609-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb609-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb609-112">Section index:</span></span>  <br/> |<span data-ttu-id="fb609-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb609-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fb609-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb609-114">Row index:</span></span>  <br/> |<span data-ttu-id="fb609-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="fb609-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="fb609-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb609-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fb609-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="fb609-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

