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
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805703"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="37b12-103">[LineCap] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="37b12-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="37b12-104">線の端点を丸、四角形、または拡張のどれにするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="37b12-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="37b12-105">**値**</span><span class="sxs-lookup"><span data-stu-id="37b12-105">**Value**</span></span>|<span data-ttu-id="37b12-106">**線の端点の形**</span><span class="sxs-lookup"><span data-stu-id="37b12-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37b12-107">0</span><span class="sxs-lookup"><span data-stu-id="37b12-107">0</span></span>  <br/> |<span data-ttu-id="37b12-108">丸</span><span class="sxs-lookup"><span data-stu-id="37b12-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="37b12-109">1</span><span class="sxs-lookup"><span data-stu-id="37b12-109">1</span></span>  <br/> |<span data-ttu-id="37b12-110">四角形</span><span class="sxs-lookup"><span data-stu-id="37b12-110">Square</span></span>  <br/> |
|<span data-ttu-id="37b12-111">2</span><span class="sxs-lookup"><span data-stu-id="37b12-111">2</span></span>  <br/> |<span data-ttu-id="37b12-112">拡張</span><span class="sxs-lookup"><span data-stu-id="37b12-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37b12-113">注釈</span><span class="sxs-lookup"><span data-stu-id="37b12-113">Remarks</span></span>

<span data-ttu-id="37b12-114">このセルの値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**] をポイントして、[**その他の矢印**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="37b12-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="37b12-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineCap] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="37b12-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37b12-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="37b12-116">Cell name:</span></span>  <br/> |<span data-ttu-id="37b12-117">[Linecap]</span><span class="sxs-lookup"><span data-stu-id="37b12-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="37b12-118">プログラムから、インデックスによって [LineCap] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="37b12-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37b12-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37b12-119">Section index:</span></span>  <br/> |<span data-ttu-id="37b12-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37b12-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37b12-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37b12-121">Row index:</span></span>  <br/> |<span data-ttu-id="37b12-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="37b12-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="37b12-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37b12-123">Cell index:</span></span>  <br/> |<span data-ttu-id="37b12-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="37b12-124">**visLineEndCap**</span></span> <br/> |
   

