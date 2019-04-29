---
title: '[ShapePermeableX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409476"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="eefbc-103">[ShapePermeableX] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="eefbc-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="eefbc-104">コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="eefbc-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="eefbc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eefbc-105">**Value**</span></span>|<span data-ttu-id="eefbc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eefbc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eefbc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eefbc-107">TRUE</span></span>  <br/> |<span data-ttu-id="eefbc-108">コネクタの接続経路は、配置可能な図形上を水平方向に通過します。</span><span class="sxs-lookup"><span data-stu-id="eefbc-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="eefbc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eefbc-109">FALSE</span></span>  <br/> |<span data-ttu-id="eefbc-110">コネクタの接続経路は、配置可能な図形上を水平方向に通過できません。</span><span class="sxs-lookup"><span data-stu-id="eefbc-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eefbc-111">注釈</span><span class="sxs-lookup"><span data-stu-id="eefbc-111">Remarks</span></span>

<span data-ttu-id="eefbc-112">このセルの値は、[**基本動作**] ダイアログボックスの [**配置**] タブで設定することもできます (図形が選択されている場合)、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、[**配置**] タブをクリックします。).</span><span class="sxs-lookup"><span data-stu-id="eefbc-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="eefbc-113">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="eefbc-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="eefbc-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePermeableX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eefbc-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eefbc-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="eefbc-115">Cell name:</span></span>  <br/> |<span data-ttu-id="eefbc-116">[shapepermeablex]</span><span class="sxs-lookup"><span data-stu-id="eefbc-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="eefbc-117">プログラムから、インデックスによって [ShapePermeableX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eefbc-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eefbc-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eefbc-118">Section index:</span></span>  <br/> |<span data-ttu-id="eefbc-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eefbc-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="eefbc-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eefbc-120">Row index:</span></span>  <br/> |<span data-ttu-id="eefbc-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="eefbc-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="eefbc-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eefbc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="eefbc-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="eefbc-123">**visSLOPermX**</span></span> <br/> |
   

