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
description: 印刷ページの図面ページの倍率をパーセントで指定します。
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410211"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="bc6fa-103">[ScaleX] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="bc6fa-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="bc6fa-104">印刷ページの図面ページの倍率をパーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="bc6fa-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc6fa-105">注釈</span><span class="sxs-lookup"><span data-stu-id="bc6fa-105">Remarks</span></span>

<span data-ttu-id="bc6fa-106">この値は、OnPage セルの値が FALSE の場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc6fa-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="bc6fa-107">ScaleX および ScaleY セルの値は常に同じで、[**ページ設定**] ダイアログボックス\*\*\*\* ([**デザイン**] タブの [**ページ設定**] 矢印をクリック) の [**印刷設定**] タブの [設定] に設定されている値に対応しています。</span><span class="sxs-lookup"><span data-stu-id="bc6fa-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="bc6fa-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ScaleX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc6fa-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc6fa-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bc6fa-109">Cell name:</span></span>  <br/> |<span data-ttu-id="bc6fa-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="bc6fa-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="bc6fa-111">プログラムから、インデックスによって [ScaleX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc6fa-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc6fa-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bc6fa-112">Section index:</span></span>  <br/> |<span data-ttu-id="bc6fa-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bc6fa-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bc6fa-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bc6fa-114">Row index:</span></span>  <br/> |<span data-ttu-id="bc6fa-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="bc6fa-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="bc6fa-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bc6fa-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bc6fa-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="bc6fa-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

