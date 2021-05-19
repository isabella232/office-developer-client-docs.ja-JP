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
description: リストから最小の数を返します。 最小は負の無限大に最も近い意味です。
ms.openlocfilehash: 7c9eb1a8d4ce30e7ab9253c2864ecd38474e8ff6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420837"
---
# <a name="min-function"></a><span data-ttu-id="6e0bb-104">MIN 関数</span><span class="sxs-lookup"><span data-stu-id="6e0bb-104">MIN Function</span></span>

<span data-ttu-id="6e0bb-105">リストから最小の数を返します。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-105">Returns the smallest number from a list.</span></span> <span data-ttu-id="6e0bb-106">最小は負の無限大に最も近い意味です。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-106">Smallest means closest to negative infinity.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6e0bb-107">構文</span><span class="sxs-lookup"><span data-stu-id="6e0bb-107">Syntax</span></span>

<span data-ttu-id="6e0bb-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6e0bb-108">MIN(\*\* *number1* \*\*, \*\* *number2* \*\*,..., \*\* *numberN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e0bb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e0bb-109">Parameters</span></span>

|<span data-ttu-id="6e0bb-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-110">**Name**</span></span>|<span data-ttu-id="6e0bb-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-111">**Required/Optional**</span></span>|<span data-ttu-id="6e0bb-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-112">**Data Type**</span></span>|<span data-ttu-id="6e0bb-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e0bb-114">_number1_</span><span class="sxs-lookup"><span data-stu-id="6e0bb-114">_number1_</span></span> <br/> |<span data-ttu-id="6e0bb-115">必須</span><span class="sxs-lookup"><span data-stu-id="6e0bb-115">Required</span></span>  <br/> |<span data-ttu-id="6e0bb-116">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-116">**Varies**</span></span> <br/> |<span data-ttu-id="6e0bb-117">リスト内の最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-117">The first number in the list.</span></span>  <br/> |
| <span data-ttu-id="6e0bb-118">_number2_</span><span class="sxs-lookup"><span data-stu-id="6e0bb-118">_number2_</span></span> <br/> |<span data-ttu-id="6e0bb-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="6e0bb-119">Optional</span></span>  <br/> |<span data-ttu-id="6e0bb-120">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-120">**Varies**</span></span> <br/> | <span data-ttu-id="6e0bb-121">リスト内の 2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-121">The second number in the list.</span></span>  <br/> |
| <span data-ttu-id="6e0bb-122">_numberN_</span><span class="sxs-lookup"><span data-stu-id="6e0bb-122">_numberN_</span></span> <br/> |<span data-ttu-id="6e0bb-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="6e0bb-123">Optional</span></span>  <br/> |<span data-ttu-id="6e0bb-124">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6e0bb-124">**Varies**</span></span> <br/> |<span data-ttu-id="6e0bb-125">リスト内の n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-125">The nth number in the list.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6e0bb-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="6e0bb-126">Return value</span></span>

<span data-ttu-id="6e0bb-127">さまざま</span><span class="sxs-lookup"><span data-stu-id="6e0bb-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="6e0bb-128">例</span><span class="sxs-lookup"><span data-stu-id="6e0bb-128">Example</span></span>

<span data-ttu-id="6e0bb-129">MIN(13 in,1 ft, 20 cm)</span><span class="sxs-lookup"><span data-stu-id="6e0bb-129">MIN(13 in,1 ft, 20 cm)</span></span> 
  
<span data-ttu-id="6e0bb-130">20 cm を返します。</span><span class="sxs-lookup"><span data-stu-id="6e0bb-130">Returns 20 centimeters.</span></span> 
  

