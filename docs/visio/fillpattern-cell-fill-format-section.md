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
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="b3871-104">[FillPattern] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="b3871-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="b3871-p102">図形の塗りつぶしのパターンを指定します。ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3871-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="b3871-107">**値**</span><span class="sxs-lookup"><span data-stu-id="b3871-107">**Value**</span></span>|<span data-ttu-id="b3871-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3871-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3871-109">0</span><span class="sxs-lookup"><span data-stu-id="b3871-109">0</span></span>  <br/> |<span data-ttu-id="b3871-110">なし (透明な塗りつぶし)。</span><span class="sxs-lookup"><span data-stu-id="b3871-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="b3871-111">1</span><span class="sxs-lookup"><span data-stu-id="b3871-111">1</span></span>  <br/> |<span data-ttu-id="b3871-112">前景の色。</span><span class="sxs-lookup"><span data-stu-id="b3871-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="b3871-113">2-40</span><span class="sxs-lookup"><span data-stu-id="b3871-113">2 - 40</span></span>  <br/> |<span data-ttu-id="b3871-114">さまざまな塗りつぶしのパターン、[**塗りつぶし**] ダイアログ ボックス内のエントリのインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3871-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3871-115">備考</span><span class="sxs-lookup"><span data-stu-id="b3871-115">Remarks</span></span>

<span data-ttu-id="b3871-116">[**塗りつぶし**] ダイアログ ボックスを使用してこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックし、[**オートフィル オプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b3871-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="b3871-117">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[FillPattern] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="b3871-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3871-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="b3871-118">Cell name:</span></span>  <br/> |<span data-ttu-id="b3871-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="b3871-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="b3871-120">プログラムから、インデックスによって [FillPattern] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3871-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3871-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3871-121">Section index:</span></span>  <br/> |<span data-ttu-id="b3871-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3871-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b3871-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3871-123">Row index:</span></span>  <br/> |<span data-ttu-id="b3871-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="b3871-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="b3871-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3871-125">Cell index:</span></span>  <br/> |<span data-ttu-id="b3871-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="b3871-126">**visFillPattern**</span></span> <br/> |
   

