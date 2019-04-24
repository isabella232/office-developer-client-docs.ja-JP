---
title: MIN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251463
localization_priority: Normal
ms.assetid: b945b7c2-153f-2fc3-b768-1e975254ddf5
description: リストから最小値を返します。 最小値は負の無限大に最も近いことを意味します。
ms.openlocfilehash: 7c9eb1a8d4ce30e7ab9253c2864ecd38474e8ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360649"
---
# <a name="min-function"></a><span data-ttu-id="c4f28-104">MIN 関数</span><span class="sxs-lookup"><span data-stu-id="c4f28-104">MIN Function</span></span>

<span data-ttu-id="c4f28-105">リストから最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-105">Returns the smallest number from a list.</span></span> <span data-ttu-id="c4f28-106">最小値は負の無限大に最も近いことを意味します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-106">Smallest means closest to negative infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c4f28-107">構文</span><span class="sxs-lookup"><span data-stu-id="c4f28-107">Syntax</span></span>

<span data-ttu-id="c4f28-108">MIN (\* \* *number1* \* \*, \* \* *number2* \* \*,..., \* \**数字 n* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4f28-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4f28-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4f28-109">Parameters</span></span>

|<span data-ttu-id="c4f28-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="c4f28-110">**Name**</span></span>|<span data-ttu-id="c4f28-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c4f28-111">**Required/Optional**</span></span>|<span data-ttu-id="c4f28-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c4f28-112">**Data Type**</span></span>|<span data-ttu-id="c4f28-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="c4f28-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4f28-114">_number1_</span><span class="sxs-lookup"><span data-stu-id="c4f28-114">_number1_</span></span> <br/> |<span data-ttu-id="c4f28-115">必須</span><span class="sxs-lookup"><span data-stu-id="c4f28-115">Required</span></span>  <br/> |<span data-ttu-id="c4f28-116">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="c4f28-116">**Varies**</span></span> <br/> |<span data-ttu-id="c4f28-117">リスト内の最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="c4f28-118">_number2_</span><span class="sxs-lookup"><span data-stu-id="c4f28-118">_number2_</span></span> <br/> |<span data-ttu-id="c4f28-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="c4f28-119">Optional</span></span>  <br/> |<span data-ttu-id="c4f28-120">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="c4f28-120">**Varies**</span></span> <br/> | <span data-ttu-id="c4f28-121">リスト内の 2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="c4f28-122">_番号 n_</span><span class="sxs-lookup"><span data-stu-id="c4f28-122">_numberN_</span></span> <br/> |<span data-ttu-id="c4f28-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="c4f28-123">Optional</span></span>  <br/> |<span data-ttu-id="c4f28-124">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="c4f28-124">**Varies**</span></span> <br/> |<span data-ttu-id="c4f28-125">リスト内の n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c4f28-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="c4f28-126">Return value</span></span>

<span data-ttu-id="c4f28-127">さまざま</span><span class="sxs-lookup"><span data-stu-id="c4f28-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="c4f28-128">例</span><span class="sxs-lookup"><span data-stu-id="c4f28-128">Example</span></span>

<span data-ttu-id="c4f28-129">MIN(13 in,1 ft, 20 cm)</span><span class="sxs-lookup"><span data-stu-id="c4f28-129">MIN(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="c4f28-130">20 cm を返します。</span><span class="sxs-lookup"><span data-stu-id="c4f28-130">Returns 20 centimeters.</span></span> 
  

