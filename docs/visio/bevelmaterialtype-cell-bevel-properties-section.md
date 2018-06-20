---
title: '[BevelMaterialType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: 傾斜面で構成する材料のタイプを決定します。
ms.openlocfilehash: cd4ab223754ffcf7f46478cbc65faff373a3d692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804836"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a><span data-ttu-id="97656-103">[BevelMaterialType] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="97656-103">BevelMaterialType Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="97656-104">傾斜面で構成する材料のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="97656-104">Determines the type of material the bevel is composed of.</span></span> 
  
|<span data-ttu-id="97656-105">**説明**</span><span class="sxs-lookup"><span data-stu-id="97656-105">**Description**</span></span>|<span data-ttu-id="97656-106">**値**</span><span class="sxs-lookup"><span data-stu-id="97656-106">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97656-107">0</span><span class="sxs-lookup"><span data-stu-id="97656-107">0</span></span>  <br/> |<span data-ttu-id="97656-108">しない特殊な素材</span><span class="sxs-lookup"><span data-stu-id="97656-108">No special material</span></span>  <br/> |
|<span data-ttu-id="97656-109">1</span><span class="sxs-lookup"><span data-stu-id="97656-109">1</span></span>  <br/> |<span data-ttu-id="97656-110">つや消し</span><span class="sxs-lookup"><span data-stu-id="97656-110">Matte</span></span>  <br/> |
|<span data-ttu-id="97656-111">2</span><span class="sxs-lookup"><span data-stu-id="97656-111">2</span></span>  <br/> |<span data-ttu-id="97656-112">つや消し (明るめ)</span><span class="sxs-lookup"><span data-stu-id="97656-112">Warm Matte</span></span>  <br/> |
|<span data-ttu-id="97656-113">3</span><span class="sxs-lookup"><span data-stu-id="97656-113">3</span></span>  <br/> |<span data-ttu-id="97656-114">プラスチック</span><span class="sxs-lookup"><span data-stu-id="97656-114">Plastic</span></span>  <br/> |
|<span data-ttu-id="97656-115">4</span><span class="sxs-lookup"><span data-stu-id="97656-115">4</span></span>  <br/> |<span data-ttu-id="97656-116">メタル</span><span class="sxs-lookup"><span data-stu-id="97656-116">Metal</span></span>  <br/> |
|<span data-ttu-id="97656-117">5</span><span class="sxs-lookup"><span data-stu-id="97656-117">5</span></span>  <br/> |<span data-ttu-id="97656-118">ダーク エッジ</span><span class="sxs-lookup"><span data-stu-id="97656-118">Dark Edge</span></span>  <br/> |
|<span data-ttu-id="97656-119">6</span><span class="sxs-lookup"><span data-stu-id="97656-119">6</span></span>  <br/> |<span data-ttu-id="97656-120">ぼかし</span><span class="sxs-lookup"><span data-stu-id="97656-120">Soft Edge</span></span>  <br/> |
|<span data-ttu-id="97656-121">7</span><span class="sxs-lookup"><span data-stu-id="97656-121">7</span></span>  <br/> |<span data-ttu-id="97656-122">フラット</span><span class="sxs-lookup"><span data-stu-id="97656-122">Flat</span></span>  <br/> |
|<span data-ttu-id="97656-123">8</span><span class="sxs-lookup"><span data-stu-id="97656-123">8</span></span>  <br/> |<span data-ttu-id="97656-124">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="97656-124">Wireframe</span></span>  <br/> |
|<span data-ttu-id="97656-125">9</span><span class="sxs-lookup"><span data-stu-id="97656-125">9</span></span>  <br/> |<span data-ttu-id="97656-126">パウダー</span><span class="sxs-lookup"><span data-stu-id="97656-126">Powder</span></span>  <br/> |
|<span data-ttu-id="97656-127">10</span><span class="sxs-lookup"><span data-stu-id="97656-127">10</span></span>  <br/> |<span data-ttu-id="97656-128">透明パウダー</span><span class="sxs-lookup"><span data-stu-id="97656-128">Translucent Powder</span></span>  <br/> |
|<span data-ttu-id="97656-129">11</span><span class="sxs-lookup"><span data-stu-id="97656-129">11</span></span>  <br/> |<span data-ttu-id="97656-130">透明</span><span class="sxs-lookup"><span data-stu-id="97656-130">Clear</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97656-131">備考</span><span class="sxs-lookup"><span data-stu-id="97656-131">Remarks</span></span>

<span data-ttu-id="97656-132">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelMaterialType** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="97656-132">To get a reference to the **BevelMaterialType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97656-133">セル名:</span><span class="sxs-lookup"><span data-stu-id="97656-133">Cell name:</span></span>  <br/> | <span data-ttu-id="97656-134">BevelMaterialType</span><span class="sxs-lookup"><span data-stu-id="97656-134">BevelMaterialType</span></span>  <br/> |
   
<span data-ttu-id="97656-135">プログラムから、インデックスによって [ **BevelMaterialType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="97656-135">To get a reference to the **BevelMaterialType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97656-136">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="97656-136">Section index:</span></span>  <br/> |<span data-ttu-id="97656-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97656-137">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97656-138">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="97656-138">Row index:</span></span>  <br/> |<span data-ttu-id="97656-139">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="97656-139">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="97656-140">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="97656-140">Cell index:</span></span>  <br/> |<span data-ttu-id="97656-141">**visBevelMaterialType**</span><span class="sxs-lookup"><span data-stu-id="97656-141">**visBevelMaterialType**</span></span> <br/> |
   

