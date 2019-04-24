---
title: POW 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: 指数で累乗した数値を返します。
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356050"
---
# <a name="pow-function"></a><span data-ttu-id="0b94f-103">POW 関数</span><span class="sxs-lookup"><span data-stu-id="0b94f-103">POW Function</span></span>

<span data-ttu-id="0b94f-104">指数で累乗した数値を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0b94f-105">構文</span><span class="sxs-lookup"><span data-stu-id="0b94f-105">Syntax</span></span>

<span data-ttu-id="0b94f-106">POW (\* **数値** *、* **指数** \*)</span><span class="sxs-lookup"><span data-stu-id="0b94f-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0b94f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b94f-107">Parameters</span></span>

|<span data-ttu-id="0b94f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0b94f-108">**Name**</span></span>|<span data-ttu-id="0b94f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0b94f-109">**Required/Optional**</span></span>|<span data-ttu-id="0b94f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0b94f-110">**Data Type**</span></span>|<span data-ttu-id="0b94f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0b94f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0b94f-112">_number_</span><span class="sxs-lookup"><span data-stu-id="0b94f-112">_number_</span></span> <br/> |<span data-ttu-id="0b94f-113">必須</span><span class="sxs-lookup"><span data-stu-id="0b94f-113">Required</span></span>  <br/> |<span data-ttu-id="0b94f-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="0b94f-114">**Number**</span></span> <br/> |<span data-ttu-id="0b94f-115">指数で累乗する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="0b94f-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="0b94f-116">_exponent_</span></span> <br/> |<span data-ttu-id="0b94f-117">必須</span><span class="sxs-lookup"><span data-stu-id="0b94f-117">Required</span></span>  <br/> |<span data-ttu-id="0b94f-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="0b94f-118">**Number**</span></span> <br/> |<span data-ttu-id="0b94f-119">指数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b94f-120">解説</span><span class="sxs-lookup"><span data-stu-id="0b94f-120">Remarks</span></span>

<span data-ttu-id="0b94f-121">数値と_指数_の両方とも整数ではない場合があり、負の_値_にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0b94f-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="0b94f-122">_数値_が0以外で、_指数_が0の場合、この関数は1を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="0b94f-123">数値が0で、_指数_が負の_数_である場合、この関数は0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="0b94f-124">_数値_と_指数_の両方が0の場合、または_数値_が負で、_指数_が整数ではない場合、この関数は0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="0b94f-125">数値と_指数_の両方が負の_数_である場合、この関数は-1. #IND を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0b94f-126">例</span><span class="sxs-lookup"><span data-stu-id="0b94f-126">Example</span></span>

<span data-ttu-id="0b94f-127">POW (5、2)</span><span class="sxs-lookup"><span data-stu-id="0b94f-127">POW(5,2)</span></span> 
  
<span data-ttu-id="0b94f-128">25 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b94f-128">Returns 25.</span></span> 
  

