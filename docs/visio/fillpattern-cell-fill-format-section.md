---
title: '[FillPattern] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: 図形の塗りつぶしのパターンを指定します。ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805388"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="a8beb-104">[FillPattern] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="a8beb-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="a8beb-p102">図形の塗りつぶしのパターンを指定します。ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="a8beb-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="a8beb-107">**値**</span><span class="sxs-lookup"><span data-stu-id="a8beb-107">**Value**</span></span>|<span data-ttu-id="a8beb-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8beb-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8beb-109">0</span><span class="sxs-lookup"><span data-stu-id="a8beb-109">0</span></span>  <br/> |<span data-ttu-id="a8beb-110">なし (透明な塗りつぶし)。</span><span class="sxs-lookup"><span data-stu-id="a8beb-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="a8beb-111">1</span><span class="sxs-lookup"><span data-stu-id="a8beb-111">1</span></span>  <br/> |<span data-ttu-id="a8beb-112">前景の色。</span><span class="sxs-lookup"><span data-stu-id="a8beb-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="a8beb-113">2-40</span><span class="sxs-lookup"><span data-stu-id="a8beb-113">2 - 40</span></span>  <br/> |<span data-ttu-id="a8beb-114">さまざまな塗りつぶしのパターン。入力した値は [**塗りつぶし**] ダイアログ ボックスに表示されるインデックス付きエントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="a8beb-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8beb-115">注釈</span><span class="sxs-lookup"><span data-stu-id="a8beb-115">Remarks</span></span>

<span data-ttu-id="a8beb-116">この値は、[**塗りつぶし**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] クリックして、[**塗りつぶしのオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a8beb-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="a8beb-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillPattern] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a8beb-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8beb-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="a8beb-118">Cell name:</span></span>  <br/> |<span data-ttu-id="a8beb-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="a8beb-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="a8beb-120">プログラムから、インデックスによって [FillPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8beb-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8beb-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8beb-121">Section index:</span></span>  <br/> |<span data-ttu-id="a8beb-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8beb-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a8beb-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8beb-123">Row index:</span></span>  <br/> |<span data-ttu-id="a8beb-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="a8beb-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="a8beb-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a8beb-125">Cell index:</span></span>  <br/> |<span data-ttu-id="a8beb-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="a8beb-126">**visFillPattern**</span></span> <br/> |
   

