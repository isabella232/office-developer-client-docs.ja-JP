---
title: ISERRNA 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Cellreference の値が #n/a エラーの種類である場合は、TRUE を返します。 (利用できない)。それ以外の場合、FALSE を返します。 ISERRNA 関数は、別のセルを参照する数式で使用されます。'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805618"
---
# <a name="iserrna-function"></a><span data-ttu-id="f5e91-105">ISERRNA 関数</span><span class="sxs-lookup"><span data-stu-id="f5e91-105">ISERRNA Function</span></span>

<span data-ttu-id="f5e91-106">_Cellreference_の値が #n/a エラーの種類である場合は、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f5e91-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="f5e91-107">(利用できない)。それ以外の場合、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f5e91-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="f5e91-108">ISERRNA 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5e91-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f5e91-109">構文</span><span class="sxs-lookup"><span data-stu-id="f5e91-109">Syntax</span></span>

<span data-ttu-id="f5e91-110">ISERRNA (* * *cellreference* * *)</span><span class="sxs-lookup"><span data-stu-id="f5e91-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f5e91-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5e91-111">Parameters</span></span>

|<span data-ttu-id="f5e91-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="f5e91-112">**Name**</span></span>|<span data-ttu-id="f5e91-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f5e91-113">**Required/Optional**</span></span>|<span data-ttu-id="f5e91-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f5e91-114">**Data Type**</span></span>|<span data-ttu-id="f5e91-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f5e91-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f5e91-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="f5e91-116">_cellreference_</span></span> <br/> |<span data-ttu-id="f5e91-117">必須</span><span class="sxs-lookup"><span data-stu-id="f5e91-117">Required</span></span>  <br/> |<span data-ttu-id="f5e91-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f5e91-118">**String**</span></span> <br/> |<span data-ttu-id="f5e91-119">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5e91-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="f5e91-120">例 1</span><span class="sxs-lookup"><span data-stu-id="f5e91-120">Example 1</span></span>

|<span data-ttu-id="f5e91-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f5e91-121">**Cell**</span></span>|<span data-ttu-id="f5e91-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f5e91-122">**Formula**</span></span>|<span data-ttu-id="f5e91-123">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="f5e91-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5e91-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="f5e91-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f5e91-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="f5e91-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="f5e91-126">「8」</span><span class="sxs-lookup"><span data-stu-id="f5e91-126">"8"</span></span>  <br/> |
|<span data-ttu-id="f5e91-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="f5e91-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="f5e91-128">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="f5e91-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="f5e91-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="f5e91-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="f5e91-130">戻り値が有効であるため、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f5e91-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f5e91-131">例 2</span><span class="sxs-lookup"><span data-stu-id="f5e91-131">Example 2</span></span>

|<span data-ttu-id="f5e91-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f5e91-132">**Cell**</span></span>|<span data-ttu-id="f5e91-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f5e91-133">**Formula**</span></span>|<span data-ttu-id="f5e91-134">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="f5e91-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5e91-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="f5e91-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f5e91-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="f5e91-136">=NA( )</span></span>  <br/> |<span data-ttu-id="f5e91-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="f5e91-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="f5e91-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="f5e91-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="f5e91-139">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="f5e91-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="f5e91-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="f5e91-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="f5e91-141">戻り値がエラー タイプ #N/A! であるため、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="f5e91-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

