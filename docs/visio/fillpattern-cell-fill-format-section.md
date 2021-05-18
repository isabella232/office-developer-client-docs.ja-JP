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
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422930"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="f3294-104">[FillPattern] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="f3294-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="f3294-p102">図形の塗りつぶしのパターンを指定します。ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3294-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="f3294-107">**値**</span><span class="sxs-lookup"><span data-stu-id="f3294-107">**Value**</span></span>|<span data-ttu-id="f3294-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="f3294-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3294-109">0</span><span class="sxs-lookup"><span data-stu-id="f3294-109">0</span></span>  <br/> |<span data-ttu-id="f3294-110">なし (透明な塗りつぶし)。</span><span class="sxs-lookup"><span data-stu-id="f3294-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="f3294-111">1</span><span class="sxs-lookup"><span data-stu-id="f3294-111">1</span></span>  <br/> |<span data-ttu-id="f3294-112">前景の色。</span><span class="sxs-lookup"><span data-stu-id="f3294-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="f3294-113">2 ～ 40</span><span class="sxs-lookup"><span data-stu-id="f3294-113">2 - 40</span></span>  <br/> |<span data-ttu-id="f3294-114">さまざまな塗りつぶしのパターン。入力した値は [**塗りつぶし**] ダイアログ ボックスに表示されるインデックス付きエントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="f3294-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3294-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f3294-115">Remarks</span></span>

<span data-ttu-id="f3294-116">この値は、[**塗りつぶし**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] クリックして、[**塗りつぶしのオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="f3294-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="f3294-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillPattern] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3294-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3294-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="f3294-118">Cell name:</span></span>  <br/> |<span data-ttu-id="f3294-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="f3294-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="f3294-120">プログラムから、インデックスによって [FillPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3294-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3294-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f3294-121">Section index:</span></span>  <br/> |<span data-ttu-id="f3294-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3294-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f3294-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f3294-123">Row index:</span></span>  <br/> |<span data-ttu-id="f3294-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f3294-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="f3294-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f3294-125">Cell index:</span></span>  <br/> |<span data-ttu-id="f3294-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="f3294-126">**visFillPattern**</span></span> <br/> |
   

