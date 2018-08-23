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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806101"
---
# <a name="pow-function"></a><span data-ttu-id="f0812-103">POW 関数</span><span class="sxs-lookup"><span data-stu-id="f0812-103">POW Function</span></span>

<span data-ttu-id="f0812-104">指数で累乗した数値を返します。</span><span class="sxs-lookup"><span data-stu-id="f0812-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f0812-105">構文</span><span class="sxs-lookup"><span data-stu-id="f0812-105">Syntax</span></span>

<span data-ttu-id="f0812-106">POW (* **番号** *、* **指数** *)</span><span class="sxs-lookup"><span data-stu-id="f0812-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f0812-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f0812-107">Parameters</span></span>

|<span data-ttu-id="f0812-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="f0812-108">**Name**</span></span>|<span data-ttu-id="f0812-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f0812-109">**Required/Optional**</span></span>|<span data-ttu-id="f0812-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f0812-110">**Data Type**</span></span>|<span data-ttu-id="f0812-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0812-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f0812-112">_number_</span><span class="sxs-lookup"><span data-stu-id="f0812-112">_number_</span></span> <br/> |<span data-ttu-id="f0812-113">必須</span><span class="sxs-lookup"><span data-stu-id="f0812-113">Required</span></span>  <br/> |<span data-ttu-id="f0812-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="f0812-114">**Number**</span></span> <br/> |<span data-ttu-id="f0812-115">指数で累乗する数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0812-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="f0812-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="f0812-116">_exponent_</span></span> <br/> |<span data-ttu-id="f0812-117">必須</span><span class="sxs-lookup"><span data-stu-id="f0812-117">Required</span></span>  <br/> |<span data-ttu-id="f0812-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="f0812-118">**Number**</span></span> <br/> |<span data-ttu-id="f0812-119">指数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f0812-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0812-120">注釈</span><span class="sxs-lookup"><span data-stu-id="f0812-120">Remarks</span></span>

<span data-ttu-id="f0812-121">_数値_と_指数_の両方に整数以外の場合、可能性があり、負の値になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0812-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="f0812-122">_番号_が 0 と_指数_ではないかどうかは 0、1 を返します。</span><span class="sxs-lookup"><span data-stu-id="f0812-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="f0812-123">_数_が 0_の指数部_が負の場合、この関数は 0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="f0812-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="f0812-124">_数値_と_指数_の両方が 0 である場合、またはが負の_数_と_指数_が整数でない場合は、この関数は 0.0 を返します。</span><span class="sxs-lookup"><span data-stu-id="f0812-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="f0812-125">_数値_と_指数_の両方が負の値場合は、この関数は-1 を返します #IND.。</span><span class="sxs-lookup"><span data-stu-id="f0812-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f0812-126">例</span><span class="sxs-lookup"><span data-stu-id="f0812-126">Example</span></span>

<span data-ttu-id="f0812-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="f0812-127">POW(5,2)</span></span> 
  
<span data-ttu-id="f0812-128">25 を返します。</span><span class="sxs-lookup"><span data-stu-id="f0812-128">Returns 25.</span></span> 
  

