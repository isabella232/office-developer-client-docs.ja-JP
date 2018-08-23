---
title: '[EndArrow] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: 線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805307"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="0a693-103">[EndArrow] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="0a693-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="0a693-104">線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0a693-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="0a693-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0a693-105">**Value**</span></span>|<span data-ttu-id="0a693-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a693-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a693-107">0</span><span class="sxs-lookup"><span data-stu-id="0a693-107">0</span></span>  <br/> |<span data-ttu-id="0a693-108">矢印を付けません。</span><span class="sxs-lookup"><span data-stu-id="0a693-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="0a693-109">1-45</span><span class="sxs-lookup"><span data-stu-id="0a693-109">1 - 45</span></span>  <br/> |<span data-ttu-id="0a693-110">さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="0a693-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a693-111">注釈</span><span class="sxs-lookup"><span data-stu-id="0a693-111">Remarks</span></span>

<span data-ttu-id="0a693-112">この値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**]、[**その他の矢印**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="0a693-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="0a693-113">EndArrowSize] セルにある矢印のサイズが設定されています。</span><span class="sxs-lookup"><span data-stu-id="0a693-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="0a693-114">USE 関数を使用して、このセルにユーザー設定の線の端を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0a693-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="0a693-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndArrow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0a693-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a693-116">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0a693-116">Cell name:</span></span>  <br/> |<span data-ttu-id="0a693-117">[Endarrow]</span><span class="sxs-lookup"><span data-stu-id="0a693-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="0a693-118">プログラムから、インデックスによって [EndArrow] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a693-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a693-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a693-119">Section index:</span></span>  <br/> |<span data-ttu-id="0a693-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a693-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0a693-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a693-121">Row index:</span></span>  <br/> |<span data-ttu-id="0a693-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="0a693-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="0a693-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a693-123">Cell index:</span></span>  <br/> |<span data-ttu-id="0a693-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="0a693-124">**visLineEndArrow**</span></span> <br/> |
   

