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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436315"
---
# <a name="sum-function"></a><span data-ttu-id="04119-103">SUM 関数</span><span class="sxs-lookup"><span data-stu-id="04119-103">SUM Function</span></span>

<span data-ttu-id="04119-104">数値のリストの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="04119-104">Returns the sum of a list of numbers.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="04119-105">構文</span><span class="sxs-lookup"><span data-stu-id="04119-105">Syntax</span></span>

<span data-ttu-id="04119-106">SUM(\*\* *number1* \*\*, \*\* \*number2 \**,...,* \*\* *[numberN]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="04119-106">SUM(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *[numberN]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04119-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04119-107">Parameters</span></span>

|<span data-ttu-id="04119-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="04119-108">**Name**</span></span>|<span data-ttu-id="04119-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="04119-109">**Required/Optional**</span></span>|<span data-ttu-id="04119-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="04119-110">**Data Type**</span></span>|<span data-ttu-id="04119-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="04119-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04119-112">_number1_</span><span class="sxs-lookup"><span data-stu-id="04119-112">_number1_</span></span> <br/> |<span data-ttu-id="04119-113">必須</span><span class="sxs-lookup"><span data-stu-id="04119-113">Required</span></span>  <br/> |<span data-ttu-id="04119-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="04119-114">**Numeric**</span></span> <br/> |<span data-ttu-id="04119-115">最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="04119-115">The first number.</span></span>  <br/> |
| <span data-ttu-id="04119-116">_number2_</span><span class="sxs-lookup"><span data-stu-id="04119-116">_number2_</span></span> <br/> |<span data-ttu-id="04119-117">必須</span><span class="sxs-lookup"><span data-stu-id="04119-117">Required</span></span>  <br/> |<span data-ttu-id="04119-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="04119-118">**Numeric**</span></span> <br/> |<span data-ttu-id="04119-119">2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="04119-119">The second number.</span></span>  <br/> |
| <span data-ttu-id="04119-120">_numberN_</span><span class="sxs-lookup"><span data-stu-id="04119-120">_numberN_</span></span> <br/> |<span data-ttu-id="04119-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="04119-121">Optional</span></span>  <br/> |<span data-ttu-id="04119-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="04119-122">**Numeric**</span></span> <br/> |<span data-ttu-id="04119-123">n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="04119-123">The nth number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="04119-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="04119-124">Return value</span></span>

<span data-ttu-id="04119-125">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="04119-125">Numeric</span></span>
  
## <a name="example"></a><span data-ttu-id="04119-126">例</span><span class="sxs-lookup"><span data-stu-id="04119-126">Example</span></span>

<span data-ttu-id="04119-127">SUM(5,7,12)</span><span class="sxs-lookup"><span data-stu-id="04119-127">SUM(5,7,12)</span></span>
  
<span data-ttu-id="04119-128">24 を返します。</span><span class="sxs-lookup"><span data-stu-id="04119-128">Returns 24.</span></span>
  

