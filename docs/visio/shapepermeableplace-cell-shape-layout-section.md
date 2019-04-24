---
title: '[ShapePermeablePlace] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: '[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357058"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="6b7c9-103">[ShapePermeablePlace] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="6b7c9-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="6b7c9-104">[**レイアウトの構成**] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="6b7c9-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6b7c9-105">**Value**</span></span>|<span data-ttu-id="6b7c9-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b7c9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b7c9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b7c9-107">TRUE</span></span>  <br/> |<span data-ttu-id="6b7c9-108">他図形をこの図形の上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="6b7c9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6b7c9-109">FALSE</span></span>  <br/> |<span data-ttu-id="6b7c9-110">他図形をこの図形の上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b7c9-111">解説</span><span class="sxs-lookup"><span data-stu-id="6b7c9-111">Remarks</span></span>

<span data-ttu-id="6b7c9-112">このセルの値は、[**基本動作**] ダイアログボックスの [**配置**] タブで設定することもできます (図形が選択されている場合)、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、[**配置**] タブをクリックします。).</span><span class="sxs-lookup"><span data-stu-id="6b7c9-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="6b7c9-113">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="6b7c9-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePermeablePlace] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b7c9-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6b7c9-115">Cell name:</span></span>  <br/> |<span data-ttu-id="6b7c9-116">[shapepermeableplace]</span><span class="sxs-lookup"><span data-stu-id="6b7c9-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="6b7c9-117">プログラムから、インデックスによって [ShapePermeablePlace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b7c9-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b7c9-118">Section index:</span></span>  <br/> |<span data-ttu-id="6b7c9-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b7c9-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6b7c9-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b7c9-120">Row index:</span></span>  <br/> |<span data-ttu-id="6b7c9-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="6b7c9-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="6b7c9-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6b7c9-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6b7c9-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="6b7c9-123">**visSLOPermeablePlace**</span></span> <br/> |
   

