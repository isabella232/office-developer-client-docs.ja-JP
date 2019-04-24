---
title: MODULUS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: 数値を除数で割ったときの剰余 (モジュラス) を返します。
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356995"
---
# <a name="modulus-function"></a><span data-ttu-id="c063f-103">MODULUS 関数</span><span class="sxs-lookup"><span data-stu-id="c063f-103">MODULUS Function</span></span>

<span data-ttu-id="c063f-104">数値を除数で割ったときの剰余 (モジュラス) を返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c063f-105">構文</span><span class="sxs-lookup"><span data-stu-id="c063f-105">Syntax</span></span>

<span data-ttu-id="c063f-106">モジュラス (\* **数値** \*, \* **除数** \*)</span><span class="sxs-lookup"><span data-stu-id="c063f-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c063f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c063f-107">Parameters</span></span>

|<span data-ttu-id="c063f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c063f-108">**Name**</span></span>|<span data-ttu-id="c063f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c063f-109">**Required/Optional**</span></span>|<span data-ttu-id="c063f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c063f-110">**Data Type**</span></span>|<span data-ttu-id="c063f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c063f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c063f-112">_number_</span><span class="sxs-lookup"><span data-stu-id="c063f-112">_number_</span></span> <br/> |<span data-ttu-id="c063f-113">必須</span><span class="sxs-lookup"><span data-stu-id="c063f-113">Required</span></span>  <br/> |<span data-ttu-id="c063f-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="c063f-114">**Number**</span></span> <br/> |<span data-ttu-id="c063f-115">被除数 (割られる数) を指定します。</span><span class="sxs-lookup"><span data-stu-id="c063f-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="c063f-116">_序数_</span><span class="sxs-lookup"><span data-stu-id="c063f-116">_divisor_</span></span> <br/> |<span data-ttu-id="c063f-117">必須</span><span class="sxs-lookup"><span data-stu-id="c063f-117">Required</span></span>  <br/> |<span data-ttu-id="c063f-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="c063f-118">**Number**</span></span> <br/> |<span data-ttu-id="c063f-119">除数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c063f-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c063f-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="c063f-120">Return value</span></span>

<span data-ttu-id="c063f-121">番号</span><span class="sxs-lookup"><span data-stu-id="c063f-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c063f-122">解説</span><span class="sxs-lookup"><span data-stu-id="c063f-122">Remarks</span></span>

<span data-ttu-id="c063f-p101">結果には除数と同じ符号が付きます。除数が 0 の場合、#DIV/0! エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="c063f-126">ほとんどの場合、MOD 関数ではなく MODULUS 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="c063f-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c063f-127">例 1</span><span class="sxs-lookup"><span data-stu-id="c063f-127">Example 1</span></span>

<span data-ttu-id="c063f-128">MODULUS(5, 1.4)</span><span class="sxs-lookup"><span data-stu-id="c063f-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="c063f-129">0.8 を返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c063f-130">例 2</span><span class="sxs-lookup"><span data-stu-id="c063f-130">Example 2</span></span>

<span data-ttu-id="c063f-131">MODULUS(5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="c063f-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="c063f-132">-0.6 を返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c063f-133">例 3</span><span class="sxs-lookup"><span data-stu-id="c063f-133">Example 3</span></span>

<span data-ttu-id="c063f-134">MODULUS(-5, 1.4)</span><span class="sxs-lookup"><span data-stu-id="c063f-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="c063f-135">0.6 を返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="c063f-136">例 4</span><span class="sxs-lookup"><span data-stu-id="c063f-136">Example 4</span></span>

<span data-ttu-id="c063f-137">MODULUS(-5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="c063f-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="c063f-138">-0.8 を返します。</span><span class="sxs-lookup"><span data-stu-id="c063f-138">Returns -0.8.</span></span>
  

