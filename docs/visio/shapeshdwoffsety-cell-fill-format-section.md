---
title: '[ShapeShdwOffsetY] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60077
localization_priority: Normal
ms.assetid: ef200f41-7b69-1291-f9df-a7035239a033
description: 図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 669e15fd1badf9cf76decb117a9c4fb91e731271
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806419"
---
# <a name="shapeshdwoffsety-cell-fill-format-section"></a><span data-ttu-id="cce9e-103">[ShapeShdwOffsetY] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="cce9e-103">ShapeShdwOffsetY Cell (Fill Format Section)</span></span>

<span data-ttu-id="cce9e-104">図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="cce9e-104">Determines the distance in page units that a shape's shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cce9e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="cce9e-105">Remarks</span></span>

<span data-ttu-id="cce9e-106">この値は、[**影**] ダイアログ ボックスの [**Y オフセット**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="cce9e-106">This value corresponds to the value in the **Y Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="cce9e-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwOffsetY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cce9e-107">To get a reference to the ShapeShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cce9e-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="cce9e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cce9e-109">ShapeShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="cce9e-109">ShapeShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="cce9e-110">プログラムから、インデックスによって [ShapeShdwOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cce9e-110">To get a reference to the ShapeShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cce9e-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cce9e-111">Section index:</span></span>  <br/> |<span data-ttu-id="cce9e-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cce9e-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cce9e-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cce9e-113">Row index:</span></span>  <br/> |<span data-ttu-id="cce9e-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="cce9e-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="cce9e-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cce9e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cce9e-116">**visFillShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="cce9e-116">**visFillShdwOffsetY**</span></span> <br/> |
   

