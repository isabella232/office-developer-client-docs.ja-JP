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
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806455"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="15f28-103">[ShdwPattern] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="15f28-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="15f28-104">図形の影の塗りつぶしパターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="15f28-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="15f28-105">**値**</span><span class="sxs-lookup"><span data-stu-id="15f28-105">**Value**</span></span>|<span data-ttu-id="15f28-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="15f28-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15f28-107">0</span><span class="sxs-lookup"><span data-stu-id="15f28-107">0</span></span>  <br/> |<span data-ttu-id="15f28-108">なし (透明な塗りつぶし)</span><span class="sxs-lookup"><span data-stu-id="15f28-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="15f28-109">1</span><span class="sxs-lookup"><span data-stu-id="15f28-109">1</span></span>  <br/> |<span data-ttu-id="15f28-110">無地の前景色</span><span class="sxs-lookup"><span data-stu-id="15f28-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="15f28-111">2-40</span><span class="sxs-lookup"><span data-stu-id="15f28-111">2 - 40</span></span>  <br/> |<span data-ttu-id="15f28-112">さまざまなパターン</span><span class="sxs-lookup"><span data-stu-id="15f28-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15f28-113">注釈</span><span class="sxs-lookup"><span data-stu-id="15f28-113">Remarks</span></span>

<span data-ttu-id="15f28-p101">塗りつぶしパターンを設定するには、パターンのコレクションのインデックスである 0 ～ 40 の数値を入力します。塗りつぶしパターンのコレクションは、[**塗りつぶし**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="15f28-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="15f28-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwPattern] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="15f28-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15f28-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="15f28-117">Cell name:</span></span>  <br/> |<span data-ttu-id="15f28-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="15f28-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="15f28-119">プログラムから、インデックスによって [ShdwPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="15f28-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15f28-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15f28-120">Section index:</span></span>  <br/> |<span data-ttu-id="15f28-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15f28-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="15f28-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15f28-122">Row index:</span></span>  <br/> |<span data-ttu-id="15f28-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="15f28-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="15f28-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15f28-124">Cell index:</span></span>  <br/> |<span data-ttu-id="15f28-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="15f28-125">**visFillShdwPattern**</span></span> <br/> |
   

