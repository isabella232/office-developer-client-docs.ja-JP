---
title: MAGNITUDE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: constantA と constantB のそれぞれの定数によって、x がで、その実行が B であるベクトルの大きさを返します。
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317816"
---
# <a name="magnitude-function"></a><span data-ttu-id="c4cf4-103">MAGNITUDE 関数</span><span class="sxs-lookup"><span data-stu-id="c4cf4-103">MAGNITUDE Function</span></span>

<span data-ttu-id="c4cf4-104">_constantA_と_constantB_のそれぞれの定数によっ__ て、x がで、その実行が_B_であるベクトルの大きさを返します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c4cf4-105">構文</span><span class="sxs-lookup"><span data-stu-id="c4cf4-105">Syntax</span></span>

<span data-ttu-id="c4cf4-106">マグニチュード (\* \* *constantA* \* *、* \* *A* \* *、* \* *constantB* \* *、* \* *B* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4cf4-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4cf4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4cf4-107">Parameters</span></span>

|<span data-ttu-id="c4cf4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-108">**Name**</span></span>|<span data-ttu-id="c4cf4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-109">**Required/Optional**</span></span>|<span data-ttu-id="c4cf4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-110">**Data Type**</span></span>|<span data-ttu-id="c4cf4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4cf4-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="c4cf4-112">_constantA_</span></span> <br/> |<span data-ttu-id="c4cf4-113">必須</span><span class="sxs-lookup"><span data-stu-id="c4cf4-113">Required</span></span>  <br/> |<span data-ttu-id="c4cf4-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-114">**Number**</span></span> <br/> |<span data-ttu-id="c4cf4-115">高さを乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="c4cf4-116">_A_</span><span class="sxs-lookup"><span data-stu-id="c4cf4-116">_A_</span></span> <br/> |<span data-ttu-id="c4cf4-117">必須</span><span class="sxs-lookup"><span data-stu-id="c4cf4-117">Required</span></span>  <br/> |<span data-ttu-id="c4cf4-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-118">**Number**</span></span> <br/> |<span data-ttu-id="c4cf4-119">高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="c4cf4-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="c4cf4-120">_constantB_</span></span> <br/> |<span data-ttu-id="c4cf4-121">必須</span><span class="sxs-lookup"><span data-stu-id="c4cf4-121">Required</span></span>  <br/> |<span data-ttu-id="c4cf4-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-122">**Number**</span></span> <br/> |<span data-ttu-id="c4cf4-123">水平距離を乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="c4cf4-124">_B_</span><span class="sxs-lookup"><span data-stu-id="c4cf4-124">_B_</span></span> <br/> |<span data-ttu-id="c4cf4-125">必須</span><span class="sxs-lookup"><span data-stu-id="c4cf4-125">Required</span></span>  <br/> |<span data-ttu-id="c4cf4-126">**数値**</span><span class="sxs-lookup"><span data-stu-id="c4cf4-126">**Number**</span></span> <br/> |<span data-ttu-id="c4cf4-127">水平距離を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4cf4-128">解説</span><span class="sxs-lookup"><span data-stu-id="c4cf4-128">Remarks</span></span>

<span data-ttu-id="c4cf4-129">MAGNITUDE は次の数式に従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="c4cf4-130">SQRT ((constantA \* A) ^ 2 + (constantB \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="c4cf4-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="c4cf4-131">例</span><span class="sxs-lookup"><span data-stu-id="c4cf4-131">Example</span></span>

<span data-ttu-id="c4cf4-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="c4cf4-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="c4cf4-133">5 を返します。</span><span class="sxs-lookup"><span data-stu-id="c4cf4-133">Returns 5.</span></span> 
  

