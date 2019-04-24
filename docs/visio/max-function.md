---
title: MAX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251462
localization_priority: Normal
ms.assetid: a17369b1-f366-3010-9e60-ae5cc101ecc8
description: リストの最大値を返します。 最大値は、正の無限大に最も近いことを意味します。
ms.openlocfilehash: ed8afbcba7f4fbf60c77f6a281389132a12a8a55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341665"
---
# <a name="max-function"></a><span data-ttu-id="6fa4f-104">MAX 関数</span><span class="sxs-lookup"><span data-stu-id="6fa4f-104">MAX Function</span></span>

<span data-ttu-id="6fa4f-105">リストの最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-105">Returns the largest number from a list.</span></span> <span data-ttu-id="6fa4f-106">最大値は、正の無限大に最も近いことを意味します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-106">Largest means closest to positive infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6fa4f-107">構文</span><span class="sxs-lookup"><span data-stu-id="6fa4f-107">Syntax</span></span>

<span data-ttu-id="6fa4f-108">MAX (\* \* *number1* \* \*, \* \* *number2* \* \*,..., \* \**数字 n* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-108">MAX(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6fa4f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6fa4f-109">Parameters</span></span>

|<span data-ttu-id="6fa4f-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-110">**Name**</span></span>|<span data-ttu-id="6fa4f-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-111">**Required/Optional**</span></span>|<span data-ttu-id="6fa4f-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-112">**Data Type**</span></span>|<span data-ttu-id="6fa4f-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6fa4f-114">_number1_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-114">_number1_</span></span> <br/> |<span data-ttu-id="6fa4f-115">必須</span><span class="sxs-lookup"><span data-stu-id="6fa4f-115">Required</span></span>  <br/> |<span data-ttu-id="6fa4f-116">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-116">**Varies**</span></span> <br/> |<span data-ttu-id="6fa4f-117">リスト内の最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="6fa4f-118">_number2_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-118">_number2_</span></span> <br/> |<span data-ttu-id="6fa4f-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fa4f-119">Optional</span></span>  <br/> |<span data-ttu-id="6fa4f-120">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-120">**Varies**</span></span> <br/> | <span data-ttu-id="6fa4f-121">リスト内の 2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="6fa4f-122">_番号 n_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-122">_numberN_</span></span> <br/> |<span data-ttu-id="6fa4f-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fa4f-123">Optional</span></span>  <br/> |<span data-ttu-id="6fa4f-124">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6fa4f-124">**Varies**</span></span> <br/> |<span data-ttu-id="6fa4f-125">リスト内の n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6fa4f-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="6fa4f-126">Return value</span></span>

<span data-ttu-id="6fa4f-127">さまざま</span><span class="sxs-lookup"><span data-stu-id="6fa4f-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="6fa4f-128">例</span><span class="sxs-lookup"><span data-stu-id="6fa4f-128">Example</span></span>

<span data-ttu-id="6fa4f-129">MAX(13 in,1 ft, 20 cm)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-129">MAX(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="6fa4f-130">13 インチを返します。</span><span class="sxs-lookup"><span data-stu-id="6fa4f-130">Returns 13 inches.</span></span> 
  

