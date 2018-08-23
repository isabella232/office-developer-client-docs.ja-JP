---
title: ISERRVALUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: Cellreference の値がエラーの場合は TRUE を返しますが、数式内の引数が間違った型である、#VALUE を入力します。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805623"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="edac3-104">ISERRVALUE 関数</span><span class="sxs-lookup"><span data-stu-id="edac3-104">ISERRVALUE Function</span></span>

<span data-ttu-id="edac3-105">_Cellreference_の値がエラーの場合は TRUE を返しますが、数式内の引数が間違った型である、#VALUE を入力します。</span><span class="sxs-lookup"><span data-stu-id="edac3-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="edac3-106">ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="edac3-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="edac3-107">構文</span><span class="sxs-lookup"><span data-stu-id="edac3-107">Syntax</span></span>

<span data-ttu-id="edac3-108">ISERRVALUE (* * *cellreference* * *)</span><span class="sxs-lookup"><span data-stu-id="edac3-108">ISERRVALUE(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="edac3-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edac3-109">Parameters</span></span>

|<span data-ttu-id="edac3-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="edac3-110">**Name**</span></span>|<span data-ttu-id="edac3-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="edac3-111">**Required/Optional**</span></span>|<span data-ttu-id="edac3-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="edac3-112">**Data Type**</span></span>|<span data-ttu-id="edac3-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="edac3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="edac3-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="edac3-114">_cellreference_</span></span> <br/> |<span data-ttu-id="edac3-115">必須</span><span class="sxs-lookup"><span data-stu-id="edac3-115">Required</span></span>  <br/> |<span data-ttu-id="edac3-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="edac3-116">**String**</span></span> <br/> |<span data-ttu-id="edac3-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="edac3-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edac3-118">注釈</span><span class="sxs-lookup"><span data-stu-id="edac3-118">Remarks</span></span>

<span data-ttu-id="edac3-p103">[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edac3-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="edac3-122">例 1</span><span class="sxs-lookup"><span data-stu-id="edac3-122">Example 1</span></span>

|<span data-ttu-id="edac3-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="edac3-123">**Cell**</span></span>|<span data-ttu-id="edac3-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="edac3-124">**Formula**</span></span>|<span data-ttu-id="edac3-125">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="edac3-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edac3-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="edac3-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="edac3-127">= "House"</span><span class="sxs-lookup"><span data-stu-id="edac3-127">= "House"</span></span>  <br/> |<span data-ttu-id="edac3-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="edac3-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="edac3-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="edac3-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="edac3-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="edac3-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="edac3-131">2</span><span class="sxs-lookup"><span data-stu-id="edac3-131">2</span></span>  <br/> |
   
<span data-ttu-id="edac3-p104">戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。</span><span class="sxs-lookup"><span data-stu-id="edac3-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="edac3-134">例 2</span><span class="sxs-lookup"><span data-stu-id="edac3-134">Example 2</span></span>

|<span data-ttu-id="edac3-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="edac3-135">**Cell**</span></span>|<span data-ttu-id="edac3-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="edac3-136">**Formula**</span></span>|<span data-ttu-id="edac3-137">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="edac3-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edac3-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="edac3-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="edac3-139">="5 +7"</span><span class="sxs-lookup"><span data-stu-id="edac3-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="edac3-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="edac3-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="edac3-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="edac3-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="edac3-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="edac3-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="edac3-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="edac3-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="edac3-p105">戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。</span><span class="sxs-lookup"><span data-stu-id="edac3-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

