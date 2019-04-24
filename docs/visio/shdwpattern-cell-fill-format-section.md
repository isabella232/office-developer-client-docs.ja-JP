---
title: '[ShdwPattern] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: 図形の影の塗りつぶしパターンを指定します。
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349043"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="73fad-103">[ShdwPattern] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="73fad-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="73fad-104">図形の影の塗りつぶしパターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="73fad-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="73fad-105">**値**</span><span class="sxs-lookup"><span data-stu-id="73fad-105">**Value**</span></span>|<span data-ttu-id="73fad-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="73fad-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73fad-107">.0</span><span class="sxs-lookup"><span data-stu-id="73fad-107">0</span></span>  <br/> |<span data-ttu-id="73fad-108">なし (透明な塗りつぶし)</span><span class="sxs-lookup"><span data-stu-id="73fad-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="73fad-109">1-d</span><span class="sxs-lookup"><span data-stu-id="73fad-109">1</span></span>  <br/> |<span data-ttu-id="73fad-110">無地の前景色</span><span class="sxs-lookup"><span data-stu-id="73fad-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="73fad-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="73fad-111">2 - 40</span></span>  <br/> |<span data-ttu-id="73fad-112">さまざまなパターン</span><span class="sxs-lookup"><span data-stu-id="73fad-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73fad-113">解説</span><span class="sxs-lookup"><span data-stu-id="73fad-113">Remarks</span></span>

<span data-ttu-id="73fad-p101">塗りつぶしパターンを設定するには、パターンのコレクションのインデックスである 0 ～ 40 の数値を入力します。塗りつぶしパターンのコレクションは、[**塗りつぶし**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="73fad-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="73fad-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwPattern] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="73fad-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73fad-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="73fad-117">Cell name:</span></span>  <br/> |<span data-ttu-id="73fad-118">[shdwpattern]</span><span class="sxs-lookup"><span data-stu-id="73fad-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="73fad-119">プログラムから、インデックスによって [ShdwPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="73fad-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73fad-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="73fad-120">Section index:</span></span>  <br/> |<span data-ttu-id="73fad-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="73fad-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="73fad-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="73fad-122">Row index:</span></span>  <br/> |<span data-ttu-id="73fad-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="73fad-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="73fad-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="73fad-124">Cell index:</span></span>  <br/> |<span data-ttu-id="73fad-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="73fad-125">**visFillShdwPattern**</span></span> <br/> |
   

