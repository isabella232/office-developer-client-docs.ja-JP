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
description: セル参照の値がエラー型の場合は true を#VALUE式の引数が間違った型です。 ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404429"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="cd55a-104">ISERRVALUE 関数</span><span class="sxs-lookup"><span data-stu-id="cd55a-104">ISERRVALUE Function</span></span>

<span data-ttu-id="cd55a-105">セル参照の値がエラー型の場合は true を#VALUE式の引数が間違った型です。</span><span class="sxs-lookup"><span data-stu-id="cd55a-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="cd55a-106">ISERRVALUE 関数は、別のセルを参照する論理式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd55a-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd55a-107">構文</span><span class="sxs-lookup"><span data-stu-id="cd55a-107">Syntax</span></span>

<span data-ttu-id="cd55a-108">ISERRVALUE(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cd55a-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd55a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd55a-109">Parameters</span></span>

|<span data-ttu-id="cd55a-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="cd55a-110">**Name**</span></span>|<span data-ttu-id="cd55a-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cd55a-111">**Required/Optional**</span></span>|<span data-ttu-id="cd55a-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cd55a-112">**Data Type**</span></span>|<span data-ttu-id="cd55a-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="cd55a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd55a-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="cd55a-114">_cellreference_</span></span> <br/> |<span data-ttu-id="cd55a-115">必須</span><span class="sxs-lookup"><span data-stu-id="cd55a-115">Required</span></span>  <br/> |<span data-ttu-id="cd55a-116">**String**</span><span class="sxs-lookup"><span data-stu-id="cd55a-116">**String**</span></span> <br/> |<span data-ttu-id="cd55a-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd55a-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd55a-118">注釈</span><span class="sxs-lookup"><span data-stu-id="cd55a-118">Remarks</span></span>

<span data-ttu-id="cd55a-p103">[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cd55a-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cd55a-122">例 1</span><span class="sxs-lookup"><span data-stu-id="cd55a-122">Example 1</span></span>

|<span data-ttu-id="cd55a-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cd55a-123">**Cell**</span></span>|<span data-ttu-id="cd55a-124">**式**</span><span class="sxs-lookup"><span data-stu-id="cd55a-124">**Formula**</span></span>|<span data-ttu-id="cd55a-125">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="cd55a-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd55a-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="cd55a-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="cd55a-127">= "House"</span><span class="sxs-lookup"><span data-stu-id="cd55a-127">= "House"</span></span>  <br/> |<span data-ttu-id="cd55a-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="cd55a-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="cd55a-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="cd55a-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="cd55a-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="cd55a-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="cd55a-131">2</span><span class="sxs-lookup"><span data-stu-id="cd55a-131">2</span></span>  <br/> |
   
<span data-ttu-id="cd55a-p104">戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。</span><span class="sxs-lookup"><span data-stu-id="cd55a-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cd55a-134">例 2</span><span class="sxs-lookup"><span data-stu-id="cd55a-134">Example 2</span></span>

|<span data-ttu-id="cd55a-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cd55a-135">**Cell**</span></span>|<span data-ttu-id="cd55a-136">**式**</span><span class="sxs-lookup"><span data-stu-id="cd55a-136">**Formula**</span></span>|<span data-ttu-id="cd55a-137">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="cd55a-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd55a-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="cd55a-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="cd55a-139">="5 +7"</span><span class="sxs-lookup"><span data-stu-id="cd55a-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="cd55a-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="cd55a-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="cd55a-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="cd55a-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="cd55a-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="cd55a-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="cd55a-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="cd55a-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="cd55a-p105">戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。</span><span class="sxs-lookup"><span data-stu-id="cd55a-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

