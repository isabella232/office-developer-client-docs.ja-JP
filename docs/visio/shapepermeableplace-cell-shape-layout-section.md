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
description: レイアウトの構成] ダイアログ ボックス内の図形をレイアウトするとき、配置可能な図形を図形の上に配置できるかどうかを決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806395"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="ae2ca-103">[ShapePermeablePlace] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="ae2ca-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ae2ca-104">**レイアウトの構成**] ダイアログ ボックス内の図形をレイアウトするとき、配置可能な図形を図形の上に配置できるかどうかを決定する ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、**他のレイアウト オプションをクリックし、**).</span><span class="sxs-lookup"><span data-stu-id="ae2ca-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="ae2ca-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ae2ca-105">**Value**</span></span>|<span data-ttu-id="ae2ca-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae2ca-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae2ca-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ae2ca-107">TRUE</span></span>  <br/> |<span data-ttu-id="ae2ca-108">他図形をこの図形の上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="ae2ca-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="ae2ca-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ae2ca-109">FALSE</span></span>  <br/> |<span data-ttu-id="ae2ca-110">他図形をこの図形の上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="ae2ca-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae2ca-111">注釈</span><span class="sxs-lookup"><span data-stu-id="ae2ca-111">Remarks</span></span>

<span data-ttu-id="ae2ca-112">**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして).</span><span class="sxs-lookup"><span data-stu-id="ae2ca-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="ae2ca-113">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="ae2ca-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="ae2ca-114">取得する、[ShapePermeablePlace] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae2ca-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae2ca-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ae2ca-115">Cell name:</span></span>  <br/> |<span data-ttu-id="ae2ca-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="ae2ca-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="ae2ca-117">プログラムから、インデックスによって [ShapePermeablePlace] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae2ca-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae2ca-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae2ca-118">Section index:</span></span>  <br/> |<span data-ttu-id="ae2ca-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae2ca-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ae2ca-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae2ca-120">Row index:</span></span>  <br/> |<span data-ttu-id="ae2ca-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ae2ca-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="ae2ca-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae2ca-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ae2ca-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="ae2ca-123">**visSLOPermeablePlace**</span></span> <br/> |
   

