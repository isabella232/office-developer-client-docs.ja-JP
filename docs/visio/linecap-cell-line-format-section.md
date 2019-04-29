---
title: '[LineCap] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: 線の端点を丸、四角形、または拡張のどれにするかを指定します。
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425200"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="dc58b-103">[LineCap] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="dc58b-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="dc58b-104">線の端点を丸、四角形、または拡張のどれにするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc58b-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="dc58b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dc58b-105">**Value**</span></span>|<span data-ttu-id="dc58b-106">**線の端点の形**</span><span class="sxs-lookup"><span data-stu-id="dc58b-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc58b-107">.0</span><span class="sxs-lookup"><span data-stu-id="dc58b-107">0</span></span>  <br/> |<span data-ttu-id="dc58b-108">端数</span><span class="sxs-lookup"><span data-stu-id="dc58b-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="dc58b-109">1 </span><span class="sxs-lookup"><span data-stu-id="dc58b-109">1</span></span>  <br/> |<span data-ttu-id="dc58b-110">四角</span><span class="sxs-lookup"><span data-stu-id="dc58b-110">Square</span></span>  <br/> |
|<span data-ttu-id="dc58b-111">2 </span><span class="sxs-lookup"><span data-stu-id="dc58b-111">2</span></span>  <br/> |<span data-ttu-id="dc58b-112">拡張</span><span class="sxs-lookup"><span data-stu-id="dc58b-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc58b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="dc58b-113">Remarks</span></span>

<span data-ttu-id="dc58b-114">このセルの値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**] をポイントして、[**その他の矢印**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="dc58b-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="dc58b-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineCap] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc58b-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc58b-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="dc58b-116">Cell name:</span></span>  <br/> |<span data-ttu-id="dc58b-117">[linecap]</span><span class="sxs-lookup"><span data-stu-id="dc58b-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="dc58b-118">プログラムから、インデックスによって [LineCap] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc58b-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc58b-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc58b-119">Section index:</span></span>  <br/> |<span data-ttu-id="dc58b-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dc58b-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dc58b-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc58b-121">Row index:</span></span>  <br/> |<span data-ttu-id="dc58b-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="dc58b-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="dc58b-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dc58b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="dc58b-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="dc58b-124">**visLineEndCap**</span></span> <br/> |
   

