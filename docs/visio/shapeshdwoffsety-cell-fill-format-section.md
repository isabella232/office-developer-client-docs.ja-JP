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
# <a name="shapeshdwoffsety-cell-fill-format-section"></a><span data-ttu-id="7d422-103">[ShapeShdwOffsetY] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="7d422-103">ShapeShdwOffsetY Cell (Fill Format Section)</span></span>

<span data-ttu-id="7d422-104">図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="7d422-104">Determines the distance in page units that a shape's shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d422-105">注釈</span><span class="sxs-lookup"><span data-stu-id="7d422-105">Remarks</span></span>

<span data-ttu-id="7d422-106">この値は、[**影**] ダイアログ ボックスで設定する**Y のオフセット**値に対応する ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="7d422-106">This value corresponds to the value in the **Y Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="7d422-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwOffsetY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7d422-107">To get a reference to the ShapeShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d422-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7d422-108">Cell name:</span></span>  <br/> | <span data-ttu-id="7d422-109">ShapeShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="7d422-109">ShapeShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="7d422-110">プログラムから、インデックスによって [ShapeShdwOffsetY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d422-110">To get a reference to the ShapeShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d422-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d422-111">Section index:</span></span>  <br/> |<span data-ttu-id="7d422-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d422-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7d422-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d422-113">Row index:</span></span>  <br/> |<span data-ttu-id="7d422-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="7d422-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="7d422-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7d422-115">Cell index:</span></span>  <br/> |<span data-ttu-id="7d422-116">**visFillShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="7d422-116">**visFillShdwOffsetY**</span></span> <br/> |
   

