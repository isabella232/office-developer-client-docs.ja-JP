---
title: '[OnPage] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: 特定のプリンター ページ番号に図面を印刷するかどうかを示します。
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439605"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="9422b-103">[OnPage] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="9422b-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="9422b-104">特定のプリンター ページ番号に図面を印刷するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9422b-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="9422b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9422b-105">**Value**</span></span>|<span data-ttu-id="9422b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="9422b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9422b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9422b-107">TRUE</span></span>  <br/> |<span data-ttu-id="9422b-108">図面ページを定義済みのプリンター ページ数に合わせて指定します。</span><span class="sxs-lookup"><span data-stu-id="9422b-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="9422b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9422b-109">FALSE</span></span>  <br/> |<span data-ttu-id="9422b-110">プリンター ページを定義済みの図面ページ番号に合わせません。</span><span class="sxs-lookup"><span data-stu-id="9422b-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9422b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9422b-111">Remarks</span></span>

<span data-ttu-id="9422b-p101">[OnPage] セルが TRUE に設定されている場合は、[PagesX] セルおよび [PagesY] セルを使用して、図面に合うプリンター ページ番号が特定されます。[ScaleX] セルおよび [ScaleY] セル内の値は無視されます。これは "自動サイズ" 設定と見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="9422b-p101">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing. Values in the ScaleX and ScaleY cells are ignored. This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="9422b-115">この値は、[ページセットアップ] ダイアログ ボックスの [印刷設定] タブの [適合] オプションに対応します ([デザイン] タブの [ページ設定] 矢印 **をクリック** します)。 </span><span class="sxs-lookup"><span data-stu-id="9422b-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="9422b-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [OnPage] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9422b-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9422b-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9422b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9422b-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="9422b-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="9422b-119">プログラムから、インデックスによって [OnPage] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9422b-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9422b-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9422b-120">Section index:</span></span>  <br/> |<span data-ttu-id="9422b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9422b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9422b-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9422b-122">Row index:</span></span>  <br/> |<span data-ttu-id="9422b-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="9422b-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="9422b-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9422b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="9422b-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="9422b-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

