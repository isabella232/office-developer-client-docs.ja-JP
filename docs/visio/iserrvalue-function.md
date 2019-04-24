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
description: 'cellreference の値が error type #VALUE の場合は TRUE を返します。数式の引数の型が正しくありません。 iserrvalue 関数は、別のセルを参照する論理式で使用します。'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317886"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="cca44-104">ISERRVALUE 関数</span><span class="sxs-lookup"><span data-stu-id="cca44-104">ISERRVALUE Function</span></span>

<span data-ttu-id="cca44-105">_cellreference_の値が error type #VALUE の場合は TRUE を返します。数式の引数の型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="cca44-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="cca44-106">iserrvalue 関数は、別のセルを参照する論理式で使用します。</span><span class="sxs-lookup"><span data-stu-id="cca44-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cca44-107">構文</span><span class="sxs-lookup"><span data-stu-id="cca44-107">Syntax</span></span>

<span data-ttu-id="cca44-108">iserrvalue (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cca44-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cca44-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cca44-109">Parameters</span></span>

|<span data-ttu-id="cca44-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="cca44-110">**Name**</span></span>|<span data-ttu-id="cca44-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cca44-111">**Required/Optional**</span></span>|<span data-ttu-id="cca44-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cca44-112">**Data Type**</span></span>|<span data-ttu-id="cca44-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="cca44-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cca44-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="cca44-114">_cellreference_</span></span> <br/> |<span data-ttu-id="cca44-115">必須</span><span class="sxs-lookup"><span data-stu-id="cca44-115">Required</span></span>  <br/> |<span data-ttu-id="cca44-116">**String**</span><span class="sxs-lookup"><span data-stu-id="cca44-116">**String**</span></span> <br/> |<span data-ttu-id="cca44-117">セルの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="cca44-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cca44-118">解説</span><span class="sxs-lookup"><span data-stu-id="cca44-118">Remarks</span></span>

<span data-ttu-id="cca44-p103">[Scratch] セル A ～ D は #VALUE! エラーを返しません。このセルの数式では、同じ文字列内に数値と文字を含めることができるためです。ただしセル [X] および [Y] では、数値のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cca44-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cca44-122">例 1</span><span class="sxs-lookup"><span data-stu-id="cca44-122">Example 1</span></span>

|<span data-ttu-id="cca44-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cca44-123">**Cell**</span></span>|<span data-ttu-id="cca44-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="cca44-124">**Formula**</span></span>|<span data-ttu-id="cca44-125">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="cca44-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cca44-126">最初の X1</span><span class="sxs-lookup"><span data-stu-id="cca44-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="cca44-127">= "House"</span><span class="sxs-lookup"><span data-stu-id="cca44-127">= "House"</span></span>  <br/> |<span data-ttu-id="cca44-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="cca44-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="cca44-129">最初の A1</span><span class="sxs-lookup"><span data-stu-id="cca44-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="cca44-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="cca44-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="cca44-131">pbm-2</span><span class="sxs-lookup"><span data-stu-id="cca44-131">2</span></span>  <br/> |
   
<span data-ttu-id="cca44-p104">戻り値は #VALUE! エラーを示す 2 です。Microsoft Visio でエラーの代わりに 2 を返すように式で指定されています。</span><span class="sxs-lookup"><span data-stu-id="cca44-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cca44-134">例 2</span><span class="sxs-lookup"><span data-stu-id="cca44-134">Example 2</span></span>

|<span data-ttu-id="cca44-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="cca44-135">**Cell**</span></span>|<span data-ttu-id="cca44-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="cca44-136">**Formula**</span></span>|<span data-ttu-id="cca44-137">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="cca44-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cca44-138">最初の A1</span><span class="sxs-lookup"><span data-stu-id="cca44-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="cca44-139">="5 +7"</span><span class="sxs-lookup"><span data-stu-id="cca44-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="cca44-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="cca44-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="cca44-141">最初の B1</span><span class="sxs-lookup"><span data-stu-id="cca44-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="cca44-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="cca44-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="cca44-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="cca44-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="cca44-p105">戻り値は #VALUE! エラーではなく、また元のセルの値を返すように式で指定されているため、12 を返します。</span><span class="sxs-lookup"><span data-stu-id="cca44-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

