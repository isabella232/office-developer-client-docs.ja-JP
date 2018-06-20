---
title: ISERROR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Cellreference の値は、エラーの種類は、かどうかに TRUE を返します。それ以外の場合、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805620"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="6b5d9-104">ISERROR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6b5d9-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6b5d9-105">_Cellreference_の値は、エラーの種類は、かどうかに TRUE を返します。それ以外の場合、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="6b5d9-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="6b5d9-106">ISERROR 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b5d9-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6b5d9-107">構文</span><span class="sxs-lookup"><span data-stu-id="6b5d9-107">Syntax</span></span>

<span data-ttu-id="6b5d9-108">ISERROR (* * *cellreference* * *)</span><span class="sxs-lookup"><span data-stu-id="6b5d9-108">ISERROR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6b5d9-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b5d9-109">Parameters</span></span>

|<span data-ttu-id="6b5d9-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-110">**Name**</span></span>|<span data-ttu-id="6b5d9-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-111">**Required/Optional**</span></span>|<span data-ttu-id="6b5d9-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-112">**Data Type**</span></span>|<span data-ttu-id="6b5d9-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6b5d9-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="6b5d9-114">_cellreference_</span></span> <br/> |<span data-ttu-id="6b5d9-115">必須</span><span class="sxs-lookup"><span data-stu-id="6b5d9-115">Required</span></span>  <br/> |<span data-ttu-id="6b5d9-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-116">**String**</span></span> <br/> |<span data-ttu-id="6b5d9-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b5d9-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="6b5d9-118">例 1</span><span class="sxs-lookup"><span data-stu-id="6b5d9-118">Example 1</span></span>

|<span data-ttu-id="6b5d9-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-119">**Cell**</span></span>|<span data-ttu-id="6b5d9-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-120">**Formula**</span></span>|<span data-ttu-id="6b5d9-121">**返される値**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b5d9-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="6b5d9-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="6b5d9-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="6b5d9-123">=NA( )</span></span>  <br/> |<span data-ttu-id="6b5d9-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="6b5d9-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="6b5d9-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="6b5d9-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="6b5d9-126">=ISERROR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="6b5d9-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="6b5d9-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b5d9-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="6b5d9-p103">ISERROR 関数は #N/A! エラーを認識するため、TRUE を返します。#N/A! エラー以外のすべてのエラー タイプを検出する場合は、ISERR を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6b5d9-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6b5d9-132">例 2</span><span class="sxs-lookup"><span data-stu-id="6b5d9-132">Example 2</span></span>

|<span data-ttu-id="6b5d9-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-133">**Cell**</span></span>|<span data-ttu-id="6b5d9-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-134">**Formula**</span></span>|<span data-ttu-id="6b5d9-135">**返される値**</span><span class="sxs-lookup"><span data-stu-id="6b5d9-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b5d9-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="6b5d9-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="6b5d9-137">="House"</span><span class="sxs-lookup"><span data-stu-id="6b5d9-137">="House"</span></span>  <br/> |<span data-ttu-id="6b5d9-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="6b5d9-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="6b5d9-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="6b5d9-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="6b5d9-140">=ISERROR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="6b5d9-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="6b5d9-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b5d9-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="6b5d9-p104">ISERROR 関数は #VALUE! エラーを認識するため、TRUE を返します。#VALUE! エラーを基に式を作成するには、ISERRVALUE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6b5d9-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

