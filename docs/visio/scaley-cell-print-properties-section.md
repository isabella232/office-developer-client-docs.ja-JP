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
description: プリンター ページの図面ページの倍率の割合を指定します。
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406991"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="df394-103">[ScaleY] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="df394-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="df394-104">プリンター ページの図面ページの倍率の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="df394-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df394-105">注釈</span><span class="sxs-lookup"><span data-stu-id="df394-105">Remarks</span></span>

<span data-ttu-id="df394-106">この値は、OnPage セルの値が FALSE の場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="df394-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="df394-107">ScaleX セルと ScaleY セルの値は常に同じです。これは、[ページセットアップ] ダイアログボックスの [印刷設定] タブの [調整] 設定の値に対応します ([デザイン] タブの [ページ設定] 矢印を **クリック** します)。 </span><span class="sxs-lookup"><span data-stu-id="df394-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="df394-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ScaleY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="df394-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df394-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="df394-109">Cell name:</span></span>  <br/> |<span data-ttu-id="df394-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="df394-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="df394-111">プログラムから、インデックスによって [ScaleY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="df394-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df394-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="df394-112">Section index:</span></span>  <br/> |<span data-ttu-id="df394-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df394-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="df394-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="df394-114">Row index:</span></span>  <br/> |<span data-ttu-id="df394-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="df394-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="df394-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="df394-116">Cell index:</span></span>  <br/> |<span data-ttu-id="df394-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="df394-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

