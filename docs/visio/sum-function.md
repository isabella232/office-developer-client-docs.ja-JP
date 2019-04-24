---
title: SUM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251501
localization_priority: Normal
ms.assetid: fc97cef7-59c3-5be1-34fe-a40b4b33d1d6
description: 数値のリストの合計を返します。
ms.openlocfilehash: 749bf1620a26c6f4cf793a2f9e596d5720175be0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332496"
---
# <a name="sum-function"></a><span data-ttu-id="27540-103">SUM 関数</span><span class="sxs-lookup"><span data-stu-id="27540-103">SUM Function</span></span>

<span data-ttu-id="27540-104">数値のリストの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="27540-104">Returns the sum of a list of numbers.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="27540-105">構文</span><span class="sxs-lookup"><span data-stu-id="27540-105">Syntax</span></span>

<span data-ttu-id="27540-106">合計 (\* \* *number1* \* \*, \* \* *number2* \* \*,..., \* \* *[number n]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="27540-106">SUM(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *[numberN]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="27540-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27540-107">Parameters</span></span>

|<span data-ttu-id="27540-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="27540-108">**Name**</span></span>|<span data-ttu-id="27540-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="27540-109">**Required/Optional**</span></span>|<span data-ttu-id="27540-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="27540-110">**Data Type**</span></span>|<span data-ttu-id="27540-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="27540-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="27540-112">_number1_</span><span class="sxs-lookup"><span data-stu-id="27540-112">_number1_</span></span> <br/> |<span data-ttu-id="27540-113">必須</span><span class="sxs-lookup"><span data-stu-id="27540-113">Required</span></span>  <br/> |<span data-ttu-id="27540-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="27540-114">**Numeric**</span></span> <br/> |<span data-ttu-id="27540-115">最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="27540-115">The first number.</span></span>  <br/> |
| <span data-ttu-id="27540-116">_number2_</span><span class="sxs-lookup"><span data-stu-id="27540-116">_number2_</span></span> <br/> |<span data-ttu-id="27540-117">必須</span><span class="sxs-lookup"><span data-stu-id="27540-117">Required</span></span>  <br/> |<span data-ttu-id="27540-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="27540-118">**Numeric**</span></span> <br/> |<span data-ttu-id="27540-119">2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="27540-119">The second number.</span></span>  <br/> |
| <span data-ttu-id="27540-120">_番号 n_</span><span class="sxs-lookup"><span data-stu-id="27540-120">_numberN_</span></span> <br/> |<span data-ttu-id="27540-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="27540-121">Optional</span></span>  <br/> |<span data-ttu-id="27540-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="27540-122">**Numeric**</span></span> <br/> |<span data-ttu-id="27540-123">n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="27540-123">The nth number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="27540-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="27540-124">Return value</span></span>

<span data-ttu-id="27540-125">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="27540-125">Numeric</span></span>
  
## <a name="example"></a><span data-ttu-id="27540-126">例</span><span class="sxs-lookup"><span data-stu-id="27540-126">Example</span></span>

<span data-ttu-id="27540-127">合計 (5、7、12)</span><span class="sxs-lookup"><span data-stu-id="27540-127">SUM(5,7,12)</span></span>
  
<span data-ttu-id="27540-128">24 を返します。</span><span class="sxs-lookup"><span data-stu-id="27540-128">Returns 24.</span></span>
  

