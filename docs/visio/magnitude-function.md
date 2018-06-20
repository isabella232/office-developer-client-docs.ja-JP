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
description: 返すベクトルの大きさの増加は、A の実行は、B、それぞれを掛けた値の定数 constantA と constantB。
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805812"
---
# <a name="magnitude-function"></a><span data-ttu-id="13671-103">MAGNITUDE 関数</span><span class="sxs-lookup"><span data-stu-id="13671-103">MAGNITUDE Function</span></span>

<span data-ttu-id="13671-104">台頭は、 _A_との実行は、 _B_、それぞれの定数を掛けた値は、ベクトルの大きさを返します_constantA_と_constantB_。</span><span class="sxs-lookup"><span data-stu-id="13671-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13671-105">構文</span><span class="sxs-lookup"><span data-stu-id="13671-105">Syntax</span></span>

<span data-ttu-id="13671-106">マグニチュード (* * *constantA* * *、* * *A* * *、* * *constantB* * *、* * *B* * *)</span><span class="sxs-lookup"><span data-stu-id="13671-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="13671-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="13671-107">Parameters</span></span>

|<span data-ttu-id="13671-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="13671-108">**Name**</span></span>|<span data-ttu-id="13671-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="13671-109">**Required/Optional**</span></span>|<span data-ttu-id="13671-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="13671-110">**Data Type**</span></span>|<span data-ttu-id="13671-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="13671-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="13671-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="13671-112">_constantA_</span></span> <br/> |<span data-ttu-id="13671-113">必須</span><span class="sxs-lookup"><span data-stu-id="13671-113">Required</span></span>  <br/> |<span data-ttu-id="13671-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="13671-114">**Number**</span></span> <br/> |<span data-ttu-id="13671-115">高さを乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="13671-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="13671-116">_A_</span><span class="sxs-lookup"><span data-stu-id="13671-116">_A_</span></span> <br/> |<span data-ttu-id="13671-117">必須</span><span class="sxs-lookup"><span data-stu-id="13671-117">Required</span></span>  <br/> |<span data-ttu-id="13671-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="13671-118">**Number**</span></span> <br/> |<span data-ttu-id="13671-119">高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="13671-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="13671-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="13671-120">_constantB_</span></span> <br/> |<span data-ttu-id="13671-121">必須</span><span class="sxs-lookup"><span data-stu-id="13671-121">Required</span></span>  <br/> |<span data-ttu-id="13671-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="13671-122">**Number**</span></span> <br/> |<span data-ttu-id="13671-123">水平距離を乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="13671-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="13671-124">_B_</span><span class="sxs-lookup"><span data-stu-id="13671-124">_B_</span></span> <br/> |<span data-ttu-id="13671-125">必須</span><span class="sxs-lookup"><span data-stu-id="13671-125">Required</span></span>  <br/> |<span data-ttu-id="13671-126">**番号**</span><span class="sxs-lookup"><span data-stu-id="13671-126">**Number**</span></span> <br/> |<span data-ttu-id="13671-127">水平距離を指定します。</span><span class="sxs-lookup"><span data-stu-id="13671-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13671-128">注釈</span><span class="sxs-lookup"><span data-stu-id="13671-128">Remarks</span></span>

<span data-ttu-id="13671-129">MAGNITUDE は次の数式に従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="13671-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="13671-130">SQRT ((constantA \* A) ^2 + (constantB \* B) ^2)</span><span class="sxs-lookup"><span data-stu-id="13671-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="13671-131">例</span><span class="sxs-lookup"><span data-stu-id="13671-131">Example</span></span>

<span data-ttu-id="13671-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="13671-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="13671-133">5 を返します。</span><span class="sxs-lookup"><span data-stu-id="13671-133">Returns 5.</span></span> 
  

