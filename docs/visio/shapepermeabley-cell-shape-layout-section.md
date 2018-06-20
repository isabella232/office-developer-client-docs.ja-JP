---
title: '[ShapePermeableY] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806392"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="efd65-103">[ShapePermeableY] セル ([Shape Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="efd65-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="efd65-104">コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="efd65-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="efd65-105">**値**</span><span class="sxs-lookup"><span data-stu-id="efd65-105">**Value**</span></span>|<span data-ttu-id="efd65-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="efd65-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efd65-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="efd65-107">TRUE</span></span>  <br/> |<span data-ttu-id="efd65-108">コネクタの接続経路は、配置可能な図形上を垂直方向に通過します。</span><span class="sxs-lookup"><span data-stu-id="efd65-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="efd65-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="efd65-109">FALSE</span></span>  <br/> |<span data-ttu-id="efd65-110">コネクタの接続経路は、配置可能な図形上を垂直方向に通過できません。</span><span class="sxs-lookup"><span data-stu-id="efd65-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efd65-111">注釈</span><span class="sxs-lookup"><span data-stu-id="efd65-111">Remarks</span></span>

<span data-ttu-id="efd65-112">**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして).</span><span class="sxs-lookup"><span data-stu-id="efd65-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="efd65-113">Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。</span><span class="sxs-lookup"><span data-stu-id="efd65-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="efd65-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapePermeableY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="efd65-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efd65-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="efd65-115">Cell name:</span></span>  <br/> |<span data-ttu-id="efd65-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="efd65-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="efd65-117">プログラムから、インデックスによって [ShapePermeableY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="efd65-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efd65-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd65-118">Section index:</span></span>  <br/> |<span data-ttu-id="efd65-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="efd65-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="efd65-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd65-120">Row index:</span></span>  <br/> |<span data-ttu-id="efd65-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="efd65-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="efd65-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="efd65-122">Cell index:</span></span>  <br/> |<span data-ttu-id="efd65-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="efd65-123">**visSLOPermY**</span></span> <br/> |
   

