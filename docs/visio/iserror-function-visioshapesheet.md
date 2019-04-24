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
description: cellreference の値がエラー型の場合は TRUE を返します。それ以外の場合は、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317893"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="d44d4-104">ISERROR 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d44d4-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d44d4-105">_cellreference_の値がエラー型の場合は TRUE を返します。それ以外の場合は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="d44d4-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="d44d4-106">ISERROR 関数は、別のセルを参照する数式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d44d4-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d44d4-107">構文</span><span class="sxs-lookup"><span data-stu-id="d44d4-107">Syntax</span></span>

<span data-ttu-id="d44d4-108">ISERROR (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d44d4-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d44d4-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d44d4-109">Parameters</span></span>

|<span data-ttu-id="d44d4-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="d44d4-110">**Name**</span></span>|<span data-ttu-id="d44d4-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d44d4-111">**Required/Optional**</span></span>|<span data-ttu-id="d44d4-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d44d4-112">**Data Type**</span></span>|<span data-ttu-id="d44d4-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="d44d4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d44d4-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="d44d4-114">_cellreference_</span></span> <br/> |<span data-ttu-id="d44d4-115">必須</span><span class="sxs-lookup"><span data-stu-id="d44d4-115">Required</span></span>  <br/> |<span data-ttu-id="d44d4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="d44d4-116">**String**</span></span> <br/> |<span data-ttu-id="d44d4-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d44d4-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d44d4-118">例 1</span><span class="sxs-lookup"><span data-stu-id="d44d4-118">Example 1</span></span>

|<span data-ttu-id="d44d4-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d44d4-119">**Cell**</span></span>|<span data-ttu-id="d44d4-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="d44d4-120">**Formula**</span></span>|<span data-ttu-id="d44d4-121">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d44d4-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d44d4-122">最初の A1</span><span class="sxs-lookup"><span data-stu-id="d44d4-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="d44d4-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="d44d4-123">=NA( )</span></span>  <br/> |<span data-ttu-id="d44d4-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="d44d4-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="d44d4-125">最初の B1</span><span class="sxs-lookup"><span data-stu-id="d44d4-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d44d4-126">= ISERROR (最初に A1)</span><span class="sxs-lookup"><span data-stu-id="d44d4-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="d44d4-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="d44d4-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="d44d4-p103">ISERROR 関数は #N/A! エラーを認識するため、TRUE を返します。#N/A! エラー以外のすべてのエラー タイプを検出する場合は、ISERR を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d44d4-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d44d4-132">例 2</span><span class="sxs-lookup"><span data-stu-id="d44d4-132">Example 2</span></span>

|<span data-ttu-id="d44d4-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d44d4-133">**Cell**</span></span>|<span data-ttu-id="d44d4-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="d44d4-134">**Formula**</span></span>|<span data-ttu-id="d44d4-135">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="d44d4-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d44d4-136">最初の X1</span><span class="sxs-lookup"><span data-stu-id="d44d4-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="d44d4-137">= "House"</span><span class="sxs-lookup"><span data-stu-id="d44d4-137">="House"</span></span>  <br/> |<span data-ttu-id="d44d4-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="d44d4-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="d44d4-139">最初の B1</span><span class="sxs-lookup"><span data-stu-id="d44d4-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d44d4-140">= ISERROR (最初の X1)</span><span class="sxs-lookup"><span data-stu-id="d44d4-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="d44d4-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="d44d4-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="d44d4-p104">ISERROR 関数は #VALUE! エラーを認識するため、TRUE を返します。#VALUE! エラーを基に式を作成するには、ISERRVALUE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d44d4-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

