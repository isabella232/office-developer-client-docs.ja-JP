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
description: 立ち上がりが A で、実行が B のベクトルの大きさを、それぞれの定数定数A と定数B を乗算して返します。
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420459"
---
# <a name="magnitude-function"></a><span data-ttu-id="7976c-103">MAGNITUDE 関数</span><span class="sxs-lookup"><span data-stu-id="7976c-103">MAGNITUDE Function</span></span>

<span data-ttu-id="7976c-104">立ち上がりが  _A_ で、実行が  _B_ のベクトルの大きさを、それぞれの定数  _定数A_ と定数B を掛けた値を  _返します_。</span><span class="sxs-lookup"><span data-stu-id="7976c-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7976c-105">構文</span><span class="sxs-lookup"><span data-stu-id="7976c-105">Syntax</span></span>

<span data-ttu-id="7976c-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span><span class="sxs-lookup"><span data-stu-id="7976c-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7976c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7976c-107">Parameters</span></span>

|<span data-ttu-id="7976c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="7976c-108">**Name**</span></span>|<span data-ttu-id="7976c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="7976c-109">**Required/Optional**</span></span>|<span data-ttu-id="7976c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="7976c-110">**Data Type**</span></span>|<span data-ttu-id="7976c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="7976c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7976c-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="7976c-112">_constantA_</span></span> <br/> |<span data-ttu-id="7976c-113">必須</span><span class="sxs-lookup"><span data-stu-id="7976c-113">Required</span></span>  <br/> |<span data-ttu-id="7976c-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="7976c-114">**Number**</span></span> <br/> |<span data-ttu-id="7976c-115">高さを乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7976c-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="7976c-116">_A_</span><span class="sxs-lookup"><span data-stu-id="7976c-116">_A_</span></span> <br/> |<span data-ttu-id="7976c-117">必須</span><span class="sxs-lookup"><span data-stu-id="7976c-117">Required</span></span>  <br/> |<span data-ttu-id="7976c-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="7976c-118">**Number**</span></span> <br/> |<span data-ttu-id="7976c-119">高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7976c-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="7976c-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="7976c-120">_constantB_</span></span> <br/> |<span data-ttu-id="7976c-121">必須</span><span class="sxs-lookup"><span data-stu-id="7976c-121">Required</span></span>  <br/> |<span data-ttu-id="7976c-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="7976c-122">**Number**</span></span> <br/> |<span data-ttu-id="7976c-123">水平距離を乗算する定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7976c-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="7976c-124">_B_</span><span class="sxs-lookup"><span data-stu-id="7976c-124">_B_</span></span> <br/> |<span data-ttu-id="7976c-125">必須</span><span class="sxs-lookup"><span data-stu-id="7976c-125">Required</span></span>  <br/> |<span data-ttu-id="7976c-126">**数値**</span><span class="sxs-lookup"><span data-stu-id="7976c-126">**Number**</span></span> <br/> |<span data-ttu-id="7976c-127">水平距離を指定します。</span><span class="sxs-lookup"><span data-stu-id="7976c-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7976c-128">注釈</span><span class="sxs-lookup"><span data-stu-id="7976c-128">Remarks</span></span>

<span data-ttu-id="7976c-129">MAGNITUDE は次の数式に従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="7976c-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="7976c-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span><span class="sxs-lookup"><span data-stu-id="7976c-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="7976c-131">例</span><span class="sxs-lookup"><span data-stu-id="7976c-131">Example</span></span>

<span data-ttu-id="7976c-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="7976c-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="7976c-133">5 を返します。</span><span class="sxs-lookup"><span data-stu-id="7976c-133">Returns 5.</span></span> 
  

