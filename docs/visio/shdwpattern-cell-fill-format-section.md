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
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="ff0ab-103">[ShdwPattern] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="ff0ab-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="ff0ab-104">図形の影の塗りつぶしパターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff0ab-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="ff0ab-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ff0ab-105">**Value**</span></span>|<span data-ttu-id="ff0ab-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ff0ab-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff0ab-107">0</span><span class="sxs-lookup"><span data-stu-id="ff0ab-107">0</span></span>  <br/> |<span data-ttu-id="ff0ab-108">なし (透明な塗りつぶし)</span><span class="sxs-lookup"><span data-stu-id="ff0ab-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="ff0ab-109">1</span><span class="sxs-lookup"><span data-stu-id="ff0ab-109">1</span></span>  <br/> |<span data-ttu-id="ff0ab-110">無地の前景色</span><span class="sxs-lookup"><span data-stu-id="ff0ab-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="ff0ab-111">2-40</span><span class="sxs-lookup"><span data-stu-id="ff0ab-111">2 - 40</span></span>  <br/> |<span data-ttu-id="ff0ab-112">さまざまなパターン</span><span class="sxs-lookup"><span data-stu-id="ff0ab-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff0ab-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ff0ab-113">Remarks</span></span>

<span data-ttu-id="ff0ab-114">塗りつぶしのパターンを設定するには、番号を入力、0 から 40、パターンのコレクションのインデックスとなっています。</span><span class="sxs-lookup"><span data-stu-id="ff0ab-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="ff0ab-115">塗りつぶしパターンのコレクションを表示するには、[**塗りつぶし**] ダイアログ ボックスで ([**ホーム**] タブの [**図形**] グループで、**塗りつぶし**] をクリックし、[**オートフィル オプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="ff0ab-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="ff0ab-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwPattern] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ff0ab-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff0ab-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ff0ab-117">Cell name:</span></span>  <br/> |<span data-ttu-id="ff0ab-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="ff0ab-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="ff0ab-119">プログラムから、インデックスによって [ShdwPattern] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff0ab-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff0ab-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff0ab-120">Section index:</span></span>  <br/> |<span data-ttu-id="ff0ab-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff0ab-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ff0ab-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff0ab-122">Row index:</span></span>  <br/> |<span data-ttu-id="ff0ab-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ff0ab-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="ff0ab-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff0ab-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ff0ab-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="ff0ab-125">**visFillShdwPattern**</span></span> <br/> |
   

