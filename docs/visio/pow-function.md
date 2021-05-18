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
description: 指数の出力に上げられた数値を返します。
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406312"
---
# <a name="pow-function"></a><span data-ttu-id="0a967-103">POW 関数</span><span class="sxs-lookup"><span data-stu-id="0a967-103">POW Function</span></span>

<span data-ttu-id="0a967-104">指数の出力に上げられた数値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0a967-105">構文</span><span class="sxs-lookup"><span data-stu-id="0a967-105">Syntax</span></span>

<span data-ttu-id="0a967-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0a967-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a967-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0a967-107">Parameters</span></span>

|<span data-ttu-id="0a967-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0a967-108">**Name**</span></span>|<span data-ttu-id="0a967-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0a967-109">**Required/Optional**</span></span>|<span data-ttu-id="0a967-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0a967-110">**Data Type**</span></span>|<span data-ttu-id="0a967-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a967-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a967-112">_number_</span><span class="sxs-lookup"><span data-stu-id="0a967-112">_number_</span></span> <br/> |<span data-ttu-id="0a967-113">必須</span><span class="sxs-lookup"><span data-stu-id="0a967-113">Required</span></span>  <br/> |<span data-ttu-id="0a967-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="0a967-114">**Number**</span></span> <br/> |<span data-ttu-id="0a967-115">指数で累乗する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a967-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="0a967-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="0a967-116">_exponent_</span></span> <br/> |<span data-ttu-id="0a967-117">必須</span><span class="sxs-lookup"><span data-stu-id="0a967-117">Required</span></span>  <br/> |<span data-ttu-id="0a967-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="0a967-118">**Number**</span></span> <br/> |<span data-ttu-id="0a967-119">指数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a967-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a967-120">注釈</span><span class="sxs-lookup"><span data-stu-id="0a967-120">Remarks</span></span>

<span data-ttu-id="0a967-121">数値 _と__指数の両方が_ 整数以外で、負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0a967-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="0a967-122">_数値が_ 0 ではなく、_指数_ が 0 の場合、この関数は 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="0a967-123">_数値が_ 0 で、_指数が_ 負の場合、この関数は 0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="0a967-124">数値と _指数_ の _両方_ が 0 の場合、または _数値_ が負で指数が整数ではない場合、この関数は 0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="0a967-125">数値と _指数の__両方が負_ の場合、この関数は -1.#IND を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0a967-126">例</span><span class="sxs-lookup"><span data-stu-id="0a967-126">Example</span></span>

<span data-ttu-id="0a967-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="0a967-127">POW(5,2)</span></span> 
  
<span data-ttu-id="0a967-128">25 を返します。</span><span class="sxs-lookup"><span data-stu-id="0a967-128">Returns 25.</span></span> 
  

