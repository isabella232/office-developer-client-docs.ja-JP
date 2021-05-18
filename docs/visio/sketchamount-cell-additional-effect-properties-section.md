---
title: '[SketchAmount] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404422"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="2ded5-103">[SketchAmount] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="2ded5-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="2ded5-104">スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="2ded5-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="2ded5-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2ded5-105">**Value**</span></span>|<span data-ttu-id="2ded5-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ded5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ded5-107">0</span><span class="sxs-lookup"><span data-stu-id="2ded5-107">0</span></span>  <br/> |<span data-ttu-id="2ded5-108">図形には、適用されるスケッチ効果はありません。</span><span class="sxs-lookup"><span data-stu-id="2ded5-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="2ded5-109">1-25</span><span class="sxs-lookup"><span data-stu-id="2ded5-109">1-25</span></span>  <br/> |<span data-ttu-id="2ded5-110">図形には、スケッチのゆがみが適用されています。1 の値ではゆがみがもっとも大きく、25 ではもっとも小さくなります。</span><span class="sxs-lookup"><span data-stu-id="2ded5-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ded5-111">注釈</span><span class="sxs-lookup"><span data-stu-id="2ded5-111">Remarks</span></span>

<span data-ttu-id="2ded5-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchAmount**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2ded5-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ded5-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="2ded5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2ded5-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="2ded5-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="2ded5-115">プログラムから、インデックスによって [**SketchAmount**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ded5-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ded5-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ded5-116">Section index:</span></span>  <br/> |<span data-ttu-id="2ded5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ded5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ded5-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ded5-118">Row index:</span></span>  <br/> |<span data-ttu-id="2ded5-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="2ded5-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="2ded5-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ded5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2ded5-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="2ded5-121">**visSketchAmount**</span></span> <br/> |
   

